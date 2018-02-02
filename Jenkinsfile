node {
   def mvnHome
   stage('Preparation') { // for display purposes
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'M3'
      //Especifar versión de JDK
      env.JAVA_HOME="${tool 'JDK8'}"
      env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
      bat 'java -version'
   }
   checkout([$class: 'SubversionSCM', 
          additionalCredentials: [], 
          excludedCommitMessages: '', 
          excludedRegions: '', 
          excludedRevprop: '', 
          excludedUsers: '', 
          filterChangelog: false, 
          ignoreDirPropChanges: false, 
          includedRegions: '', 
          locations: [[credentialsId: 'e4648de6-c36f-4616-9873-72f3bf4ae4b5', 
                       depthOption: 'infinity', 
                       ignoreExternalsOption: true, 
                       local: '.', 
                       remote: 'https://svn.justicia.es/OTROS/ESCINT_FWK2/TRUNK/justihome']], 
          workspaceUpdater: [$class: 'UpdateUpdater']])
   stage('Build') {
      // Run the maven build
      bat "'${mvnHome}/bin/mvn' -V -Dmaven.test.failure.ignore clean"
   }
   stage('Results') {
      //junit '**/target/surefire-reports/TEST-*.xml'
      archive 'justihome-webapp/target/*.war'
   }
}
