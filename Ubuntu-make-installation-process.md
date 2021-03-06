1. Install JDK 8
   1. Run the following commands in terminal to install it from PPA.
      ```    
      sudo add-apt-repository ppa:webupd8team/java
      sudo apt-get update
      sudo apt-get install java-common oracle-java8-installer
      ```    
     2. To make sure, installation was successful, open the terminal and run the following command.
        ```    
        javac -version
        ```    
          If you get a java version back, the installation was successful.
      3. After installation, you'll need to set JAVA_HOME environment variable.
         1. In the terminal, type the following command.
            ```  
            sudo su
            ```       
         2. Next, identify where java is installed using the following command.
            ```  
            which java
            ```   
         3. Now to set the JAVA_HOME globally, we edit the bash.bashrc file. To do so, run the following command.
            ```
            gedit .bashrc
            ```  
         4. A new file will open. At the end of this file, type the following, one line at a time.
            ```    
            JAVA_HOME=/usr/lib/jvm/default-java/bin                
            export JAVA_HOME 
            PATH=$PATH:$JAVA_HOME
            export PATH
            ```    
2. Install Ubuntu make from PPA. Run the following commands to accomplish that.
   ```        
   sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make
   sudo apt update 
   sudo apt install ubuntu-make
   ```         
3. Install Android Studio using Ubuntu make.
   ```       
   umake android --accept-license
   ```         
Now, Ubuntu-make will download and install all the required components.
      
