// def gv

// pipeline {
//     agent any
//     parameters {
//         choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
//         booleanParam(name: 'executeTests', defaultValue: true, description: '')
//     }
//     stages {
//         stage("init") {
//             steps {
//                 script {
//                    gv = load "script.groovy" 
//                 }
//             }
//         }
//         stage("build") {
//             steps {
//                 script {
//                     gv.buildApp()
//                 }
//             }
//         }
//         stage("test") {
//             when {
//                 expression {
//                     params.executeTests
//                 }
//             }
//             steps {
//                 script {
//                     gv.testApp()
//                 }
//             }
//         }
//         stage("deploy") {
//             steps {
//                 script {
//                     gv.deployApp()
//                 }
//             }
//         }
//     }   
// }









pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage("checkout") {
            steps {
                echo 'Checkout the scm server for codes'
            }
        }
        stage("build") {
            steps {
                echo 'Building the application'
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                echo 'Testing the application'
            }
        }
        stage("deploy") {
            steps {
                echo 'Deploying the application'
                echo "Deploying version ${params.VERSION}"
            }
        }
    }   
}












