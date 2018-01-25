node("") {
	if (env.TAG_NAME) {
		stage("Activating TAG production"){
		}
	} else {
		stage("Initialize conjur"){
			}

		stage("checkout, Build, Test"){
			}

		stage("Analyze Code"){
			}

		stage("Generating YAML"){
			}


	        stage("Fetching Test Certs"){
			}
		stage("Build + Push Test Image"){
			withCredentials([usernamePassword(credentialsId: 'damian', usernameVariable: 'USER', passwordVariable: 'PASSWORD')]) {
                      		sh "echo  docker build --build-arg user=${USER} password=${PASSWORD}  github.com/creack/docker-firefox"
               		 }
       		 }

        	stage("Provision TestEnv"){
                	}

        	stage("Deploy OB1 Test Pod"){
                	}

        	stage("Configure APIGW"){
                	}

        	stage("Obtain JWT"){
                	}

		stage("Run Integration Tests"){
                	}

        	stage("Remove OB1 Test Pod"){
                	}

		if (env.JOB_BASE_NAME == "master") {
        		stage("Generate PROD YAML"){
         	       	}

			stage("Fetching Prod Certs"){
			}

                	stage("Build + Push Prod Image"){
                	}

                	stage("Deploy Prod Pool"){
                	}

                	stage("Update APIGW Staging"){
                	}

                	stage("Run Production Tests"){
                	}

                	stage("Update APIGW Production"){
                	}

                	stage("Update Monitoring"){
                	}
		}
	}

}
