
- Future of Java SE
  - Evolving and Nimble
  - Removing something is difficult for Java platform
  - Release model, previous and new
    - in previous model, if release driven feature is delayed, all of other feature will be delayed
    - every 6 montly, functionallity releases + LTS(every 3 years)
      - All release are same
    - Oracle JDK vs Oracle OpenJDK vs other OpenJDK builds
      - previously, Oracle JDK is superset of OpenJDK
      - Oracle sync thier closed codes and opened codes after JDK 11, until JDK11 they worked for it
  - Late binding of features
    - in JDK9
      - 100+ JEPs, 100+ builds
    - in JDK10
      - 10+ JEPs, 40+ builds
    - and so on
    - in JDK11, TLS1.3 is introduced which is aprooved in Aug, 2018
    - tools for new process
      - jdeps
      	- helps to migrate to modular
      - jdeprscan
      - incubator module
      	- previously, incubating APIs and specs are in only ea
	  - few of review from widely developpers
	  - have a lot of comments after those are released
	  - but after released, changing API and specs are difficult
	- incubator modules are in normal releases
      - Preview lang and vm feature
      	- for lang and vm features
  - OpenJDK
    - Project Protola
      - Container
    - Valhalla
      - data layout
    - Panama
      - better than JNI
    - Amber
    - Skara
      - not for you, for me

- Focusing the Java Roadmap
  - Oracle introduces OpenJDK builds
  - change java feature release model
    - need more faster feature release like other successed language platform on cloud like node.js
    - change java version scheme also
  - Oracle JDK supports
    - LTS
      - for who cannot follow latest version always
      - 5 years + 3 years
  - other supports
    - Red Hat also offer LTS for RHEL
  - Java commercial features will be open
    - JMC, JFR, AppCDS, ...
    - Java Usage Tracker is not in OpenJDK
  - Client technology
    - Swing still there
    - WebStart is dead in JDK11
    - JavaFX will be no longer included in JDK
    - Applet
      - NPAPI
      - Depends on brower supporting NPAPI or not
  - Oracle JDK vs OpenJDK
    - 

- Project Panama's
  - JNI
    - implementation is on out of Java
    - to interop regacy, access functionality out of Java, performance
    - GPUs and depp learning
      - all these frameworks rely on native libraries
    - now we need native for those purpose
      - need a easy way to do it


- Graal

- Functional Exception Handling in Java

- GraalVM
  - CE and EE
  - polyglot JIT VM framework
    - JVM lang, JS, Ruby, R, python, C, C++, ...
  - about 20 times faster than JVM for some benchmark program
    - Streaming
  - about 2.x times faster for Matrix multiplication benchmark
    - by Escape analysis
  - truffle
    - Graal.js
      - ECMAScript 6 compatible
      - 1 ~ 13x faster than Nashorn, same ore less peformance vs V8
    - TruffleRuby
      - no need to change Ruby code
      - quite faster than CRuby and JRuby
    - FastR
      - 13~37x faster than GNU R 3.4.0
    - Python
      - Supporting NumPy and SciPy is important
      - working hard on it
  - native packaging
    - currently there is application cannot applicate
    - quite better startup time and memory footprint
    - working on Window support
  - embeded
    - in Oracle DB
    
