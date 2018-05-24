# uploadingasptoiis-
This is a tutorial is all about " how to host an ASP.NET webapp to iis and access it webapp locally with other devices"



How to host your asp.net website on IIS (Internet Information Services), and access it locally
1.	Create a new Project(File->New->Project), and select Asp.Net Web Application (.Net Framework), and click ok

 ![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/1.png)

2.	Select MVC templates, and change the authentication to Individual User Accounts

![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/2.png)









3.Publish your project, right-click the project name, and click publish
 ![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/3.png)
 
 
4.Make sure that you are in the Folder tab in the pick a publish target, and select a directory for the published project, then click publish.
 ![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/4.png)
 
 
5. Open your IIS, right-click “Sites” and click add Website


![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/5.png)



6. Fill-up the necessary information and select the path of the project you published awhile ago in the visual studio, and click ok
![alt text](https://github.com/mbflores/uploadingasptoiis-/blob/master/images/6.png)












7. Application Pools-> right-click your Website->Advanced Settings, then change the value of Identity (Process Model) to LocalSystem, then click ok.

 











8. This time you need to register your website, together with the “PORT” you supplied a while ago in step 6.
Register the C:\Windows\System32\drivers\etc 
*There is no HostName Entered, so the url you would like to register is “localhost”

 









9. Go to your lovely browser to test the URL of your site if your website is up and running
 
















In order for your website to be locally accessed by other devices from your local area network.
 

1.	Add new Inbound Rule, click port->next, select tcp, select specific port “8080” for my case, where in that is the port I used in step 6 earlier. -> next, click allow the connection->next->next-> and name the rule you would wanted to, then click finish

 
2.	Open website, using another device connected in your network, and access  your unit’s ip address:port(pertaining to localhost:8080) in my case, my unit’s ip is “192.168.1.5”, the the Url that I would like to access in my phone is, 192.168.1.5:8080

