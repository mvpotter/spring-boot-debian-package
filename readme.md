# Spring boot debian package

An example project that shows how can Spring boot application be packed to debian package.

### Launch using Vagrant

At the project root execute the following commands:

``` shell
mvn clean package
vagrant up
```

Wait for Vagrant to install required dependencies along with application package and launch it.
Open http://65.0.0.20:8080 in your browser and check that application is launched.

### Launch manually

Package requires Java 8, thus it is necessary to install it manually.

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
```

You can either install Java 8 yourself using

```
sudo apt-get install oracle-java8-installer
```

Or try to install *gs-spring-boot.deb* using

```
sudo dpkg -i install gs-spring-boot.deb
```

If transitive dependencies are absent, use the following command: 

```
sudo apt-get -fy install
```

If there are no errors in installation log, then *gs-spring-boot* app with all required dependencies is installed and launched successfully. 