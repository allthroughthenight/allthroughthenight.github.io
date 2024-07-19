---
layout: post
title: "Unlocking Windows"
---

My partner recently started school again, so we worked together on getting them a new used laptop set up. It came with Windows 10 Professional installed. Then they didn't touch it for a few months, so while catching up on all the updates they decided to upgrade to Windows 11. Everything updated fine and they used their laptop for the rest of the day knowing it was set up for the start of classes the following day.

Then comes the first day of class and they can't log in. We try an external keyboard, checking the caps lock and numpad, and any other related hardward or software issues. Once we exhausted everything we knew, we looked online and found we weren't the only one with password issues when upgrading from Windows 10 to Windows 11. My initial hunch was that their old password for Windows 10 didn't meet Windows 11 new password complexity. Talking with them more, their Windows 10 password used the pin feature, which wasn't supported by Windows 11.

Once we knew we couldn't just brute force our way in, I decided to see what I could do with an Ubuntu live boot stick. A few posts and articles mentioned the theory behind registry editing, but [this one](https://ostechnix.com/reset-windows-password-with-linux-live-cd/) specifically gave me the details I needed.

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

Shut down the live boot disk, then boot back into windows normally, and the specified user shouldn't have a password anymore. Overall it's not very hard, everything related to the live boot disk was the hardest. Downloading the ios, flashing the drive, booting into it. After that everything is smooth sailing.