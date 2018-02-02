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
             locations: [[credentialsId: '83063e50-9328-4fc1-a9a3-9056409c78b1', 
                          depthOption: 'infinity', 
                          ignoreExternalsOption: true, local: '.', 
                          remote: 'https://svn.justicia.es/OTROS/FRAMEWORK20/TRUNK/Codigo/Visor']], 
             quietOperation: false, workspaceUpdater: [$class: 'UpdateUpdater']])

   stage('Build') {
      // Run the maven build
      bat "${mvnHome}/bin/mvn clean install -Dmaven.test.skip=true"
   }
   stage('Results') {
      //junit '**/target/surefire-reports/TEST-*.xml'
      archive 'Visor/target/*.war'
   }
}
