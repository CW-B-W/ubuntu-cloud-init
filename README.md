# Ubuntu Cloud-Init: Ready-to-Use Seed ISO

This project provides a pre-generated `my-seed.iso` designed to solve the common issue of being unable to login to a newly imported Ubuntu VM from an `.ova` file.

## Purpose

By default, when you create an Ubuntu VM by importing an `.ova` file, it often lacks default credentials, making it impossible to log in. 

This repository provides a ready-to-use `my-seed.iso` (generated from `my-cloud-config.yaml`) that configures a default user upon first boot.

**You do NOT need to modify any files or use `cloud-init` commands to build your own ISO. Simply use the provided `my-seed.iso`.**

## Default Credentials

Once the ISO is mounted and the VM is started, you can login with:

*   **Username:** `ubuntu`
*   **Password:** `ubuntu`

## How to Use

1.  Import your Ubuntu `.ova` file into your virtualization software (e.g., VirtualBox, VMware).
2.  In the VM settings, go to the **Storage** or **Optical Drive** section.
3.  Mount the provided `my-seed.iso` as a CD/DVD drive.
4.  Start the VM.
5.  Login using the default credentials above.

---
*Note: This configuration enables password-based SSH login (`ssh_pwauth: True`) for convenience in development environments.*
