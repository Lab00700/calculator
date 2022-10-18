pipeline { 
     agent any
     	
     stages { 
          stage("Compile") { 
               steps { 
                   ./gradlew compileJava
               } 
          } 
          stage("Unit test") { 
               steps { 
                    ./gradlew test
               } 
          } 
     } 
} 
