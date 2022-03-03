# WSL Installation Guide

Windows Subsystem For Linux is a tool which will allow you to run Linux natively of Windows. It allows you to install a Linux distribution as an app and gives you access to important bash commands such as `git`!

These installation steps can all be found in the [WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/install).

## Installation Steps

![Image of PowerShell installing WSL](/WSL/images/ps_admin.PNG 'Installing WSL using the PowerShell terminal')

To install WSL on Windows the first thing you will need to run Powershell as an administrator and enter the following code `wsl --install` and restart your machine.

![Image of Ubuntu terminal on restart](/WSL/images/ubuntu_install.PNG 'Continuing the installation after restarting your machine')

After restarting your machine you should have an **Ubuntu** terminal pop up (if this doesn't happen you can open it from the start menu) that continues the installation after restart.

If all goes well you should be prompted to create a username and password (this doesn't have to be your Windows login information). This will become the default user with administrator privileges (allowing you to run `sudo` commands!)

And that's it, you're ready to go. Please continue to the next step which is [setting up your dev environment](/WSL/setup/setup.md)!

---

## Common Issues

Unfortunately things don't always go to plan and you may instead get an error message with a code such as `0x80070003`. Included below are a list of errors we commonly see and instructions on how to fix them. If you get an error not listed here please use the troubleshooting guidelines found [here](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues) or post in the **precourse** channel on Slack.

| Error Code | Description                                                                   | Link                                                                                                                                                                         |
| ---------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0x800701bc | You need to download the WSL2 Ubuntu kernel update                            | [Help](https://docs.microsoft.com/en-gb/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)                                                      |
| 0x80370102 | This error occurs when you do not have virtualisation enabled on your machine | [Help](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed) |
| 0x80070003 | Similar to the issue above but night need to go into your computers BIOS      | [Help](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues)                                                                                   |
