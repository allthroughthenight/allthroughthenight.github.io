---
layout: post
title: "Unlocking Windows"
---

My partner started school again and got a new laptop. While going through all the updates after not using it for a few months, they also upgraded from Windows 10 to Windows 11. After that everything went fine and they used their laptop for the rest of the day.

When they went to use their laptop on first day of class and they couldn't log in. We tried an external keyboard, checked the caps lock and numpad, along with a bunch of other issues and exhausted everything we knew. Looking online we found others having password issues when upgrading from Windows 10 to Windows 11. My initial hunch was that their old password for Windows 10 didn't meet Windows 11 new password complexity. Talking with them more, they used Windows 10's pin feature to log in, which wasn't supported by Windows 11.

I went to see what I could do with an Ubuntu live boot stick. A few posts and articles mentioned the theory behind registry editing, but [this one](https://ostechnix.com/reset-windows-password-with-linux-live-cd/) specifically gave me the details I needed.

In short, take an Ubuntu live boot disk, and execute the following

Install the tools
```
sudo apt install chntpw
sudo dnf install chntpw
```

Find the disk. It should be the largetst NTFS disk.
```
sudo sfdisk -l
```

Mount the disk
```
mkdir ~/winmount
sudo mount /dev/sda2 ~/winmount
```

Remove the user password. The tool is straight forwrad, just make sure to write the changes.
```
cd ~/winmount/Windows/System32/config/
sudo chntpw -i SAM
```

Shut down the live boot disk, then boot back into Windows normally, and the user shouldn't have a password anymore. It wasn't hard, everything related to the live boot disk was the hardest. Downloading the ISO, flashing the drive, booting into it. Executing the steps needed was the easy part.