<p align="center">
<img <img width="410" alt="Screenshot 2025-01-31 at 19 31 03" src="https://github.com/user-attachments/assets/6f24d05b-f928-41e6-8d5b-0a98eacb3a90" />


<h1>
Network File Shares and Permissions </h1>
This tutorial explains how Network File Shares and Permissions function, and how they interact with both users and administrators



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Created sample file shares with various permissions
- Attempt to access file shares as a normal user
- Create an Accountants security group, assign permissions, an test access


<h2>Installation Steps</h2>

<p>
<img <img width="555" alt="Screenshot 2025-01-31 at 20 01 36" src="https://github.com/user-attachments/assets/2dd7e5ab-740e-438a-ad7e-7e037beb3686" />

<p>
I logged into DC-1 using my domain admin account and accessed my Client-1 account as a standard user. I created four folders: 'read-access', 'write-access', 'no-access', and 'accounting' on my domain account, then configured different permissions for each folder.
</p>
<br />

<p>
<img <img width="273" alt="Screenshot 2025-01-31 at 20 03 34" src="https://github.com/user-attachments/assets/53cb9cd8-23e8-4c2b-a91f-e69423eda47f" />

<p>
I attempted to access file shares as a standard user. On my Client-1 account, I navigated to the shared folder (Start>Run>\DC-1) and tested each folder to determine which ones I could access, where I could create files, and if the permissions were correctly configured.</p>
<br />

<p>
<img <img width="278" alt="Screenshot 2025-01-31 at 20 10 45" src="https://github.com/user-attachments/assets/9740e796-13fb-4a8e-85ad-bfb06cf2be64" />

<p>
On DC-1, I created an "Acccountants" security group through Active Directory, assigned the appropriate permissions, and tested access. I configured the 'Accounting' folder as a user who should not have access, and the attempt failed. I then logged out of Client-1 and added the user to the 'Accountants' security group on DC-1. After signing back into Client-1, I tested access to the 'Accounting' share to verify that the permissions were applied correctly.
<br />
