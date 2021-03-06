hoge


- Intel
  - Intel contribute to OpenJDK with Oracle togather
  - JDK9's features
    - Jigsaw, VarHandle, JShell, etc
    - VarHandle: API to replace Unsafe
    - Compact String
  - JDK10's features
    - LVTI, GC Interface, Parallel FullGC for G1
    - AppCDShare, Heap Allocation on Alternative Memory Devices, Graal
    - around 400 improvement in JDK 10
  - JDK11
    - ZGC, Flight recorder, Single file execution
    - X86 optimizations

  - x86 optimization in general for JDK 10 and 11
    - improvement in vectorization
    - instrinsics performance by using avx512
    - FMA vector
    - Base64 intrinsics
  - Array compare: vectorizedMismatch
    - 240% faster than jdk11
  - Sqrt vectorization
    - 600%~ faster
  - AVX512
    - 170% faster than AVX2
  - FMA
    - FMA API was added in JDK9
    - Vectorized in JDK10
  - Base64
    - 200% faster by optimization
  - PM
    - Whole Java heap on PM
      - Available from JDK 10
      - -XX:AllocateHeapAt/mnt/pmem1
    - Partial Java Heap on PM
      - Place old gen on PM and young gen on DRAM
      - Java caching usage for HBase
    - Application directed allocate on PM
      - DirectByteBuffer
   - VectorAPI
     - Express vector algorithms in Java
     - Able to use CPU vector operation
     - part of Panama
   - Direct IO
   - RDMA
     - JEP337
   - Accelarating IO
   - JDK 12
     - 210 improvement for Hotspot
   - Future feature
     - Vector API
     - Limit Speculative exec.
     - RDMA network sockets
     - JVM Constant API
     - Intrinsics for LDC and INDY
     - etc
     - Skara
       - Move to git
       - /Project-Skara/jdk/
     - Loom, Panama, Value types, Valhalla, Metropolise      

- Schenandoh
  - Do concurrent compaction
  - "GC Handbook"
  - Available JDK8, 10, 11(Developper build)

- Nestmate and
  - NestMate
    - new Inner().a if a is private
      - access$000
      	- getfield
    - JVM SPec
      - Accessible by same class
    - JLS
      - Accessible by same OR NESTED class
    - This missmatch breaks reflection
      - Inner's private hello can be accessed from outer, but reflection is not
    - Nestmates Attribute
      - NestMembers attribute and  NestHost attribute
      	- outer class has NestMembers attribute
  - Condy
    - constant dynamic
    - indy comes for dynamic languages
    - indy to return constants is overhead
      - BootstrapMethod and ConstantCallSite, MethodHandle returns constat
    - condy
      - No CallSite or target MH
    - Usecases
      - Con-capturing lambda

- Vankat

- Paul Sandoz
  
- Keynote
  - 405 sessions
  - GitHub loves Java
    - Project Skara
    - hydro
      - Resque(on redis)
      - Webhooks(kestrel)
      - Analytics(Kafka)
      - datapipeline platform
      - They develop by ruby first
      - But they move it to Java
      	- due to parallelism, performance, typing, ecosystem issue
   - Java
     - 6 monthly release
     - Jigsaw
     - jdeps
     - support model
       - Java is still free
     - Projects
       - Amber
       	 - LVTI
	 - Switch expr
	 - record(value) class
	 - Type inference by instanceof + pattern match
       - Loom
       	 - jextract
       - Panama
       - Valhalla
