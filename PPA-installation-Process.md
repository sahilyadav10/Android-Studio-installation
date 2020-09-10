1. Install JDK 8
   * Run the following commands in terminal to install it from PPA.
      ```
      sudo add-apt-repository ppa:webupd8team/java
      sudo apt-get update
      sudo apt-get install java-common oracle-java8-installer
      ```  
2. To make sure, installation was successful, open the terminal and run the following command.
   ```
   javac -version
   ```
   **If you get a java version back, the installation was successful.**
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
4. Download Android Studio package for Linux from https://developer.android.com/studio/
5. Extract it somewhere (say,home directory)
6. Open terminal, and navigate to android-studio/bin/ using the following code and execute studio.sh
    ```      
    cd android-studio/bin
    ./studio.sh
    ```
   Then, select whether you want to import previous Android Studio settings or not, and click OK.          
7. After installation completes, set the ANDROID_HOME environment variable to the location of your Android SDK installation. To do so, run the following commands in terminal.
   ``` 
   sudo gedit ~/.bashrc   
   ```
        
   Now, paste the following lines in the editor and save the file.
   ```
   export ANDROID_HOME=/home/user_directory/Android/Sdk
   export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
   export JAVA_HOME=/usr/lib/jvm/java-8-oracle
   ```   
        
You're all set to use Android Studio!
