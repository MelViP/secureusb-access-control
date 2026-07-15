<p align="center">
  <img src="docs/assets/flowers.gif" width="220">
</p>

<h1 align="center">🌸 SecureUSB Access Control 🌸</h1>

<p align="center">
Certificate-Based USB Protection using Python, Ubuntu, OpenSSL & Windows WMI
</p>

<p align="center">
<i>"Security is strongest when it quietly protects what matters most."</i>
</p>

## ✨ Why I Built This

During my time at **BDS Asesores Jurídicos**, I participated in security initiatives focused on protecting sensitive legal information and strengthening internal security practices.

One of the challenges involved safeguarding digital evidence stored on USB devices against unauthorized modifications while supporting compliance initiatives aligned with **Littler Global security standards**.

Because the original solution belongs to my former employer, this repository is a **complete recreation built from scratch**, using my own implementation and documentation to demonstrate the same technical concepts without exposing confidential information.

I enjoy building solutions that combine security, automation, and practical problem-solving, and this project represents exactly that.

---

## 🔐 Problem

Sensitive files transported using USB devices can easily be modified when connected to unauthorized computers.

For organizations handling legal evidence or confidential information, preserving file integrity is essential.

---

## 💡 Solution

This project implements certificate-based authorization using an internal Certificate Authority (CA).

When a USB device is connected:

- ✔ Verify the client certificate.
- ✔ Allow **Read/Write** access for trusted computers.
- ✔ Automatically switch to **Read-Only** mode on unauthorized devices.
- ✔ Preserve the integrity of sensitive files.

---

## 🚀 Features

- Certificate-Based Authentication
- Public Key Infrastructure (PKI)
- Internal Certificate Authority (OpenSSL)
- Windows Certificate Validation (WMI)
- Python Automation
- Dynamic USB Permission Enforcement
- Read-Only Protection
- Security-Oriented Architecture

---

## 🛠 Technologies

- Python
- Ubuntu Server
- OpenSSL
- Windows WMI
- X.509 Certificates
- NTFS Permissions
- Git

---

## 🌱 Future Improvements

- Certificate Revocation (CRL)
- Logging & Auditing
- GUI Application
- Docker Deployment
- Active Directory Integration
- Automatic Certificate Renewal

---

## 🤍 Disclaimer

This project is an original recreation inspired by a real-world enterprise security solution.

No proprietary source code, documentation, certificates, infrastructure details, or intellectual property from my former employer are included in this repository.
