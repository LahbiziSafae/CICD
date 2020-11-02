// Declarative pipelines must be enclosed with a "pipeline" directive.
pipeline {
    // This line is required for declarative pipelines. Just keep it here.
    agent any

    // This section contains environment variables which are available for use in the
    // pipeline's stages.
    environment {
	    region = "eu-west-3"
        docker_repo_uri = "110609031244.dkr.ecr.eu-west-3.amazonaws.com/sample-app:latest"
		task_def_arn = "arn:aws:ecs:eu-west-3:110609031244:task-definition/first-run-task-definition:3"
        cluster = "safaework"
        exec_role_arn = "arn:aws:iam::110609031244:role/ecsTaskExecutionRole"
    }
    
    // Here you can define one or more stages for your pipeline.
    // Each stage can execute one or more steps.
    stages {
        // This is a stage.
        stage('Example') {
            steps {
                // This is a step of type "echo". It doesn't do much, only prints some text.
                echo 'This is a sample stage'
                // For a list of all the supported steps, take a look at
                // https://jenkins.io/doc/pipeline/steps/ .
            }
        }
    }
}
