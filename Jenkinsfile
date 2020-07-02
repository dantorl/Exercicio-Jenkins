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
	 stage('Enviar para AWS'){
	  steps{
	   sh 'scp -o StrictHostKeyChecking=no target/Api-Investimentos-0.0.1-SNAPSHOT.jar ubuntu@3.19.211.210:Api-Investimentos-0.0.1-SNAPSHOT.jar'
	   echo 'Enviado para AWS'
	  }
	 }
	}
}
