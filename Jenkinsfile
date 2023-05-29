pipeline 
{
    agent any
    stages 
	{
    stage('hello') {
    steps
    {
    bat 'echo "hello world" '
    }
    }
    stage('test')
    {
    steps
    {
       input message: 'Waiting for approval from Manoj to download the code', submitter: 'manoj'
    git branch: 'main', url: 'https://github.com/kimoai/DevOps-task.git'
    mail bcc: '', body: '', cc: 'projects2488@gmail.com', from: '', replyTo: '', subject: 'Build to perform on a project', to: 'manoj@gmail.com'
    }
    }
    }
    post 
	{ 
    aborted 
	{ 
    bat 'echo "Project Aborted. " '
    }
    }
}