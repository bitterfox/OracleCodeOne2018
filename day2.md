
- AdoptOpenJDK
  - background
    - JDK: JRE + tools for developer
    - OracleJDK vs OpenJDK
    - OpenJDK vs IcedTea, Zulu, OpenJ9
    - Java Is Still Free
   - What is AdoptOpenJDK
     - build farm for OpenJDK
     - History
     - Betterrev
       - Difficult to contribute
       - Make it easier
       - ended in 2016
     - IBM is building and deliver OpenJ9 on AdoptOpenJDK
       - IBM donate testing infrastructure
     
   - Build farm
     - Build OpenJDK for different archtecture and with different JVM
     - Clone Mercurial repo to github -> jenkins -> build -> test -> ship
     - Demo
   - CI
     - Binary deploy mentioned above
     - Website deploy
   - Host prep
     - machines must have different arctecture and OS
     - Keep tools and dependencies consitent between machines
       - They use Ansible to do it
       - They like agentless and simple yaml syntax
       
     
