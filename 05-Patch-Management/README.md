# Patch Management Configuration & Validation

## Overview

Configured and validated **patch management** across a Windows Server 2022 domain controller and Windows 11 Pro client using **Action1** to remotely identify and deploy Windows updates.

The project demonstrates basic endpoint management, update deployment, and verification of patch status across multiple systems in a simulated IT support environment.

## Environment

* **Hypervisor:** Oracle VirtualBox
* **Operating Systems:** Windows Server 2022 and Windows 11 Pro
* **Patch Management:** Action1
* **Network:** Windows Server 2022 Domain Controller

## Configuration

### Action1 Agent

Installed and configured the **Action1 agent** on the Windows Server 2022 and Windows 11 Pro systems to allow centralized endpoint management and patch deployment.

### Windows Update Deployment

Used Action1 to identify available Windows updates and deploy patches to both the Windows Server 2022 and Windows 11 Pro systems.

### Patch Verification

Verified that the selected updates were successfully installed and confirmed the patch status of both systems in Action1.

## Validation

* Confirmed the Windows Server 2022 and Windows 11 Pro systems were registered in Action1.
* Identified available Windows updates.
* Deployed Windows patches through Action1.
* Verified successful patch installation.
* Confirmed both endpoints reported updated patch status.

### Endpoint Registration

![Endpoint Registration](./screenshots/endpoint-registration.png)

### Available Updates

![Available Updates](./screenshots/available-updates.png)

### Patch Deployment

![Patch Deployment](./screenshot/patch-deployment.png)

### Patch Verification

![Patch Verification](./screenshots/patch-verification.png)
