# 🛡️ DISA-STIG-Remediation-Lab

This repository documents my hands-on work implementing Windows 11 STIG remediations in a lab environment using Tenable, Azure VMs, Local Security Policy, and PowerShell.

## 📌 Goals
- Identify failed STIG controls
- Remediate them manually and with PowerShell where possible
- Validate changes through rescanning
- Document lessons learned from hardening, including system access impacts

## Tools Used
- Tenable Vulnerability Management
- Azure Virtual Machines
- Local Security Policy
- PowerShell

---

## 🔍 STIG Remediations

---

### 1. SMBv1 Disabled
- **STIG ID:** WN11-00-000170  
- **Issue:** SMBv1 protocol enabled (insecure legacy protocol)  
- **Fix:** Disabled SMBv1 via Windows Features / PowerShell  
- **Validation:** Rescan confirmed improved compliance  

---

### 2. WinRM Basic Authentication Disabled
- **STIG ID:** WN11-CC-000345  
- **Issue:** WinRM allowed Basic authentication  
- **Fix:** Disabled Basic authentication in WinRM config  
- **Validation:** Rescan confirmed improved compliance  

---

### 3. UAC Enabled (Admin Approval Mode)
- **STIG ID:** WN11-SO-000270  
- **Issue:** UAC not enforced for administrators  
- **Fix:** Enabled Admin Approval Mode via Group Policy  
- **Validation:** Rescan confirmed improved compliance  

---

### 4. SMB Signing Required
- **STIG ID:** WN11-SO-000020  
- **Issue:** SMB signing not required  
- **Fix:** Enabled SMB signing via Group Policy  
- **Validation:** Rescan confirmed improved compliance  

---

### 5. Legal Notice Banner Configured
- **STIG ID:** WN11-SO-000075  
- **Issue:** No interactive logon banner configured  
- **Fix:** Configured logon warning message via Group Policy  
- **Validation:** Rescan confirmed improved compliance  

---

### 6. Printing Over HTTP Disabled
- **STIG ID:** WN11-CC-000110  
- **Issue:** Printing over HTTP allowed (insecure)  
- **Fix:** Disabled HTTP printing via Group Policy  
- **Validation:** Rescan confirmed improved compliance  

---

### 7. Microsoft Consumer Experiences Disabled
- **STIG ID:** WN11-CC-000197  
- **Issue:** Consumer features enabled (potential data exposure)  
- **Fix:** Disabled Microsoft consumer experiences  
- **Validation:** Rescan confirmed improved compliance  

---

### 8. Remote Desktop Secure RPC Required
- **STIG ID:** WN11-CC-000285  
- **Issue:** RDP did not require secure RPC communication  
- **Fix:** Enforced secure RPC for Remote Desktop  
- **Validation:** Rescan confirmed improved compliance  

---

### 9. Virtualization-Based Security Enabled
- **STIG ID:** WN11-CC-000070  
- **Issue:** Virtualization-based security not enabled  
- **Fix:** Enabled VBS with secure boot configuration  
- **Validation:** Rescan confirmed improved compliance  

---

### 10. Hardware Security Device Requirement (Windows Hello)
- **STIG ID:** WN11-CC-000255  
- **Issue:** Hardware-backed security not enforced  
- **Fix:** Enabled Windows Hello for Business / hardware security requirement  
- **Validation:** Rescan confirmed improved compliance  

---

## 📊 Results Summary
- Reduced failed STIG findings from 159 → 109  
- Improved overall system hardening posture  
- Applied multiple secure configuration controls aligned with DISA STIG guidelines

- <img width="1089" height="1444" alt="3b58ebb8-28e6-407a-905f-e8a905b75248" src="https://github.com/user-attachments/assets/cbab68d1-0f83-4543-8625-d65d4e63f4dd" />


---

## 🚀 Key Takeaways
- STIGs focus on **secure configuration**, not just vulnerabilities  
- Small misconfigurations can create major security risks  
- Validation through rescanning is critical  

---
