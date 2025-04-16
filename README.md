
![Screenshot 2025-03-15 190857](https://github.com/user-attachments/assets/5ac6045a-86bf-4b1a-b068-d695f4e7820e)


</p>

<h1>Deploying Active Directory</h1>
This tutorial explores deploying an Active Directory environment, from creation and management to deactivation and removal.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Powershell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10</b> (21H2)

<h2>High-Level Deployment and Steps</h2>

- Install Active Directory 
- Create a Domain Admin user within the domain
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create users and attempt to log into client-1 with one of the users
<h2>Lifecycle Stages</h2>

<p>
  
![Screenshot 2025-03-10 044619](https://github.com/user-attachments/assets/72eae983-1277-4d03-826c-26546e94bc81)


</p>
<p>
Select both virtual macines, click on the three dots and start them both.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 044626](https://github.com/user-attachments/assets/19cfb982-7484-4418-936e-53731efbf46f)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 044751](https://github.com/user-attachments/assets/f2e04937-5ac1-4855-be0c-777ef8c6c27f)

</p>
<p>
Open Remote Desktop and copy dc-1 public ip address to computer in Remote Desktop.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 044808](https://github.com/user-attachments/assets/24e9c27f-e062-48a5-bf42-aa4b7bd63369)

</p>
<p>
Login as labuser
</p>
<br />

<p>
  
![Screenshot 2025-03-10 044823](https://github.com/user-attachments/assets/e9156049-a0e9-4de4-93a5-b4f077fd5c92)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050156](https://github.com/user-attachments/assets/18e1c14e-519f-4b8b-9cf0-c5ef4603016f)

</p>
<p>
In server manager click on Add Roles and Features. Click on Next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050230](https://github.com/user-attachments/assets/0a9d2f4e-059d-46dd-81a2-39aa6b93a886)

</p>
<p>
Select Next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050250](https://github.com/user-attachments/assets/c26acae4-30c8-43ce-81f8-8aa546834bed)

</p>
<p>
There should be only one server to select. Click Next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050338](https://github.com/user-attachments/assets/fa9fd01f-0a19-4f90-b92a-984463885979)

</p>
<p>
Click Add Features.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050354](https://github.com/user-attachments/assets/160fe28e-928e-4130-8eac-d31664f955ae)

</p>
<p>
Check Active Directory Domain Services and click Next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050407](https://github.com/user-attachments/assets/fafe4205-5345-4767-80ec-0711819ecd9e)

</p>
<p>
Leave as is and click next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050421](https://github.com/user-attachments/assets/a00b676c-632d-4793-9dc0-17e8e013460f)

</p>
<p>
Click next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050444](https://github.com/user-attachments/assets/ba45336c-39f3-4815-a460-dd82a26b7e95)

</p>
<p>
Check the Restart the destination server automatically if required box and select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050514](https://github.com/user-attachments/assets/98dae871-4fb8-41f9-902c-1323878012a8)

</p>
<p>
Select Install.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050630](https://github.com/user-attachments/assets/4c38f7fa-333f-4673-9cff-afe5ac576135)

</p>
<p>
Once the installation is complete select close.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050739](https://github.com/user-attachments/assets/c0aa4b17-366a-4863-a54b-35db6b27e9b6)

</p>
<p>
Now that active directory is installed, I can make the server a domain. Go back to Server Manager and click on the notification flag on the top right.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050818](https://github.com/user-attachments/assets/e6f4e11e-83cd-4d30-957a-487b3a892c84)

</p>
<p>
Click on "Promote this server to a domain controller".
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050913](https://github.com/user-attachments/assets/a50b6fef-ecb9-4a47-8a3c-128171bd4773)

</p>
<p>
Select Add a new forest and made mydomain.com as the root domain name. Click next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 050958](https://github.com/user-attachments/assets/11eb3879-99ff-4d12-83d7-1a48029b7720)

</p>
<p>
Left checked boxes as is and created a password. Click next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051033](https://github.com/user-attachments/assets/337be418-6aee-4ce0-a851-f85d4852686e)

</p>
<p>
Uncheck Create DNS Delegation and click next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051054](https://github.com/user-attachments/assets/8f6146b5-0368-4ba5-893e-124b0cbbcc56)

</p>
<p>
Select next.
<br />

<p>
  
![Screenshot 2025-03-10 051113](https://github.com/user-attachments/assets/74ae2524-8506-40da-900a-e14fb0819816)

</p>
<p>
Select next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051128](https://github.com/user-attachments/assets/dda7f810-7089-4505-aa25-d29eba03d35c)

</p>
<p>
Select next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051212](https://github.com/user-attachments/assets/d3e25d43-8f98-4531-817b-8dfb8ebd9509)

</p>
<p>
Click install.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051221](https://github.com/user-attachments/assets/4ea94081-c789-41f0-ad04-42823c32ef98)

</p>
<p>
The installaton is in progress. 
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051520](https://github.com/user-attachments/assets/b0bdd8ce-f7a5-4312-8ccf-22a3dd0c30f2)

</p>
<p>
The sever should restart automatically.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 051917](https://github.com/user-attachments/assets/1cb6d7ff-922b-41db-b2bd-31453dd88634)


</p>
<p>
Login using mydomain.com\labuser to access the remote server as a domain.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052035](https://github.com/user-attachments/assets/7b671485-4f05-4e25-b11c-cde875c771b3)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052424](https://github.com/user-attachments/assets/83bca5db-24b3-4ce2-8d00-3a89567ff11a)

</p>
<p>
Click on the start menu and select Active Directory Users and Computers.
</p>
<br />


<p>
  
![Screenshot 2025-03-10 052613](https://github.com/user-attachments/assets/67dfcb1e-eb98-46d8-bc1c-d95687ef6d0b)

</p>
<p>
Right-click on mydomain.com, hover over new and select Organizational Unit.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052728](https://github.com/user-attachments/assets/44f8bbac-72e7-4628-be7e-acbf310731eb)

</p>
<p>
Name the OU "_EMPLOYEES" and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052804](https://github.com/user-attachments/assets/6e549266-2376-41f5-9fef-8555e55e8ed7)

</p>
<p>
Once the "_EMPLOYEES" oraganization unit has been created, go back to mydomain.com, hover over new, and select Organiztional Unit.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052832](https://github.com/user-attachments/assets/3b5ca154-9b81-4f7e-a02e-f87c0ef8578d)

</p>
<p>
Name the OU "_ADMINS" and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052840](https://github.com/user-attachments/assets/e5b6356f-69b6-49af-992c-550d5e434bc6)

</p>
<p>
Both organizaional units have been created.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 052925](https://github.com/user-attachments/assets/88e0a735-8204-459c-97c8-8547440d8f64)

</p>
<p>
Right-click on mydomain.com and select refresh.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053044](https://github.com/user-attachments/assets/66bf6ade-d76a-4a66-8bf9-b1f4cdb3bb76)

</p>
<p>
In the _ADMINS organizational unit right click, hover over new, and select user.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053203](https://github.com/user-attachments/assets/b3741705-8bb0-4a1c-87cb-355aec5932bf)

</p>
<p>
Created a new user as Jane Smith and select next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053240](https://github.com/user-attachments/assets/ecedceb1-3da4-43c8-9c46-1cc5763d4736)

</p>
<p>
Created a password and check password never expires for the sake of the lab. Click Next.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053253](https://github.com/user-attachments/assets/6adf5a30-6182-44c9-bbcc-352159af92e9)

</p>
<p>
Select Finish.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053324](https://github.com/user-attachments/assets/e10c4f27-dbee-4381-9fc3-a0189ddf49a3)

</p>
<p>
Right-click on _ADMIN, right-click on the new user and select properties.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053410](https://github.com/user-attachments/assets/b0c5654d-f0f4-40ca-9710-87ccb1286828)

</p>
<p>
Go to the Member Of tab and click Add.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053444](https://github.com/user-attachments/assets/b1df0f37-da36-4e80-8b3c-9bff9bf3c307)

</p>
<p>
Enter "domains admins" as the abject names to select. Click on check names and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053506](https://github.com/user-attachments/assets/b9ef6b39-2117-4071-ac80-eb877906546b)

</p>
<p>
Select Apply.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053512](https://github.com/user-attachments/assets/aaa6ab27-fdd7-45ef-9ae0-c2ebf475d8af)

</p>
<p>
Click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 053647](https://github.com/user-attachments/assets/52581747-42a9-4d43-8905-14b4c3c0029e)

</p>
<p>
Sign out.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054132](https://github.com/user-attachments/assets/8d25e715-d6cb-446a-a393-1c091c411c53)

</p>
<p>
Go back to Azure and under virtual machines copy the client-1 public IP address and paste it in Remote Desktop and click connect.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054314](https://github.com/user-attachments/assets/206486ac-5a47-4816-9cd1-032de3376584)

</p>
<p>
Right-click on the start menu and select system.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054350](https://github.com/user-attachments/assets/e1a1ea12-6667-4efd-9a68-616ede987ae0)

</p>
<p>
Click on Rename this PC (advanced).
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054410](https://github.com/user-attachments/assets/65ba926a-53d8-4c2e-b425-e7f22dd957c3)

</p>
<p>
Under the computer name tab click on change.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054457](https://github.com/user-attachments/assets/963d5a2f-1f6c-4fa1-baa7-64d489abd819)

</p>
<p>
Select Domain, type mydomain.com and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054651](https://github.com/user-attachments/assets/b7d93a29-7d5f-49b8-bf64-c41e50bcfb76)

</p>
<p>
This windows security screen should pop up to login as the admin of the domain which is mydomain.com\jane_admin. Enter the password and select OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054706](https://github.com/user-attachments/assets/38a16659-cdaa-452e-870c-1a37d63e9827)

</p>
<p>
Successfully linked client-1 to the domain.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054715](https://github.com/user-attachments/assets/19d0ef67-a1dd-4b2a-957b-4429d663cf18)

</p>
<p>
Select OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054807](https://github.com/user-attachments/assets/a2316fcc-eafb-4b5b-a5ad-f28ded9090c5)

</p>
<p>
Select Restart Now.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 054938](https://github.com/user-attachments/assets/c483bafd-c701-4d5b-8f22-9c930eeb4dff)

</p>
<p>
To verify that client-1 is apart of the domain search Active Directory Users and Computers.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055019](https://github.com/user-attachments/assets/62cbbe27-c977-475a-b261-812332cdc2e1)

</p>
<p>
Under the mydomain.com ou select computers and client-1 should be present.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055117](https://github.com/user-attachments/assets/6fb4f65b-f1d7-489a-b0e1-f53d22d14a07)

</p>
<p>
Right-click on mydomain.com, hover over new, and select Organizational Unit.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055135](https://github.com/user-attachments/assets/dfa3fd6b-1627-4d8e-b068-a24ff25f745d)

</p>
<p>
Type _CLIENTS for the name and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055200](https://github.com/user-attachments/assets/c190cd9b-40be-4239-be43-4f7f7bee016e)

</p>
<p>
Go back to computers and drag client-1 to _CLIENTS ou.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055215](https://github.com/user-attachments/assets/26821f8f-b93a-48b8-8e9d-a7f07d5e6bc1)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055237](https://github.com/user-attachments/assets/271cc99a-52ac-4dd9-8895-d4554b445865)

</p>
<p>
Right-click on mydomain.com and click refresh.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055435](https://github.com/user-attachments/assets/04f85733-886a-40b8-a7f1-8f6e3953648c)

</p>
<p>
Back in Azure select both virtual machines, click on the three dots and select Stop.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 055442](https://github.com/user-attachments/assets/7d9d81a6-ef2f-4414-9963-60a29d3808f0)

</p>
<p>
To conclude this lab, select Yes.
</p>
<br />
