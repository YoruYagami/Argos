### Argos Aggressor Script

Argos is an Aggressor script for Cobalt Strike, designed to enhance its capabilities and make it easier to perform various tasks. It provides a set of functions to interact with antivirus, firewall, and perform enumeration tasks using PowerView.

### Usage
The Argos script adds a new submenu to the Cobalt Strike beacon context menu. Each function is represented as an item in the menu, allowing you to easily execute the function with a single click.

### Disclaimer
This script is intended for legitimate security testing purposes only. Please use responsibly and ensure that you have proper authorization before using it in a live environment.

### Menù structure
```
├─ Antivirus
│   ├─ Disable Windows Defender
│   ├─ Disable Windows Defender IOAV
│   └─ Get Windows Defender Status
├─ Firewall
│   ├─ Disable Firewall
│   ├─ Show Firewall Status
│   └─ Show Firewall Configuration
└─ PowerView
    ├─ Local Admin Enumeration
    │   ├─ Enumerate all local admins
    │   └─ List local admins account names
    ├─ User Enumeration
    │   ├─ Dump all users and information
    │   ├─ List usernames (CN, SamAccountName, expanded SamAccountName)
    │   ├─ List user descriptions
    │   ├─ Search descriptions for 'password' or 'admin'
    │   ├─ Show all user properties
    │   ├─ Show password last set date
    │   ├─ Show user login count
    │   ├─ Show bad password count
    │   └─ List all Users with RDP enabled
    ├─ Computer Enumeration
    │   ├─ List all workstations in the domain
    │   ├─ Get detailed information on all domain computers
    │   ├─ List DNS hostnames of domain computers
    │   ├─ List computer names and operating systems
    │   └─ List computers by operating system (Windows 7, Windows 10, Windows Server 2016, Windows Server 2019)
    │   └─ List computers with unconstrained delegation
    ├─ Share Enumeration
    │   ├─ Invoke Module ShareFinder
    │   ├─ Enumerate Domain Shares
    │   ├─ Enumerate Shares that current User has Access
    │   └─ Enumerate Files that include *passwords*
    ├─ File Enumeration
    │   ├─ Invoke Module FileFinder
    │   └─ List full names of found files
    └─ GPO Enumeration
        ├─ Enumerate GPOs (Verbose)
        ├─ List the names of the policies
        ├─ List all policies with details
        └─ List all Organization Units
```
### License
Argos is released under the MIT License. See the LICENSE file for more details.
