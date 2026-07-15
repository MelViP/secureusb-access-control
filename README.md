<p align="center">
  <img src="docs/assets/flowers.gif" width="220">
</p>

<h1 align="center">🌸 SecureUSB Access Control 🌸</h1>

<p align="center">
Certificate-Based USB Access Control using Python, Ubuntu, OpenSSL, Microsoft Intune & Windows WMI
</p>


---

## 🖖🏼 Background

This repository is an original recreation of a real-world enterprise security solution I designed while working at **BDS Asesores Jurídicos**.

The original implementation was part of an internal security roadmap supporting compliance initiatives aligned with **Littler Global security standards**. Its objective was to protect sensitive legal evidence stored on USB devices from unauthorized modification before being delivered to judicial authorities.

Because the original solution is the intellectual property of my former employer, **all source code, documentation, and infrastructure contained in this repository have been recreated from scratch**. The focus is to demonstrate the architecture, engineering decisions, and security concepts behind the solution without exposing confidential information.

---

## 👉🏼 The Challenge

Sensitive information transported through removable media is vulnerable to unauthorized modification once connected to an untrusted computer.

For organizations handling confidential legal documentation, preserving file integrity is critical. This project demonstrates one possible approach using Public Key Infrastructure (PKI), endpoint authentication, and automated access control.

---

## ☝🏼 Solution Overview

The solution combines Linux-based PKI administration with automated endpoint validation on Windows.

### 🪴 Infrastructure

- Create an internal Root Certificate Authority (CA) on Ubuntu Server using OpenSSL.
- Generate and sign client certificates.
- Securely transfer certificates using SFTP.
- Deploy trusted certificates to Windows endpoints through Microsoft Intune.

### 🪴 Endpoint Validation

When a USB device is connected, the Python application:

- Reads the **Windows Personal Certificate Store (Current User → Personal / My)**.
- Validates the installed client certificate using WMI.
- Confirms the certificate was issued by the trusted internal CA.
- Grants **Read/Write** permissions to authorized devices.
- Automatically enforces **Read-Only** permissions on unauthorized systems.

---

## 🫶🏼 Features

- Certificate-Based Authentication
- Public Key Infrastructure (PKI)
- OpenSSL Root Certificate Authority
- Ubuntu Server Administration
- Secure Certificate Distribution (SFTP)
- Microsoft Intune Certificate Deployment
- Windows Personal Certificate Store Validation
- Windows Management Instrumentation (WMI)
- Python Security Automation
- Dynamic NTFS Permission Enforcement
- Read-Only Protection for Unauthorized Devices

---

## 💅🏼 Technologies

| Infrastructure | Endpoint | Development |
|---------------|----------|-------------|
| Ubuntu Server | Microsoft Intune | Python |
| OpenSSL | Windows Certificate Store | WMI |
| SFTP | NTFS Permissions | Git |
| X.509 PKI | Windows Security APIs | VS Code |

---

## ✍🏼 Architecture

```text
                     Ubuntu Server
                   (OpenSSL Root CA)
                           │
            Generate & Sign Client Certificates
                           │
                    Secure Transfer (SFTP)
                           │
                           ▼
               Windows Test Workstation
                           │
             Deploy via Microsoft Intune
                           │
                           ▼
      Windows Personal Certificate Store (My)
                           │
                           ▼
            Python + WMI Certificate Validation
                           │
          Validate Issuer & Certificate Presence
                           │
                ┌──────────┴──────────┐
                │                     │
        Trusted Workstation     Untrusted Workstation
             Read/Write               Read-Only
```

---

## ✌🏼 Repository Scope

This repository focuses on the components I personally engineered:

- Python endpoint automation
- Certificate validation logic
- USB permission enforcement
- Overall solution architecture
- Security documentation (AI helped me with this 🫰🏼)

The PKI infrastructure follows established OpenSSL best practices and official documentation rather than introducing a custom certificate authority implementation.

---

## 👍🏼 Future Improvements

- To be continued...

---

## 🤍 Disclaimer 🛼

This repository is an independent implementation inspired by a real enterprise security solution.

No proprietary source code, internal documentation, certificates, infrastructure configuration, or confidential information from **BDS Asesores Jurídicos** or **Littler Global** has been copied or included.

The implementation presented here was developed independently for educational and portfolio purposes while preserving the original engineering concepts.
