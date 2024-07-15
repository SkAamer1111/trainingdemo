pipeline{
    agent any
    tools {
        jdk "JDK_17"
        maven "MAVEN_3.9"
    }
    parameters{
        choice(name: 'CHOICE', choices: ['validate', 'test', 'package', 'deploy'])
    }
    stages{
        stage('build'){
            steps{
                sh "mvn ${params.CHOICE}"
            }
        }
    }
}