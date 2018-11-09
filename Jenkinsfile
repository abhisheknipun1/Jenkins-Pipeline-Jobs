pipeline 
{
    agent{
        label 'master'
    }
    stages
	{
		stage('ABC')
		{
			steps
			{
				input ('Ready to go for ABC Job?')  //Asking Permission before Triggering 'ABC' Job
				build job: 'ABC', parameters: [
                    [$class: 'StringParameterValue', name: 'a', value: "${a}"],
					[$class: 'StringParameterValue', name: 'b', value: "${c}"],
					[$class: 'StringParameterValue', name: 'c', value: "${a}"],
					[$class: 'StringParameterValue', name: 'd', value: "${d}"],
				]
			}
			
		}
		stage('PQR')
		{
			steps
			{
				build job: 'PQR', parameters: [
                    [$class: 'StringParameterValue', name: 'a', value: "${a}"],
				]
			}
			
		}
		//Many More Stages may be included
	}
}
