job('test-pipeline){
  description('this is a test jenkins pipeline ')
  parameters{
  stringParam("Planet", defaultValue="World", description= 'This is the world')
    choiceParam("OPTION", ['option 1 (default)', 'option 2', 'option 3'])
  }
  steps {
     shell("""
	echo 'Hello World Dev!'
    """
       )
  }
  publishers{
  mailer('dhanai_rajpal@yahoo.com', true, true)
  }
  
}