pipeline {
    stages {
        stage ('Get AWS Access Key') {
            def aws_access_key = ''
            steps {
                aws_access_key = input(
                    id: 'aws_access_key_arg', message: 'Provide AWS Credentials', parameters: [
                        [$class: 'WReadonlyStringParameterDefinition', name: 'AWS Access Key']
                        ]
                    )
            }
            environment {
                AWS_ACCESS_KEY_ID = aws_access_key
            }
        }
        stage ('Get AWS Secret Key') {
            def aws_secret_key = ''
            steps {
                aws_secret_key = input(
                    id: 'aws_secret_key_arg', message: 'Provide AWS Credentials', parameters: [
						[$class: 'WReadonlyStringParameterDefinition', name: 'AWS Secret Key']
						]
					)
			}
            environment {
                AWS_SECRET_ACCESS_KEY = aws_secret_key
			}
        }
		stage ('Print AWS credentials') {
			steps {
				echo "AWS_ACCESS_KEY_ID = ${AWS_ACCESS_KEY_ID}"
				echo "AWS_SECRET_ACCESS_KEY = ${AWS_SECRET_ACCESS_KEY}"
			}
		}
    }
}
