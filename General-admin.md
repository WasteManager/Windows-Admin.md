# Check to see if a port is open on a machine
  - admin powershell
  - Test-NetConnection -ComputerName computer1 -Port desiredport

## Windows Administration & PowerShell Commands Cheat Sheet

###  System Information
| Command | Description |
|---------|-------------|
| `systeminfo` | View system configuration and details |
| `hostname` | Display system hostname |
| `Get-ComputerInfo` | PowerShell: Detailed system info |
| `Get-CimInstance -ClassName Win32_OperatingSystem` | OS details |
| `Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion'` | Registry-based OS info |

---

###  PowerShell Basics
| Command | Description |
|---------|-------------|
| `Get-Command` | List all commands |
| `Get-Help <cmd>` | Get help on command |
| `Get-Process` | List running processes |
| `Stop-Process -Name notepad` | Stop a process |
| `Start-Process notepad` | Start a process |
| `Get-Service` | List all services |
| `Restart-Service -Name spooler` | Restart a service |

---

###  User & Group Management
| Command | Description |
|---------|-------------|
| `net user` | List local users |
| `net user <username> <password> /add` | Add user |
| `net localgroup` | List local groups |
| `net localgroup Administrators <user> /add` | Add user to group |
| `Get-LocalUser` | PowerShell: List local users |
| `New-LocalUser -Name "user" -Password (ConvertTo-SecureString "pass" -AsPlainText -Force)` | Create local user |

---

###  Permissions & Security
| Command | Description |
|---------|-------------|
| `icacls <file>` | View/change file permissions |
| `secpol.msc` | Open local security policy GUI |
| `gpedit.msc` | Open Group Policy Editor |
| `Get-Acl <path>` | PowerShell: Get permissions |
| `Set-Acl <path> <acl>` | Set permissions |

---

###  File & Directory Management
| Command | Description |
|---------|-------------|
| `dir` | List files in a directory |
| `cd` | Change directory |
| `copy`, `xcopy`, `robocopy` | File copy tools |
| `del`, `erase`, `Remove-Item` | Delete files |
| `mkdir`, `New-Item -ItemType Directory` | Create directories |
| `Get-ChildItem` | PowerShell equivalent of `ls` |

---

###  Services & Processes
| Command | Description |
|---------|-------------|
| `services.msc` | Open Services GUI |
| `taskmgr` | Open Task Manager |
| `tasklist` | List running tasks |
| `taskkill /IM notepad.exe /F` | Kill a task |
| `Get-Service` | List services in PowerShell |
| `Start-Service`, `Stop-Service`, `Restart-Service` | Control services |

---

###  Networking
| Command | Description |
|---------|-------------|
| `ipconfig /all` | Show network config |
| `ping <host>` | Test connectivity |
| `tracert <host>` | Trace route |
| `netstat -an` | View open ports |
| `Get-NetIPAddress` | PowerShell: Show IPs |
| `Test-NetConnection <host>` | PS: Ping + port test |
| `New-NetFirewallRule` | Create firewall rule |

---

###  System Monitoring & Logs
| Command | Description |
|---------|-------------|
| `eventvwr.msc` | Open Event Viewer |
| `Get-EventLog -LogName System -Newest 50` | Last 50 system log entries |
| `perfmon` | Performance monitor |
| `resmon` | Resource monitor GUI |
| `chkdsk` | Check disk integrity |
| `sfc /scannow` | Scan system files |

---

###  Pro Tips
- Use `Ctrl + Shift + Enter` to run PowerShell or CMD as admin
- Tab-complete in PowerShell for fast typing
- Use `Out-File` or `>` to export command output: `Get-Process > procs.txt`
- Use PowerShell Remoting: `Enter-PSSession -ComputerName <name>`
- Use `schtasks` to schedule tasks from command line

---

