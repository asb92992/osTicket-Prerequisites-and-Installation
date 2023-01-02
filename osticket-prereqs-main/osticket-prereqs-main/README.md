<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure

- create a resource group

- windows 10 virtual machine
<h2>Installation Steps</h2>

![prequisit OsTicket](https://user-images.githubusercontent.com/58159183/210190696-4722aad2-d222-498f-8ebb-88134cfaade0.gif)
</p>
<p>
In my gif I am creating my environment in Azure for the OsTicketing system that I will be making in Azure.
</p>



<br />

![Installation osTicket part1](https://user-images.githubusercontent.com/58159183/210194207-274a3e84-8edf-4d07-b61f-cab442238678.gif)

</p>
<p>
I connected to the VM with remote desktop then began installing MySQL 5.5, all x86 PHP versions, PHP manager and Microsoft visual C++.
</p>
<br />

</p>
<p>

![Installation osTicket part2](https://user-images.githubusercontent.com/58159183/210272811-5268d472-276c-4139-86a1-1ad99d2c12da.gif)

</p>
<p>

- In this gif I downloaded osTicket and copy the upload folder into c:\inetpub\wwwroot

- Within c:\inetpub\wwwroot, rename upload to osTickt

- I then went to IIS and click on sites > default> osticket and went to the right side of osticket and clicked on browse 80

- In osTicket i clicked on php manager and then click on enable or disable an extension and then enable Enable php_imap.dll, php_intl.dll, php_opcache.dll

- I went back to the browser to refresh the osTicket and observe the changes and procedded to rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php  To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

- I then procedded to assign permission to ost-config.php and disable inheritance and remove all then set new permissions 
to everyone.
</p>
<br />

![Installation osTicket part3](https://user-images.githubusercontent.com/58159183/210281145-7aa26fbf-e448-4f6b-a2b4-91ded9af7729.gif)

</p>
<p>
  
  - In this gif I continue setting up osTIcket in the browser and instal HeidiSQL
  
  - Continue making a username and password for MYSQL database
  
  - Then after making sure that everything work correctly I then proceeded to clean up osTicket by deleteing C:\inetpub\wwwroot\osTicket\setup and setting permissions to read only in C:\inetpub\wwwroot\osTicket\include\ost-config.php
