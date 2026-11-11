# Microsoft Intune Enterprise Device Management Lab

## Overview

This project demonstrates the deployment and management of Windows devices using Microsoft Intune in a simulated enterprise environment. The lab focuses on enterprise endpoint management, security policy enforcement, application deployment, and device compliance using Microsoft cloud technologies.

---

## Technologies Used

- Microsoft Intune
- Microsoft Entra ID
- Windows 11
- Microsoft Defender for Endpoint
- Security Baselines
- Configuration Profiles
- Compliance Policies

---

## Project Objectives

- Enroll Windows devices into Intune
- Configure compliance policies
- Deploy applications
- Create configuration profiles
- Implement security baselines
- Configure Microsoft Defender security settings

---

## Key Skills Demonstrated

- Endpoint Management
- Identity and Access Management (IAM)
- Device Compliance
- Application Deployment
- Security Hardening
- Policy Configuration
- Microsoft Intune Administration
- Microsoft Entra ID Integration
- Enterprise Device Security

---

# Project Phases

## Phase 1: Environment Setup

Configured the Microsoft Intune environment and established Microsoft Entra ID prerequisites for device management.

### Tasks Completed

- Created test users
- Configured security groups
- Verified Microsoft Intune licensing
- Prepared Windows 11 test devices

**Screenshots:**

![Environment Setup](screenshots/environment-setup.png)

---

## Phase 2: Device Enrollment

Successfully enrolled Windows 11 devices into Microsoft Intune using Microsoft Entra ID.

### Tasks Completed

- Joined device to Microsoft Entra ID
- Verified enrollment status
- Confirmed device synchronization
- Reviewed device inventory

**Screenshots:**

![Device Enrollment](screenshots/device-enrollment.png)

---

## Phase 3: Compliance Policies

Implemented compliance policies to ensure devices meet organizational security requirements.

### Tasks Completed

- Required BitLocker encryption
- Required Microsoft Defender protection
- Configured password requirements
- Assigned policies to security groups

**Screenshots:**

![Compliance Policy](screenshots/compliance-policy.png)

---

## Phase 4: Configuration Profiles

Created configuration profiles to standardize endpoint settings across managed devices.

### Tasks Completed

- Configured password requirements
- Set lock screen timeout
- Disabled guest accounts
- Applied security settings

**Screenshots:**

![Configuration Profiles](screenshots/configuration-profiles.png)

---

## Phase 5: Application Deployment

Deployed enterprise applications using Microsoft Intune.

### Applications Deployed

- Google Chrome
- Notepad++
- 7-Zip

### Tasks Completed

- Created app deployment assignments
- Tested installation success
- Verified device deployment status

**Screenshots:**

![Application Deployment](screenshots/app-deployment.png)

---

## Phase 6: Security Baselines

Implemented Microsoft security baselines and endpoint protection configurations.

### Tasks Completed

- Deployed Windows Security Baseline
- Configured Firewall policies
- Implemented Attack Surface Reduction (ASR) rules
- Enabled Microsoft Defender protection settings

**Screenshots:**

![Security Baseline](screenshots/security-baseline.png)

---

## Architecture Diagram

```text
Windows 11 Device
        │
        ▼
Microsoft Entra ID
        │
        ▼
Microsoft Intune
        │
 ┌──────┼───────┐
 ▼      ▼       ▼
Policies Apps Security
```

---

## Challenges and Lessons Learned

Throughout this project, several real-world administrative challenges were encountered and resolved:

- Troubleshooting security group assignment issues
- Understanding device-based versus user-based assignments
- Managing compliance reporting delays
- Resolving Microsoft Store application discovery limitations
- Troubleshooting enrollment synchronization and policy application
- Learning proper deployment targeting for applications and security policies

These challenges provided hands-on experience with enterprise troubleshooting and Microsoft Intune administration.

---

## Results

Successfully deployed and managed Windows endpoints using Microsoft Intune enterprise administration practices.

### Outcomes

✅ Device enrollment and management

✅ Compliance policy enforcement

✅ Application deployment

✅ Security baseline implementation

✅ Microsoft Defender configuration

✅ Endpoint security hardening

✅ Configuration profile deployment

---

## Screenshots

### Entra ID Device

![Entra Device](screenshots/entra-device.png)

### Compliance Status

![Compliance Status](screenshots/compliance-status.png)

### Configuration Profile

![Configuration Profile](screenshots/config-profile.png)

### Application Deployment

![App Deployment](screenshots/app-deployment.png)

### Security Baseline

![Security Baseline](screenshots/security-baseline.png)

### Microsoft Defender Configuration

![Defender Configuration](screenshots/defender-config.png)

---

## Documentation

### Project Files

- [Intune_Project_Guide.docx](Intune_Project_Guide.docx)
- [Intune_Project_Guide.pdf](Intune_Project_Guide.pdf)

---

## Author

**Tayo**

- B.S. Cybersecurity, UTSA
- CompTIA Security+
- Aspiring Cloud / Security Engineer
- Hands-on experience with Microsoft Intune, Microsoft Entra ID, Active Directory, and Enterprise Endpoint Management
