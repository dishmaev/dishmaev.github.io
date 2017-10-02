## Welcome to my site

All of my open source software packages contained in the repositories for the corresponding operating systems. To work with repositories need a few keys.

### Linux GPG key details

* Download: [https://dishmaev.github.io/repos/linux/linux_signing_key.pub](https://dishmaev.github.io/repos/linux/linux_signing_key.pub)
* Fingerprint: 5076 50DE 33C7 BA92 EDD1  569D F4F5 A67B E44E EED4

### Linux APT-based system (Debian, Ubuntu, etc.)

#### Command line key download and installation

`wget -O - https://dishmaev.github.io/repos/linux/linux_signing_key.pub | sudo apt-key add -`

You can verify the key installation by running:

`apt-key list`

It should be in the output list.


#### Command line add repository

Official packages list repository is `stable`, enabled by default. Other lists are intended for testing and development, the `testing` and `unstable`, respectively.

`sudo wget -P /etc/apt/sources.list.d/ https://dishmaev.github.io/public-apt-dishmaev.list`

### Linux RPM-based system (Oracle Linux, Fedora , etc.)

#### Command line add repository

Official packages list repository is `release`, enabled by default. Other lists are intended for testing and development, the `test` and `develop`, respectively.

`sudo yum-config-manager --add-repo https://dishmaev.github.io/public-yum-dishmaev.repo`

Specified key is automatically loaded when you make first request (update, install, etc.) to a repository. After it you can verify the key installation by running:

`rpm -qi gpg-pubkey-e44eeed4-*`

Details of the key must be in the output.
