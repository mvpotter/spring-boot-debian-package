# Spring boot debian package

An example project that shows how can Spring boot application be packed to debian package.

### Installation

Unfortunately, it is not included to aptitude default repository for Ubuntu 14.04.
Thus, it is necessary to install it manually.

It is suggested ot use **webupd8team** repository for installing Java 8.


```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
```

You can either install Java 8 manually using

```
sudo apt-get install oracle-java8-installer
```

Or try to install *registry.deb* using

```
sudo dpkg -i install registry.deb
```

If transitive dependencies are absent, use the following command: 

```
sudo apt-get -fy install
```

If there are no errors in installation log, then *registry app* with all required dependencies is installed and launched successfully. 