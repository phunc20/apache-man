## Setup
- [Single node cluster](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html)
    - Not every file on the main distribution site can be stably downloaded, i.e. when a file seems difficult
      to download, try with another one
        - On X86 cpu structure, the executables/binary files are packed in tarballs of similar names to `hadoop-3.3.6.tar.gz  `
    - In the installation tuto, one step is to modify the `JAVA_HOME` env variable in `etc/hadoop/hadoop-env.sh`.
      It is not very clearly described, but basically you need to provide it with your preferred Java executable path.
      More precisely, `JAVA_HOME` should be the directory which contains `bin/java`, where `java` is the executable
      file.  
      
      For example, on my machine I use SDKMan for Java usage, and when I type
      ```bash
      $ which java
      /home/phunc20/.sdkman/candidates/java/current/bin/java
      ```
      so I need to set
      ```
      export java_home="/home/phunc20/.sdkman/candidates/java/current"
      ```
