# Resolution to Deploy error

Last evening when trying to deploy to a Windows server I encountered an error.  I was unable to find the exact error via Google.

The reason for this repo/README is to provide anyone looking for a solution on how to fix this problem.

During the Dowload Bundle phase of the deploy I was getting an error that stated 
> Invalid argument @ dir_s_mkdir - C:\ProgramData/Amazon/CodeDeploy/169ae977-15e6-4fc5-8f15-0fc8efeac785/d-UC5UMER6T/deployment-archive/PK

As you can see this is a very vague error.  However the solution was easier than I thought and once I figured it out I felt like I was chasing my tail for an hour.

To be safe and because I don't know much about Windows you should make sure of the following 

1. Install the CodeDeploy Agent here's how to accomplish that https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-windows.html
1. When you use the **aws deploy push** command be sure to up load your project as a zip file and not a tar file.

tl:dr: Push your file as a .zip and not .tar 
