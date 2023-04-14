pipeline{
  agent any
  description('this is a test jenkins pipeline ')
  parameters{
  stringParam("Planet", defaultValue="World", description= 'This is the world')
    choiceParam("OPTION", ['option 1 (default)', 'option 2', 'option 3'])
  }
  stages {
	stage ("build"){
		steps {
		echo "buidling..."
		}
	}
	stage ("test"){
		steps {
			echo "testing..."
		}
	}
	stage ("deploy"){
		steps {
			echo "deploying..."
		}
	}
  }
  publishers{
	mailer('dhanai_rajpal@yahoo.com', true, true)
  }
  
}