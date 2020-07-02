pipeline{
	agent any
	post{
	 success{
	   echo 'Pipeline concluída com sucesso!'
	 }
	}
	stages{
	 stage('Test'){
	  steps{
	   sh './mvnw package'
	   echo 'Empacotado'
	  }
	 }
	}
}
