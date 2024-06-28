## Fork the demo code
1. Sign in to your GitHub account.
2. Navigate to https://github.com/Azure-Samples/msdocs-flask-postgresql-sample-app.
3. Select `Fork`.
4. Select `Create Fork`.
![Create Fork](create_fork.png)

## In the Web App page
1. Select `Settings` > `Environment variables`. <br>
2. In `App Settings` , click `+ Add`.

![Add Environment Variable](add_env_var.png)

3. Enter the following values:<br>
   **Name**: `AZURE_POSTGRESQL_CONNECTIONSTRING`<br>
   **Value**: `dbname=python-postgres-database host=<POSTGRESQL_NAME>.postgres.database.azure.com port=5432 sslmode=require user=<USERNAME> password=<PASSWORD>`

![Enter Variable](enter_var.png)

4. Click `Apply`.

5. Click `Apply` on **App Setting** page

![Apply Variable](apply_var.png)


<br>

## In the Deployment Center page
Select `Deployment` > `Deployment Center` <br>
![Deployment Center](deployment_center.png)
<br>

Enter the following values:<br>

1. **Source**: select `GitHub`.<br>
   By default, **GitHub Actions** is selected as the build provider.

2. Sign in to your GitHub account and follow the prompt to authorize Azure.

3. **Organization**: select your account.

4. **Repository**: select `msdocs-flask-postgresql-sample-app`.

5. **Branch**: select `main`.

![Setup Source](setup_source.png)

6. In the top menu, select `Save`.<br>
   App Service commits a workflow file into the chosen GitHub repository, in the `.github/workflows` directory.

7. Select `Logs`. A deployment run is already started.

8. In the log item for the deployment run, select `Build/Deploy Logs`. 
   ![Deploy Log](deploy_log.png)

9. You're taken to your GitHub repository and see that the GitHub action is running. The workflow file defines two separate stages, build and deploy. Wait for the GitHub run to show a status of **Complete**. It takes about 5 minutes.<br>
If the GitHub Action workflow job failed, try re-run the jobs again.

   ![GitHub Actions](github_actions.png)

## Generate database schema
The easiest way to run Flask database migrations is in an SSH session with the App Service container.

1. In the App Service page, select `Development Tools` > `SSH`.

2. Click `Go`

   ![Open SSH](open_ssh.png)

3.  In the SSH terminal, run `flask db upgrade`. <br>
    If it succeeds, App Service is connecting successfully to the database. <br>
    Only changes to files in /home can persist beyond app restarts. Changes outside of /home aren't persisted.

4. Click `Create`.<br> 
   ![Click "Create"](create_web_app2.png)

5. Wait a minute until the web app will be created.<br>
   Then Click `Go to resource`.

   ![Web App creation complete](web_app_create_complete.png)



[< Previous step ](../Step.1/Create_PostgreSQL_database.md) &emsp; - &emsp; **[Home](../README.md)** &emsp; - &emsp; [Next step >](../Step.3/Deploy_code_from_GitHub.md)

