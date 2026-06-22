# Logging in to Hyak Klone

**If you are completely new to Hyak or Open OnDemand (OOD)**, there are two things you must do first:
1. Log in to Hyak Klone at least once so your **home directory is created**;
2. Become aware of [**Hyak storage locations and quotas**](https://hyak.uw.edu/docs/storage/data) so you do not accidentally fill your home directory.

## UW VPN (Required for Off-Campus OOD Access)

If you are connecting from off campus, you must connect to the UW VPN before accessing Open OnDemand services on Hyak, including JupyterLab, follow these steps:

[**<ins>Husky OnNet instructions</ins>**](https://itconnect.uw.edu/tools-services-support/networks-connectivity/husky-onnet/installing-configuring-and-using-husky-onnet/)

> 📝 **Note:** These instructions are different for Windows and MacOS. Follow the instructions that correspond to your operating system. 

If you encounter issues connecting to the VPN, send an email to **<ins>help@uw.edu</ins>**. 

## First Login to Hyak Klone (Required Once)

Helpful resources:

- [**Hyak Klone Login Video**](https://youtu.be/gbse1xqezqk)
- [**Detailed Login Instructions**](https://github.com/UWrc/linux-fundamentals/blob/main/01-logging-in.md)
- [**SSH Client Overview**](https://github.com/UWrc/linux-fundamentals/blob/main/00-prereqs.md)

To initialize your account and create your home directory, log in to Klone once using SSH:

```bash
ssh UWNetID@klone.hyak.uw.edu
```

A successful login will display a welcome banner. Once you see this, your **home directory has been created**.

> 📝 **NOTE:** Too many failed login attempts may result in a temporary IP ban (one hour).

## Storage Overview

After logging in, you will land in your home directory:

```bash
[UWNetID@klone-login01 ~]$
```

### Home Directory

Your home directory:

- Is intended for configuration files and small scripts
- Has a strict **10 GB storage quota**
- Should ***not*** be used for large datasets or software installations

Resource: [**Hyak Home Directories Video**](https://youtu.be/OhLwqAZIBOo)

### Scrubbed Storage — Our Tutorial Workspace

For this workshop, you will work in:

```bash
/gscratch/scrubbed/$USER
```

This location is designed for active computation and provides substantially more space. 

> 📝 **NOTE:** Scrubbed storage is temporary scratch space for active computation. Files are **not backed up** and are automatically deleted after **21 days of inactivity**.

Create your personal folder there and navigate to it:

```bash
mkdir /gscratch/scrubbed/$USER
cd /gscratch/scrubbed/$USER
```

> 📝 **NOTE:** The `$USER` variable automatically expands to your username.

Next, clone the git repository for this tutorial into your personal folder:

```bash
git clone https://github.com/UWrc/data-science-REU-2026.git
```

## Configure Open OnDemand Access to Scratch Storage

Jupyter launched through Open OnDemand starts in your **home directory** by default.

To make it easy to access high-capacity storage from within Jupter, we create a **symbolic link** in your home directory that points to your scratch workspace.

### Create a Symbolic Link to Scratch Storage

```bash 
ln -s /gscratch/scrubbed/$USER ~/scratch
```

This creates a directory called `scratch` in your home directory that points to your workspace for this tutorial.

Now, when you launch Jupyter through Open OnDemand, you can easily navigate to `~/scratch` and work directly in your scratch storage.

> 📝 **Important notes about symbolic links:**
> 
> - A symbolic link is not a copy of the directory — it is a pointer
> - Deleting the link **does not delete the target directory** or its contents
> - You can safely remove the link later with:
> ```bash 
> rm ~/scratch
> ```
> Your data in `/gscratch/scrubbed/$USER` will remain intact.

These setup steps ensure that interactive applications launched through Open OnDemand can access appropriate storage locations without risking home directory quota issues.