Azure OwnCloud Deployment Project

📌 Project Overview



This project demonstrates the end-to-end deployment of OwnCloud on Microsoft Azure using a secure, scalable, and production-style architecture. The solution separates the application server and database server using public and private subnets, enforces security through Network Security Groups (NSGs), and enables controlled internet access using a NAT Gateway.



The project was executed as part of a cloud learning exercise to understand real-world Azure infrastructure design and application deployment.



🏗️ Architecture Components



Azure Virtual Network (VNet) with CIDR-based addressing



Public Subnet – Application Server (Apache + PHP + OwnCloud)



Private Subnet – Database Server (MySQL)



NAT Gateway – Secure outbound internet access for private subnet



Network Security Groups (NSGs) – Inbound and outbound traffic control



Two Azure Virtual Machines



Application Server VM



Database Server VM



⚙️ Implementation Steps

1️⃣ Infrastructure Setup



Created a Virtual Network with public and private subnets



Configured NSG rules for application and database tiers



Attached NAT Gateway to the private subnet



Deployed Application VM (public IP enabled)



Deployed Database VM (private IP only)



2️⃣ Database Server Configuration



Securely copied SSH key from application server to database server



Installed and configured MySQL



Created database and database user for OwnCloud



Restricted database access to private subnet only



3️⃣ Application Server Configuration



Installed Apache web server



Installed PHP 7.4 and required extensions



Deployed OwnCloud application



Configured Apache modules and permissions



Verified web application access via browser



🌐 Application Access



The application was successfully accessed using the browser:



http://<Application\_Server\_Public\_IP>/owncloud





Users were able to:



Log in to OwnCloud



Browse folders



Upload and view files



Access images and documents successfully



🧪 Challenges Faced \& Resolutions



SSH key authentication failures – Resolved by correcting key permissions and authorized\_keys configuration



MySQL root access issues – Fixed by proper service initialization and user creation



OwnCloud PHP compatibility error – Resolved by installing and enabling PHP 7.4



Incorrect download format – Identified HTML file download instead of archive and corrected URL



These issues provided strong hands-on troubleshooting experience.



🧹 Cleanup \& Cost Management



Application and database services were stopped safely



All Azure resources including:



Virtual Machines



Network Security Groups



Virtual Network



NAT Gateway



Public IP addresses



Managed Disks

were deleted by removing the Resource Group



Final verification ensured no running resources remained, preventing additional costs.



🎯 Key Learnings



Designed and deployed a secure multi-tier Azure architecture



Gained practical experience with Azure networking, VM management, Linux administration, and real-world troubleshooting



🛠️ Technologies Used



Microsoft Azure



Ubuntu Linux



Apache HTTP Server



PHP 7.4



MySQL



OwnCloud



SSH \& SCP



📁 Repository Contents



README.md – Project documentation



Screenshots – Step-by-step execution evidence













