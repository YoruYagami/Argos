# Argos
<p align="center">
  <img src="https://github.com/YoruYagami/Argos/assets/70035442/1b96abda-950c-4fec-8f8b-7c6c263bba66" width="500">
</p>

Argos is an Aggressor script for Cobalt Strike, designed to enhance its capabilities and make it easier to perform various tasks. It provides a set of functions to interact with antivirus, firewall, and perform enumeration tasks using PowerView and Bloodhound and execute lateral movement / priv esc technique via mimikatz and PwerUp .

### Usage
The Argos script adds a new submenu to the Cobalt Strike beacon context menu. Each function is represented as an item in the menu, allowing you to easily execute the function with a single click.

<p align="center">
<img width="513" alt="image" src="https://github.com/YoruYagami/Argos/assets/70035442/01caa219-6ae9-45a1-a87d-b1d06a24ff9f">
</p>

### Disclaimer
This script is intended for legitimate security testing purposes only. Please use responsibly and ensure that you have proper authorization before using it in a live environment.

### Menù structure
```
├─ Antivirus
│   ├─ Disable Windows Defender
│   └─ Disable Windows Defender IOAV
├─ Firewall
│   ├─ Disable Firewall
│   ├─ Show Firewall Status
│   └─ Show Firewall Configuration
└─ PowerView
    ├─ Import PowerView
    ├─ Local Admin Enumeration
    │   ├─ Enumerate all local admins
    │   └─ List local admins account names
    ├─ User Enumeration
    │   ├─ Dump all users and information
    │   ├─ List usernames (CN, SamAccountName, expanded SamAccountName)
    │   ├─ List user descriptions
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
    │   └─ List computers with unconstrained delegation
    ├─ Share Enumeration
    │   ├─ Invoke Module ShareFinder
    │   ├─ Enumerate Domain Shares
    │   ├─ Enumerate Shares that current User has Access
    │   └─ Enumerate Files that include *passwords*
    ├─ File Enumeration
    │   ├─ Invoke Module FileFinder
    │   └─ List full names of found files
    ├─ GPO Enumeration
    │   ├─ Enumerate GPOs
    │   ├─ List the names of the policies
    │   ├─ List all policies with details
    │   └─ List all Organization Units
    ├─ Bloodhound
    │   ├─ Upload BloodHound
    │   └─ Execute Collection Method All
    ├─ PowerUp
    │   ├─ Import PowerUp
    │   ├─ Invoke-AllChecks
    │   ├─ Enumerate Service Vulnerabilities
    │   │   ├─ Get-ModifiableService
    │   │   ├─ Get-ModifiableServiceFile
    │   │   └─ Get-ServiceUnquoted
    │   └─ RegistryCheck
    │       ├─ Get-RegistryAlwaysInstallElevated
    │       ├─ Get-RegistryAutoLogon
    │       └─ Get-ModifiableRegistryAutoRun
    └─ Mimikatz
        ├─ Privilege Debug
        ├─ Token
        │   ├─ Token::elevate
        │   └─ Token::revert
        ├─ sekurlsa
        │   ├─ sekurlsa::logonpasswords
        │   ├─ sekurlsa::logonPasswords full
        │   └─ sekurlsa::tickets /export
        ├─ crypto
        │   ├─ crypto::capi
        │   ├─ crypto::cng
        │   ├─ crypto::certificates /export
        │   ├─ crypto::certificates /export /systemstore:CERT_SYSTEM_STORE_LOCAL_MACHINE
        │   ├─ crypto::keys /export
        │   └─ crypto::keys /machine /export
        ├─ vault
        │   ├─ vault::cred
        │   └─ vault::list
        ├─ lsa
        │   ├─ lsadump::sam
        │   ├─ lsadump::secrets
        │   └─ lsadump::cache
        ├─ ekeys
        │   └─ sekurlsa::ekeys
        ├─ dpapi
        │   └─ sekurlsa::dpapi
        ├─ minidump
        │   └─ sekurlsa::minidump lsass.dmp
        └─ tgt
            └─ kerberos::tgt
```

### License
Argos is released under the MIT License. See the LICENSE file for more details.
