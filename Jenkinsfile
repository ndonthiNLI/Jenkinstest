node('jnlp'){
   def mvnHome
   stage('Preparation') {
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
      sh "mvn clean compile"
   }
}
