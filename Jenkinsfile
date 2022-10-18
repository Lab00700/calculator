pipeline { 
     agent {
     	docker {
     		image 'openjdk:11-jdk-alpine'
     } 
     stages { 
          stage("Compile") { 
               steps { 
                    sh "./gradlew compileJava" 
               } 
          } 
          stage("Unit test") { 
               steps { 
                    sh "./gradlew test" 
               } 
          } 
     } 
} 
