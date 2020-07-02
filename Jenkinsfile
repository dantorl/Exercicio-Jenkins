pipeline{
	agent any
	post{
	 success{
	   echo 'Pipeline concluída com sucesso!'
	 }
	}
	stages{
	 stage('Testar'){
	  steps{
	   sh './mvnw test'
	   echo 'Testado'
	  }
	 }
	 stage('Empacotar'){
	  steps{
	   sh './mvnw package'
	   echo 'Empacotado'
	  }
	 }
	}
}
