# Active-Directory-Home-Lab-Windows-Server-2022-
(Self-Built Virtualized Windows Server Lab Project) I started this project to simulate a real-world IT infrastructure for training and learning. Upon commiting to this project I was able to demonstrate skills such as Active Directory, DNS, Group Policy, network file sharing, and domain management. 

## What this Project Covers

- Deployed a virtualized **Windows Server 2022** and **Windows 10/11** client using VirtualBox.
- Configured a functional **Active Directory Domain (lab.local)** with DNS and DHCP.
- Created and organized **Organizational Units (OUs)** for departments: Sales, HR, and IT.
- Managed **user accounts** and **group memberships** using best practices.
- Set up **shared folders with proper NTFS and share-level permissions** for role-based access control.
- Implemented **network troubleshooting and security hardening** (firewall, permissions).
- Tested and validated access control using domain-joined users and network commands.

## Technologies & Tools Used

- **Operating Systems:** Windows Server 2022, Windows 10
- **Virtualization:** VirtualBox
- **Directory Services:** Active Directory (AD DS)
- **Networking:** DNS, DHCP, SMB, TCP/IP
- **Scripting & CLI:** CMD, PowerShell (`net use`, `ipconfig`, `ping`, etc.)

- ## Lab Structure

lab.local
- OU: Sales
- - Users: sales01, sales02
- OU: HR
- -Users: hr01
-OU: IT
- -Users: itadmin

## Shared Folders

| Share Name     | Path                        | Group Access   |
|----------------|-----------------------------|----------------|
| Sales_Share    | C:\Shared\Sales_Share       | SalesUsers     |
| HR_Share       | C:\Shared\HR_Share          | HRUsers        |
| IT_Share       | C:\Shared\IT_Share          | ITUsers        |

- NTFS and Share permissions configured to allow **only group members** to access their folder.
- Unauthorized users receive **“Access Denied”** when attempting access.

## Commands Used

- `net share` — List shared folders on server
- `net use` — Map or access network drives
- `ping`, `ipconfig`  — Network diagnostics
- `netstat -an | find ":445"` — Check SMB port availability
- `whoami` = Comfirm if User is connected to (Lab.local) domain

## Screenshots

- View the [`/screenshots`] folder for key configuration screenshots:
- Active Directory Users and Computers (ADUC)
- Folder sharing & permissions
- Client joined to domain
- Network troubleshooting tests

## Lessons Learned

- The importance of proper **NTFS vs Share permissions**.
- How **DNS and network settings** directly affect domain functionality.
- Troubleshooting "network path not found" and "access denied" errors.
- The structure and management of a Windows domain in a real-world IT context.

## Future Improvements

- Automate user creation and folder mapping with PowerShell
- Implement Group Policy for drive mapping
- Add WSUS or print server for more enterprise scenarios


## Why This Project?

This home lab was built as part of my transition into IT. It demonstrates real technical problem-solving, core Windows Server skills, and foundational network administration knowledge.
  
