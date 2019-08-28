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
pipeline{
    environment {
        product_name = cdc
        module_name = userguide
        image_tag = image_tag = "${docker_repo}/${product_name}-${module_name}:${env.BRANCH_NAME}-${env.BUILD_NUMBER}"
    }

    agent any

    stages {
        // Compiles documentation and outputs it to ./_build
        stage('Build Documentation') {
            agent {
                docker {
                    image 'ddidier/sphinx-doc'
                    args '--entrypoint=""' // Unset the image entrypoint, the build will fail without this
                    reuseNode true
                }
            }
            steps{
                sh 'make html'
            }
        }
        stage('Build Nginx Container'){
            steps{
                sh "docker build -t ${image_tag} ."
            }
        }
    }
}
