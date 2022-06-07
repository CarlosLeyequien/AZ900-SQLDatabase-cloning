# AZ900-SQLDatabase-cloning
How to clone an SQL database and make a query

**Cloning the DB**

  1) In portal.azure.com open the shell(Top right hand side):

  ![image](https://user-images.githubusercontent.com/105960409/172474272-ca0f4de4-2394-4e59-8520-dc1ff6ca74ad.png)
  
  2) The command line(shell) will open in the bottom and load

  ![image](https://user-images.githubusercontent.com/105960409/172474488-06d7318c-80c4-4017-8ff3-021790e15172.png)

  2) Copy the link of the DB and paste it with the following command into the Azure cloud shell

  --  git clone (database link)
  
  This will clone the existing repository for the SQL DB into your Azure account:
  
  ![image](https://user-images.githubusercontent.com/105960409/172474666-e8de7207-67d5-4ad9-b52e-4a4dfc212929.png)

  3) cd into the folder that was created:

  ![image](https://user-images.githubusercontent.com/105960409/172474887-4347cb1b-6afd-43a1-a1ca-7ba888dffa7f.png)

  4) Execute the following to setup the DB: bash setup.sh
 
  ![image](https://user-images.githubusercontent.com/105960409/172475285-e19ca33e-2eaf-4833-8907-765307f014d1.png)

  5) After it finishes everything(can take 5-10 mins) an SQL server will have been created, go to the search bar, search for SQL Servers, and access that option:

  ![image](https://user-images.githubusercontent.com/105960409/172476491-d36a31e1-641c-4080-9183-552d37cb9ee0.png)

  6) Your SQL server will show in the content viewer

  ![image](https://user-images.githubusercontent.com/105960409/172476608-6b5d3356-cccf-45e8-ac69-f409e86b316c.png)

  7) When you click on your SQL server a pop-up window will appear with all the information and options on the server, the actual DB will be found in "SQL databases"   
     under the "settings" sub-menu 

  ![image](https://user-images.githubusercontent.com/105960409/172477038-f182d1c9-20f9-4a86-9e0b-8905c7300236.png)

  8) Click on the name of the DB you cloned and it will open the DB info page

  ![image](https://user-images.githubusercontent.com/105960409/172477175-477b71f3-c05c-474a-813c-e3767c6679e0.png)
  
  9) To provide access to the DB a firewall server needs to be set up in the general options tab, click on the aforementioned option:

  ![image](https://user-images.githubusercontent.com/105960409/172478054-22aaec9a-50b9-41af-8e1a-732198c1df15.png)

  10) On the landing page, scroll down to firewall rules, and either select your client ip address or add whichever IP you want to give access to:

  ![image](https://user-images.githubusercontent.com/105960409/172478339-01731579-2d5d-4696-a2c6-8890501e33e0.png)

  11) The selected IP address will be added to the whitelist:

  ![image](https://user-images.githubusercontent.com/105960409/172478811-afbb0fb3-5e8d-49fe-8b75-15f0d034da07.png)


**Make a query in a DB**

  1) In the DB information page go to the left column, last option of the first sub-menu, "query editor (preview)"

  ![image](https://user-images.githubusercontent.com/105960409/172477842-fad844a6-efc1-4d99-a4ee-1da6d5116e4b.png)

  2) Log in to the DB with the accoutn that was setup on creation(Not included in this practice)

  ![image](https://user-images.githubusercontent.com/105960409/172479050-a8ab1fe3-f084-481d-b133-c6f145c3c11c.png)

  3) The query tool will open

  ![image](https://user-images.githubusercontent.com/105960409/172479214-7062b0a6-748c-43ea-9046-d00568cda73f.png)

  4) In the cmd type in (Without quotes) "SELECT * FROM (Database you want to query info from) and click on run
     * means to select everything
     
  ![image](https://user-images.githubusercontent.com/105960409/172479763-5929ce32-212f-4bf0-ba29-acc972056253.png)

  5) The info will appear now in the bottom part, under "results"

  ![image](https://user-images.githubusercontent.com/105960409/172479872-249209cb-920e-4ddf-9834-322c9080a0b0.png)

  
**How to insert information into the SQL DB**

  1) This is done via the comand line in the DB information view

  2) Type in the command to insert: **INSERT INTO {DB NAME} ({location in the DB to insert to}) values({information to be inserted});**

  3) Click on run, it will report the change:

  ![image](https://user-images.githubusercontent.com/105960409/172481352-080db59a-ae0f-474b-bcd7-8dd625098add.png)

    3.1 To see the changes type in the command line (without quotes) "SELECT * FROM {DB name}" and click on run, the info will be displayed in the bottom with the     
    changes we made
    ![image](https://user-images.githubusercontent.com/105960409/172481792-14face79-68d0-4861-8654-135b15c94837.png)


  
