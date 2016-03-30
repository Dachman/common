
Prerequisite to use Maven as the dependency manager for the dachlab services
----------------------------------------------------------------------------
Run this command once in the workspace: mvn -Declipse.workspace=c:/dev/java/workspace/ eclipse:configure-workspace

Build a new project based on the dachlab services
-------------------------------------------------
1. Create an Eclipse Maven Project
2. Command line in the folder : mvn eclipse:eclipse
3. Change the compiler to 1.8 (preference of the project>Java Compiler)
4. Add the dependency to the service in the POM
5. Do Run As>Maven>Maven Install on all modules including the end program