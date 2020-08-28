1. Open up a terminal and run:

`sudo dnf install ansible -y`

 Enter your password

2. Go to https://drive.google.com/drive/folders/1yLrwmD7ZpIPt9sgJk7IN-dWVYhehQukg?usp=sharing to download all the files, including those in the VPN folder. Ensure they are all downloaded into the Downloads folder, which is usually the default

3. Open up the Terminal and clone the remote repo

`git clone https://github.com/Levi-Le/auto.git`

4. Change into the `auto` directory you just cloned

`cd auto`

5. Start the ansible playbook

`ansible-playbook basic-setup.yml -K`

 Enter your `root` password as BECOME password.
 Note that the first TASK [upgrade all packages] takes a long time to complete depending on your Fedora version.



When PLAY is over:

1. Connect to VPN:

`nmcli connection up id "1 - Red Hat Global VPN" --ask`

Enter your Kerberos password and token in the form of `kerberospasswordtoken`

2. Kinit:

`kinit`

Enter your PIN
