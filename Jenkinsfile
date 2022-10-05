pipeline{
	agent any
		stages{
			stage('checkout'){
				steps{
					git 'https://github.com/SUMALATHA-AVULA/batch8.git'
				}
			}
			stage('compile'){
				steps{
					sh 'mvn compile'
				}
			}
			stage('codeReview'){
				steps{
					sh 'mvn pmd:pmd'
				}
			}
			stage('UnitTest'){
				steps{
					sh 'mvn test'
				}
			}
			stage('MetricCheck'){
				steps{
					sh 'mvn cobertura:cobertura -dcobertura.report.format=xml'
				}
			}
			stage('package'){
				steps{
					sh 'mvn package'
				}
			}
