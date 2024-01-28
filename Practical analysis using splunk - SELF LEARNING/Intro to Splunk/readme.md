## Intro to Splunk

1. What is splunk ? 
 
  Splunk's software can be used to examine, monitor, and search for machine-generated big data through a browser-like interface.

  <img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/58a6e20f-e9b5-4629-8318-3fc3c7ef5a65">

2. Using splunk web

   Splunk web is pre configured environment, there are three pre defined roles in splunk enterprise 
   a. Admin - Full access
   b. Power - It will perform real time searches.
   c. User - user can access own knowleadge object.

   <img width="1434" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9e9e8680-1ae8-4c16-a81e-6fea6f366ca5">

   Splunk default lauch environment

   <img width="1436" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/826cf931-1357-4e91-a395-3d730a6240bd">

3. Using search

   Search option is used to search the incident log with time span.

   ## Limiting a search by time is a key to faster result and is a best pratice.##

   Eg. Installing cmatrix in remote VM (Kali) and we can see the installation logs in splunk enterprises.

   <img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/eafc204a-201c-4836-8538-5b79d5b6e9ed">

   Commands that create statics and visualisation are called transforming commands.

   We can share the share job log with other user it will remian active for 7 days, and every 10 min we need to refresh the log search.

   We can dowload the report in csv,xml,json.

4. Exploring Events

   If we search the objects in filters by default the event will turn the list, filtered keyword would be highlighted and we can examine the logs with timespan.

   <img width="795" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/4e4c2e5f-ab43-4cdf-a946-467f04b2a1a9">

   Many events actions filter will be available.

5. Using search term

   In filters we can use terms of keywords.

      Eg. fail*, failed, FAILURE

   <img width="1437" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/e9a6e6b0-c50c-43de-85f0-5d8bf3bb3a9c">

   search terms are not case senstive  and booleans also we can use
 
   Boolean operations have an order of evaluation
   a. NOT
   b. OR
   c. AND
  Note: parenthesis () should be used

   <img width="1435" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/65b158d7-0b1c-4e1f-8875-260d173699fe">

   <img width="1432" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/0af5e8b0-be9e-4a93-8b42-ece813563eae">

   User can customize the filter as per the requirements.


6. What are commands ?

   Search splunk language contain 5 component’s

   a. search term - Fiundation of search query.
   b. commands - Commands is used to customize the log as per the need like charts, statistics and formatting.
   c. functions - How we need to display the charts and evaluate the results.
   d. arguments - It is the variables which we want to apply in the functions.
   e. clauses - It will group the result as per the requirement.

   <img width="1438" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/eafd1680-a4d7-4e61-8e7a-51cdee5edfce">

7. What are knowledge  objects?

   It is tools that help you discover and analyse the data, will be grouped in 5 categories .

   a.Data Interpretation
   b.Data classifications
   c.Data Enrichment
   d.Data Normalisation
   e.Data Model

   Knowleage object is use full for several reasons it can be create by one user and share with other user with permission granted.
   It is powerful tool for your deployment

    Data Interpretation - Fields
<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/711e8725-afba-4899-ac96-77996f26dc0d">

    Data Classification - Event Type
<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/4715e91e-c1f8-4ec4-9a43-def9cce2217a">

8. Creating Reports

   Customize the report using visualization trick and statistics charts

   <img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/f9be160b-3d3f-4c85-b0a6-7b598a1813a0">

9. Creating Dashboards

    Creating new dashboard for User
   
<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/98d04786-fded-4678-9e35-59cd9cf0734f">

<img width="1436" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/d03bd2be-1d27-4a31-b771-4b0b6f07d8d5">


Dashoard of user created 

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/3ca546e9-c8af-4fa8-b72e-7ed1ed4503ff">

As per the requirement of the report and analyses we can customize the dashboard accordingly.

10. Dashboard Studio

    Classic Dashboard 

<img width="1438" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/4dbdc82c-41af-4e9d-a891-95391076c2d4">

Cloning exisitng dashboard into studio dashboard

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/e746c2df-a1b4-4449-99a1-6cccae7bed11">

Multiple customisation available to update the classic dahsboard 

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/dd3fc9a2-2c08-4bc0-ba5d-d7dbb9bd44f9">





   



   


