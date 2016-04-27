## Developer Cloud Sandbox for coast colour processing of MERIS Full Resolution with BEAM 

TBW

## Quick link
 
* [Getting Started](#getting-started)
* [Installation](#installation)
* [Submitting the workflow](#submit)
* [Community and Documentation](#community)
* [Authors](#authors)
* [Questions, bugs, and suggestions](#questions)
* [License](#license)
* [Funding](#funding)

### <a name="getting-started"></a>Getting Started 

To run this application you will need a Developer Cloud Sandbox that can be requested at support (at) terradue.com

A Developer Cloud Sandbox provides Earth Sciences data access services, and helper tools for a user to implement, test and validate a scalable data processing application. It offers a dedicated virtual machine and a Cloud Computing environment.
The virtual machine runs in two different lifecycle modes: Sandbox mode and Cluster mode. 
Used in Sandbox mode (single virtual machine), it supports cluster simulation and user assistance functions in building the distributed application.
Used in Cluster mode (a set of master and slave nodes), it supports the deployment and execution of the application with the power of distributed computing for data processing over large datasets (leveraging the Hadoop Streaming MapReduce technology). 

### <a name="installation"></a>Installation

#### Pre-requisites

Log on the developer sandbox and run these commands in a shell:

* Install **Java 7**

```bash
sudo yum install -y java-1.7.0-openjdk
```

* Select Java 7

```bash
sudo /usr/sbin/alternatives --config java
```
This will show on the terminal window:

```
There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
 + 1           /usr/java/jdk1.6.0_35/jre/bin/java
   2           /usr/lib/jvm/jre-1.5.0-gcj/bin/java
*  3           /usr/lib/jvm/jre-1.7.0-openjdk.x86_64/bin/java

Enter to keep the current selection[+], or type selection number:
```

Select java 1.7 out of the menu options by typing the correct number (here it's *3*).

##### Using the releases

Log on the Developer Cloud Sandbox.

Download the rpm package from https://github.com/ec-ecopotential/dcs-beam-coastcolour/releases.

Install the downloaded package by running these commands in a shell:

```bash
sudo yum -y install dcs-beam-coastcolour-<version>.x86_64.rpm
```

> At this stage there are no releases yet

#### Using the development version

Install the pre-requisites as instructed above.

Log on the Developer Cloud Sandbox and run these commands in a shell:

```bash
git clone git@github.com:ec-ecopotential/dcs-beam-coastcolour.git
cd dcs-beam-coastcolour
mvn install
```

### <a name="submit"></a>Submitting the workflow

To submit the application with its default parameters, run the command below in the Developer Cloud Sandbox shell:

```bash
ciop-run
```
Or invoke the Web Processing Service via the Sandbox dashboard providing the start & end date/time of the Time of Interest and the bounding box of the Area of Interest.

### <a name="community"></a>Community and Documentation

To learn more and find information go to 

* [Developer Cloud Sandbox](http://docs.terradue.com/developer)  
* [ESA Coast Colour project](http://www.coastcolour.org/)
* [BEAM Toolbox](http://www.brockmann-consult.de/cms/web/beam/)

### <a name="authors"></a>Authors (alphabetically)

* Brito Fabrice
* D'Andria Fabio
* Rossi Cesare

### <a name="questions"></a>Questions, bugs, and suggestions

Please file any bugs or questions as [issues](https://github.com/ec-ecopotential/dcs-beam-coastcolour/issues/new) or send in a pull request if you corrected any.

### <a name="license"></a>License

Copyright 2016 Terradue Srl

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0

### <a name="funding"></a>Funding

This processing service is an evolution of the [Ocean colour atmospheric correction data challenge](https://github.com/ocean-color-ac-challenge) applications

The ECOPOTENTIAL project has received funding from the European Union's Horizon 2020 research and innovation programme under grant agreement No 641762
