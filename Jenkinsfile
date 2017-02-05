node {
   def stepstats =[:]
   
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/eladnachum/Jenkinspipeline.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      //mvnHome = tool 'M3'
      echo "stage1"
      stepstats.put("stage1","pass")
   }
   if (false) {
    stage('Build') {
      // Run the maven build
      if (isUnix()) {
         echo "inUnix"
         //sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      } else {
          echo "notUnix"
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
    }
    }
   
   if (stepstats['stage2']=='pass'){
    stage('Results') {
      //junit '**/target/surefire-reports/TEST-*.xml'
      //archive 'target/*.jar'
      echo "stage3"
   }}
   else
   {
       stage('Failed stage2') {
           echo 'stage 2 failed'
       }
   }
}
