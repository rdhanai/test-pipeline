pipeline{
  agent any
   environment{
        firstname = 'Rajpal'
        lastname = 'Dhanai'
        secrect = credentials('employee_id')
    }
  stages {
	stage ("build"){
		steps{
                echo 'Building...'
                echo 'Welcome $firstname $lastname to pipeline project! your employee id is $secrect'
            }
	}
	stage ("test"){
		when {
			express{
				BRANCH_NAME == 'develop' 
			}
		}
		steps {
			echo "testing... on branch : ${BRANCH_NAME}"
		}
	}
	stage ("deploy"){
		steps {
			echo "deploying..."
		}
	}
  }
  post{
        
        always{
            echo 'I will be always executed'
        }
        success{
            echo 'I will be executed only on success'
        }
        failure{
            echo 'I will be executed only on failure'
        }
        unstable{
            echo 'I will be executed on unstable'
            
        }
    }
}