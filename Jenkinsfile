pipeline {
    agent any
    tools{
        maven 'MAVEN_PATH'
    }
    environment{
        var1='kamal'
        var2='Dinesh'
        var3='poovendhan'
        dinesh_token=credentials('DINESH-TOKEN')
        barathi_token=credentials('BARATHI-TOKEN')
    }
    parameters{
        string(name:'NAME',description:'Please give your name ?')
        choice(name:'BRANCH',choices:['good','bad'],description:'please choose your choice ?')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the job'
               echo "Build job name is: $var1"
                echo "My secret token is $dinesh_token"
                echo "My username is $barathi_token_USR"
                echo "My password is $barathi_token_PSW"
                //sh "mvn -version"
            }
        }
        
        stage('Test')
        {
            steps{
                echo 'Testing the job'
                echo "Test job name is: $var2"
                echo "My secret token is $dinesh_token"
            }
        }
        
        stage('Deploy')
        {
            steps
            {
                echo 'Deploying into production server'
                echo "Deploy job name is: $var3"
                echo "My secret token is $dinesh_token"
            }
        }
        
        stage('Environment variable')
        {
            steps{
                echo "Build number of the job is: $env.BUILD_NUMBER"
                echo "NAme of the job is: $env.JOB_NAME"
                echo "Job url is: $env.JOB_URL"
                echo "The build tag is: $env.BUILD_TAG"
                echo "The build URL is: $env.BUILD_URL"
                echo "The node name is: $env.NODE_NAME"
            }
        }
        
    }
}
