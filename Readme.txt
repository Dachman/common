
Prerequisite to use Maven as the dependency manager for the dachlab services
----------------------------------------------------------------------------
Run this command once in the workspace: mvn -Declipse.workspace=c:/dev/java/workspace/ eclipse:configure-workspace

Build a new project based on the dachlab services
-------------------------------------------------
1. Create an Eclipse Maven Project
2. Command line in the folder : mvn eclipse:eclipse
3. Change the compiler to 1.8 (preference of the project>Java Compiler)
4. Add the following lines in the POM
	<build>
		<finalName>${artifactId}-${version}</finalName>
		<sourceDirectory>sources</sourceDirectory>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<configuration>
					<source>1.8</source>
					<target>1.8</target>
				</configuration>
			</plugin>
		</plugins>
	</build> 
5. Add the dependency to the service in the POM
6. Do Run As>Maven>Maven Install on all modules including the end program 
7. To run imageService, copy onpencv-310.jar in /lib and add it in the classpath in the runnable script
8. To run it with the prod configuration file, add the parameter -Dspring.profiles.active=prod