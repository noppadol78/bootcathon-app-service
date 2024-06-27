## In the resource group page
Click `+ Create` <br>
![+ Create](click_create.png)
<br>
<br>

## Create a new Azure Database for PostgreSQL Flexible server
1. Type `postgres flexible` on the search bar, and select `create` inside **Azure Database for PostgreSQL Flexible server** box.
   ![choose "Postgres Flexible"](choose_postgres_flexible.png)
   
2. Enter the following values:<br>

   ***Project details***<br>
   * **Subscription:**  Select your Azure subscription.
   * **Resource group:**  Select your resource group, ex. `rg-flask-demo`.

   ***Server details***<br>
   * **Server name:**  Enter a new server, ex. `db-flask-demo`.
   * **Region:**  Select an Azure location, such as `Southeast Asia`.
   * **Workload type:**  Select `Development`.

   ***Authentication***<br>
   * **Authentication method:**  Select `PostgreSQL authentication only`.
   * **Admin username:**  Enter username, ex. `dbadmin`.
   * **Password:**  Enter password.
   * **Confirm password:**  Enter password.

   ![Enter values](create_db1.png)

3. Select `Review + Create`<br>

4. Click `Create`.<br> 
   ![Click "Create"](create_db2.png)

5. Click `Create server without firewall rules`.<br>
   *(For this demo, we will ignore about security practice.)*<br>

   ![Click "Create server without firewall rules"](create_db3.png)

6. Wait a few minutes until the PostgreSQL will be created.<br>
   ![DB creation complete](db_create_complete.png)


[< Previous step ](../Step.0/Prepare_Azure_subscription_and_resource_group.md) &emsp; - &emsp; **[Home](../README.md)** &emsp; - &emsp; [Next step >](../Step.2/Create_Web_App.md)


