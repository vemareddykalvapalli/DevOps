# DevOps
Sample projects
Jenkins – Tomcat Setup
Advertisements
 Previous Page Next Page  
The following prerequisites must be met for Jenkins Tomcat setup.
Java (TM) SE Run Time Environment (build 1.7.0_60-b19)

Java Hotspot (TM) 64-bit Server VM (build 24.60-b09, mixed mode)
pen JDK Runtime Environment (rhel-2.3.10.4.el6_4-x86_64)

Open JDK 64-Bit Server VM (build 23.7-b01, mixed mode)

We assume the readers of this tutorial have Java 1.7.0_60 installed on their system before proceeding for this tutorial.

In case you do not have Java JDK, you can download it from the link Oracle

Step 2: Verifying Java Installation
Set the JAVA_HOME environment variable to point to the base directory location where Java is installed on your machine. For example,

OS	Output
Windows	Set Environmental variable JAVA_HOME to C:\ProgramFiles\java\jdk1.7.0_60
Linux	export JAVA_HOME=/usr/local/java-current
oijdglkdjg

The second way is to manage the Post-Receive URLs yourself:
github repository administration
Go to your Jenkins instances root page.
If your Jenkins instance has security enabled, login as a user who has the Overall | Administer permission.
Select the Manage Jenkins link on the left hand side of the screen.
Select the Configure System link.
In the GitHub Web Hook section select the Manually manage hook URLs option.
For each project that you want to have triggering builds, you need to open the Repository Administration screen on that GitHub project's page.
Select the Service Hooks tab.
Select the Post-Receive URLs hook.
Add the URL, which will be the root URL of your Jenkins instance with /github-webhook appended.
Jenkins instanceOnce you have configured your Jenkins instance for receiving the push notifications, you can enable jobs being triggered via the push notifications:
Goto your Jenkins instance job.
Select the Configure link on the left hand side of the screen.
Select the Build when a change is pushed to GitHub checkbox and save the configuration.
