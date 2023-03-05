pipeline {
    agent { label 'master'}

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
            
            post{
                always{
                    sh 'curl -s -X POST https://api.telegram.org/bot5956232176:AAEGFFLQDInXF8eBSlN3qSELMllJx-LFk50/sendMessage -d chat_id=721861960 -d text="Good Morning!"'
                }
            }
        }
    }
    
}
