pipeline
{
	agent any
	stages
	{
		stage('build')
		{
			steps
			{
				git 'https://github.com/prasenjitkovair/JenkinsDemo.git'
			}
		}
		
		stage('Compile Stage')		
		{	
			steps			
			{	
				echo '1.) Compile Stage Started....'			
				withMaven(maven : 'maven_3_6_0'){
					sh 'mvn clean compile'
				}
			  	echo '1.) Compile Stage Ended...'		
			}	
		}

		stage('Testing Stage')		
		{			
			steps			
			{				
				echo '2.) Testing Stage Started....'
				withMaven(maven : 'maven_3_6_0'){
					sh 'mvn test'
				}
				echo '2.) Testing Stage Ended...'
			}
					
		}

		stage('test')
		{
			steps
			{
				echo 'testing..'
			}
		}
	}
	
}
