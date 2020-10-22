/*
Copyright CESSDA ERIC 2017-2019

Licensed under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.
You may obtain a copy of the License at
http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
*/
pipeline {
	options {
		buildDiscarder logRotator(numToKeepStr: '20')
	}

	environment {
		product_name = 'cdc'
		module_name = 'userguide'
		image_tag = "${docker_repo}/${product_name}-${module_name}:${env.BRANCH_NAME}-${env.BUILD_NUMBER}"
	}

	agent any

	stages {
		// Compiles documentation and outputs it to ./_build
		stage('Build Documentation') {
			agent {
				dockerfile {
					filename 'jekyll.dockerfile'
					reuseNode true
				}
			}
			steps{
				sh 'mkdir -p _site'
			}
		}
		stage('Build Profiles') {
			steps {
				sh 'docker run --rm -i -u $(id -u) -v "$(pwd)":/src klakegg/saxon xslt -s:cessda.metadata.profiles/CDC\\ 1.2.2\\ PROFILE/cdc_122_profile.xml -xsl:cessda.metadata.profiles/CDC\\ 2.5\\ PROFILE/Resources/cdc_profile_Documenter.xsl -o:_site/cdc_122_profile.html'
				sh 'docker run --rm -i -u $(id -u) -v "$(pwd)":/src klakegg/saxon xslt -s:cessda.metadata.profiles/CDC\\ 2.5\\ PROFILE/cdc25_profile.xml -xsl:cessda.metadata.profiles/CDC\\ 2.5\\ PROFILE/Resources/cdc_profile_Documenter.xsl -o:_site/cdc_25_profile.html'
			}
			post {
				success {
					publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '_build/html/', reportFiles: 'index.html', reportName: 'CDC Documentation'])
				}
			}
		}
		stage('Build Nginx Container') {
			steps {
				sh "gcloud auth configure-docker"
				sh "docker build -t ${image_tag} ."
				sh "docker push ${image_tag}"
				sh "gcloud container images add-tag ${image_tag} ${docker_repo}/${product_name}-${module_name}:${env.BRANCH_NAME}-latest"
			}
			when { branch 'master' }
		}
		stage('Deploy Nginx Container') {
			steps {
				build job: 'cessda.cdc.deploy/master', parameters: [string(name: 'userguide_image_tag', value: "${env.BRANCH_NAME}-${env.BUILD_NUMBER}")], wait: false
			}
			when { branch 'master' }
		}
	}
}
