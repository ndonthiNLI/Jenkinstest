node('jnlp'){
   def mvnHome
   stage('Preparation') {
      git 'https://github.com/jglick/simple-maven-project-with-tests.git'
      mvnHome = tool 'mvn'
   }  
   stage('Compile') {
      mvnHome = tool 'mvn'
         sh " '${mvnHome}/bin/mvn' clean compile "
      }
   }        
