---
layout:         doc-toc
title:          "Containers - Documentation"
category:       "containers"
logo:           docker 
order:          8
excerpt:        "continuousphp docker containers."
---
continuousphp docker containers include by default the following services: 

* [mysql](/documentation/databases/mysql/) 
* [postgreql](/documentation/databases/postgresql/)
* [couchbase](/documentation/nosql/couchbase/)
* [apache2](/documentation/webserver/)
* [mongodb](/documentation/nosql/mongodb/)
* [redis](/documentation/nosql/redis/)

They also include also the following tools and applications:

* [eb](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3.html) (AWS ElasticBeanstalk)
* [graphviz](http://www.graphviz.org/Documentation.php)
* latex base & recommended 
* [nvm](/documentation/nodejs/) 
* [rbenv](/documentation/ruby/)
* [subversion](https://subversion.apache.org/)
* [mailcatcher](/documentation/emails/mailcatcher/)

All locales have been installed and configured.


continuousphp is using the following docker engine version : 

- **Client**
	- Version:      1.12.1
 	- API version:  1.24
 	- Go version:   go1.6.3
 	- Git commit:   23cf638
 	- Built:        Thu Aug 18 17:52:38 2016
 	- OS/Arch:      linux/amd64

- **Server**
	- Version:      1.12.1
	- API version:  1.24
 	- Go version:   go1.6.3
 	- Git commit:   23cf638
 	- Built:        Thu Aug 18 17:52:38 2016
 	- OS/Arch:      linux/amd64



If you need any other packages installed, as sudo, you can easily install them with a Phing target in your *build.xml*:

```xml
<target name="apt-package">
   <echo message="Install packages"/>
   <exec dir="${project.basedir}"
         command="sudo apt-get update ; sudo apt-get -y install <PACKAGE_NAME>"
         checkreturn="true"
         passthru="true"/>
</target>
```

Please feel free to contact us if you think that there is missing something essential in our containers!
