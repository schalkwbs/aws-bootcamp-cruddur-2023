# Week 0 — Billing and Architecture

 ### Create GitHub repo
   Create new repo from template [ExamProCo/aws-bootcamp-cruddur-2023](https://github.com/ExamProCo/aws-bootcamp-cruddur-2023)
   New repo reachable at [schalkwbs/aws-bootcamp-cruddur-2023](https://github.com/schalkwbs/aws-bootcamp-cruddur-2023)
    
 ### Enabling Gitpod Button
   Googled the Chrome extension and downloaded from the Chrome Extension (https://chrome.google.com/webstore/detail/gitpod-always-ready-to-co/dodmmooeoklaejobgleioelladacbeki/related)
   Confirmed button was installed :![image](https://user-images.githubusercontent.com/26598534/219870419-468bc166-5ccc-4eb9-9044-2d253e4eb0c3.png)</br>
   Created a new Gitpod workspace using the new Gitpod button: ![image](https://user-images.githubusercontent.com/26598534/219870920-9ca1dc15-d6fa-473e-9b5f-0560f83b6d50.png)

## Required Homework/Tasks
   
 ### Destroy root account creds, Set MFA, IAM role
   Did most of these before the Week 0 livestream, so will just document the root account destruction and proof of new IAM account that will be used :
    "Look ma! No root user actice access keys!"![image](https://user-images.githubusercontent.com/26598534/219872666-c6fc59ae-8064-4fba-a93a-69717a9739f0.png)
    </br>
   IAM user set up with Adminstrator and Billing access, along with MFA :![image](https://user-images.githubusercontent.com/26598534/219872864-89e0c60a-ba3a-4ffa-9128-8e4a96001dde.png)
   
  ### Install AWS CLI
   Installed AWS CLI on GitPod using the following commands : </br>
    ```curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"```
    </br>
    ```unzip awscliv2.zip```
    </br>
    ```sudo ./aws/install```
    </br>
    ![image](https://user-images.githubusercontent.com/26598534/219874828-f9a2a125-bcb6-48e1-96ee-230c9edc0703.png)
    
   
   Tried to determine active credentials and got the following error as the variables have not been set : ![image](https://user-images.githubusercontent.com/26598534/219875408-ec199d5f-3660-427e-bef7-a2adeca7ee3e.png)
    
   Generated an Access key for the env var text file on Gitpod : ![image](https://user-images.githubusercontent.com/26598534/219875457-d2a0be31-92c2-41b2-9da6-c09975630893.png)
    
   Specified the values in the text file : </br>![image](https://user-images.githubusercontent.com/26598534/219875616-59fad521-237c-4de8-a65e-dd2b2049faab.png)

   Confirmed credentials on GitPod :  </br> ![image](https://user-images.githubusercontent.com/26598534/219875773-899fc07d-943b-45f1-92c1-0816f509791c.png)
   
   Next I created Budgets and the Billing Alarms using CLI :
   ![image](https://user-images.githubusercontent.com/26598534/219878092-890495d6-6b42-4d34-9695-f7a2ffb7c501.png)



