# Homebrew

Package managers make it so much easier to install and update applications (for Operating Systems) or libraries (for programming languages). The most popular one for OS X is [Homebrew](http://brew.sh/).

### Install

An important dependency before Homebrew can work is the **Command Line Tools** for **Xcode**. These include compilers that will allow you to build things from source.


We can install Homebrew! In the terminal paste the following line (without the `$`), hit **Enter**, and follow the steps on the screen:

    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

One thing we need to do is tell the system to use programs installed by Hombrew (in `/usr/local/bin`) rather than the OS default if it exists. We do this by adding `/usr/local/bin` to your `$PATH` environment variable:

    $ echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile

Alternatively, we can also insert `/usr/local/bin` to the first line of `/private/etc/paths` and reboot the Mac to change global paths loading order. Admin password may be required if you modify the file.

Open an new terminal tab with **Cmd+T** (you should also close the old one), then run the following command to make sure everything works:

    $ brew doctor

Even on OSX you should not be working with an admin account. Here are the steps to make homebrew usable for non admin users.:

#### Assumptions

I assume brew has already been installed by an administrator and it's login is admin. Change admin below to the name of your admin account.

#### Steps

Under System Preferences create a new group "brew" and add your user to it. Then open the terminal and :

```
$ su - admin
$ sudo chgrp -R brew /usr/local
$ sudo chgrp -R brew /Library/Caches/Homebrew
$ sudo chmod -R g+w /usr/local
$ sudo chmod -R g+w /Library/Caches/Homebrew
```
And if you plan to use caskroom too :
```
sudo mkdir -p /opt/homebrew-cask/Caskroom
sudo chgrp -R brew /opt/homebrew-cask
sudo chmod -R g+w /opt/homebrew-cask
```

(this logs in as the admin user and allows the members of the *"brew"* group to write to /usr/local and the Caches directory).

With your user account you can now run brew doctor to check if everything is working as it should.

Credits: Visit [this page](http://blog.strug.de/2012/06/my-homebrew-multi-user-setup/) for some more detailed instructions.
