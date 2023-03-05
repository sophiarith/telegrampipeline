pipeline {
    agent { label 'master'}
    environment{
        TODAY = "Monday" 
    }
    parameters {
        string(name: "NAME_STRING", defaultValue: "dara", trim: true, description: "Enter your name")
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "TODAY is ${TODAY}"
                echo "Build Number: ${env.BUILD_NUMBER}"

            }
            
            post{
                always{
                    sh 'curl -s -X POST https://api.telegram.org/bot5956232176:AAEGFFLQDInXF8eBSlN3qSELMllJx-LFk50/sendMessage -d chat_id=721861960 -d text="Good Morning! ${NAME_STRING}"'
                }
            }
        }
    }
    
}
