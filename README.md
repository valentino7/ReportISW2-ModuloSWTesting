# ReportISW2-testing

# start Bookkeeper tests

    mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent install

  start pitest:
  
    mvn -DwithHistory org.pitest:pitest-maven:mutationCoverage




# start Syncope tests
  
    mvn -U -T 1C clean org.jacoco:jacoco-maven-plugin:prepare-agent verify -Dinvoker.streamLogs=true -Dmodernizer.skip=true -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true -Dsass.skip=true
    
    
  Run con pit e badua (attivare il profilo di pit con -Ppit con i flag seguenti) :

    mvn -U -T 1C clean org.jacoco:jacoco-maven-plugin:prepare-agent verify org.pitest:pitest-maven:mutationCoverage surefire:test -Ppit -Dinvoker.streamLogs=true -Dmodernizer.skip=true -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true -Dsass.skip=true
  
  
  
