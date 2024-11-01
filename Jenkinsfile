pipeline {
	agent any
    environment {
		NEW_VERSION = '1.0.0'
	}
	stages {
		stage("build") {
			when {
				expression {
					env.GIT_BRANCH == 'origin/master'
				}
			}
			steps {
				echo 'building the applicaiton...'
                echo "building version ${env.GIT_BRANCH }"

			}
		}
		stage("test") {
			when {
				expression {
					env.GIT_BRANCH == 'origin/test' || env.GIT_BRANCH == ''
				}
			}
			steps {
				echo 'testing the applicaiton...'
			}
		}
		stage("deploy") {
			steps {
				echo 'deploying the applicaiton...'
			}
		}
	}
}