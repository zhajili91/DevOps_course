pipeline {
    agent any
    tools {
        maven "maven-3.6"}
    stages {

//         stage('Increment Version') {
//             steps {
//                 script {
//                     echo 'incrementing app version...'
//                     sh 'mvn build-helper:parse-version versions:set \
//                         -DnewVersion=\\\${parsedVersion.majorVersion}.\\\${parsedVersion.minorVersion}.\\\${parsedVersion.nextIncrementalVersion} \
//                         versions:commit'
//                     def matcher = readFile('pom.xml') =~ '<version>(.+)</version>'
//                     def version = matcher[0][1]
//                     env.IMAGE_NAME = "$version-$BUILD_NUMBER"
//                             }
//             }
//         }
        stage('Build App') {
            steps {
                script{
                    echo 'Building the Application'
                    sh "mvn package"
                    }
            }
        }
        stage('Deploying Step') {
            steps {
                echo 'Deploy the App'
            }
        }
    }
}