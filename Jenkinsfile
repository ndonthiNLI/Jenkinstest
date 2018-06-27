node('jnlp'){
   def mvnHome
   stage('Preparation') {
      git 'https://github.com/jglick/simple-maven-project-with-tests.git'
      mvnHome = tool 'mvn'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }    
   stage('Compile') {
      mvnHome = tool 'mvn'
      if (isUnix()) {
         #sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
         sh " '${mvnHome}/bin/mvn' clean compile "
      }
   }        
