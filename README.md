# Daily_report
logs of everyday tech knowledge I learn or found interested to save for others too

## Maven archetype:generate

archetype: An ideal example of something.

`mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=Myproject -DarchetypeArtifactId=maven-archetype-quickstart -D-DarchetypeVersion=1.4 -DinteractiveMode=false`
for parameters understanding : [Click Here](https://maven.apache.org/archetype/maven-archetype-plugin/generate-mojo.html)

> -DinteractiveMode=false means  blank java project with all default options. (non-interactive)
> -DinteractiveMode=true means rest of the options will be specified by the user.( interactive )

## Day-2

1. PuTTYgen is a key generator tool for creating pairs of public and private SSH keys.


PuTTY will open a "network" between both machines. You'll get a console (like the shell) when you'll be connected. Really useful to administrate remote server from your computer.

Usually, the port is not 80, but 22.

2. Core Azure Services -Compute 
  a. Virtual machine
  b. Function app
  c. App Service
  d. Azure Kubernetes Services. 
  
 3. Creating a virtual machine on azure.
 hosting a webpage at server not localhost
 4. Networking :
  a. Virtual networks 
  b. load balancers
  c. application gateways : it do path way routing.
  d. DnS Zones
  e. CDN profile (content delivery network )
  
  
  ## Day-3
1. Core Azure Services - Storage
    a. Blob
    b. file storage
    c. tables
    d. Queues
    e. data lake storage
    f. Data Box
    
2. Core Azure Services - databse + Analytics 
  a. Sql databases
  b. CosmosDB
  c. Data Factory
  d. event hubs
  e. Data lake analytics
 
3. Core Azure Services - AI and Machine Learning
  a. Cognitive Services 
  b. Bot services
  c. Machine Learning Studio
  
    
4. Core Azure Services - Identity

  * Azure Active Drectory :
    *   => users and group

5. Core Azure Services : Management

  * a. log analytics
  * b. Cost and biling
  * c. automation  Account  
  * d. metrics


## Day-4
hands-on: Creating a virtual machine and hosting a webpage on a server.

## Day-5


* A.	IP Adress [ 0 -255] =>  4 bytes : 198.162.1.4 – Example
>  Start      0.0.0.0
> 0.0.0.1
> .
> .
> . 
> End	255.255.255.255
* B.	IPV4 Addressing [32 bits long]
* C.	For Azure we  pick CIDR Notation ( Classless inter domain Routing Notation ).
* D.	What is CIDR Notation.
 > 198.162.0.0/16 = 8 * 2 ( 8 bits = 1 byte )
 > 198.162.1.0/24 = 8 * 3

* Azure Virtual Networks :
> a.	Through connecting to the Vnet we use  > point to site VPN and site to site VPN 
> b.	For direct connection to a network we use EXPRESSROUTE
> NIC card provide’s IP address either public or private attached to virtual machine.
> VPN ( Virtual Netowrk ) gateway .
> NSG – Network Security Group.


## Day-6
Done a Minor project based on Cloud Azure

* Create 2 Virtual Networks :  Vnet_ 1   And   Vnet_2 
* Creating Two subnets in each Vnet.
* Create Virtual Machine of Vnet-1 and Vnet -2
* Assign Public IP to both VM In Vnet-1 and Vnet-2
* Peer  Vnet-1 and Vnet2
* Create a data disk and attach to VM-1
* Log on to VM and initialize the disk 

[click here](https://github.com/kushagra67414/Daily_report/blob/main/Minor_Project_Kushagra_Bansal.docx)

## Day-7
Hands on : Hosting a jenkin server using cloud

## Day-8

=> **AZURE STORAGE**

a. Structure data
  * Stored in a database table with rows and column, data having same field or properties, relies on keys to indicated relation among table.
  
b. UnStructure data
  * data which dont have any structure which just needed to be stored like videos, images, audio
  
c. Semi- Structure data
  * it does not fit into the table , rows and column
  * uses tag and keys to organize and provide a hierarchy for the data 

=> **AZURE SQL DATABASE**

* reliable, high-performance, secure database.
* build data-driven applications and websites.

![Screenshot (523)](https://user-images.githubusercontent.com/46487696/98438774-715d4d00-2112-11eb-9c5a-9809e1ed1cc9.png)

=> **AZURE COSMO DB****

![Screenshot (524)](https://user-images.githubusercontent.com/46487696/98438779-7c17e200-2112-11eb-939e-b28adb75c06b.png)


=> **AN AZURE STORAGE ACCOUNT**

* Processess high availabilty
* Provides Security
* Highly Scalable
* Task Redundant
* Is Highly durable

=> **ADVANTAGE OF AZURE STORAGE**

![Screenshot (525)](https://user-images.githubusercontent.com/46487696/98438783-8508b380-2112-11eb-87e3-3c80bdaa0bf1.png)


=> **AZURE STORAGE ACCOUNT TYPE**

* General Purpose Storage Client:

1. BLOBs(Binary Large Object) => used to store audio, video, etc random data or used for backup.
2. FILES => will having shared files or network  files.
3. QUEUES => How are we processing data one by one stored in buffered data.
4. TABLES => will have tabular data like structure data.

![2](https://user-images.githubusercontent.com/46487696/98439150-d9616280-2115-11eb-8d8a-5544d62b3ce1.png)

![Screenshot (533)](https://user-images.githubusercontent.com/46487696/98439202-42e17100-2116-11eb-83a9-f9969c2ca518.png)

![Screenshot (534)](https://user-images.githubusercontent.com/46487696/98439207-4aa11580-2116-11eb-8aaa-f9a418d169cc.png)


=> **WHAT IS REPLICATION IN AZURE STORAGE**

1. LRS => here 3+ copies of your data is stored in your same data center.

![Screenshot (562)](https://user-images.githubusercontent.com/46487696/98649831-1029b980-235e-11eb-8275-90d601679c0e.png)
![Screenshot (563)](https://user-images.githubusercontent.com/46487696/98649835-115ae680-235e-11eb-9b04-73e82018fced.png)

2. ZRS => here 3+ copies of your data is stored in different datacenter but in same region.

![Screenshot (566)](https://user-images.githubusercontent.com/46487696/98649858-1ae44e80-235e-11eb-9336-b8be2c1f6db4.png)
![Screenshot (567)](https://user-images.githubusercontent.com/46487696/98649861-1b7ce500-235e-11eb-857c-983956cdf0de.png)

3. GRS => here 6+ copies of your data is stored in far away from primary datacenter.

![Screenshot (568)](https://user-images.githubusercontent.com/46487696/98649877-23d52000-235e-11eb-870c-9de0ad7548b0.png)

4. RA-GRS => here 6+ copies of your data is stored in far away from primary datacenter but, with the read access.

![Screenshot (570)](https://user-images.githubusercontent.com/46487696/98649905-2d5e8800-235e-11eb-9437-fc98a4930b01.png)
![Screenshot (571)](https://user-images.githubusercontent.com/46487696/98649909-2f284b80-235e-11eb-816f-15d08a8f7337.png)


## Types of Blob Storage

![Screenshot (546)](https://user-images.githubusercontent.com/46487696/98483083-ae693280-222b-11eb-9498-9afcc340c083.png)

## Storage tiers

![Screenshot (548)](https://user-images.githubusercontent.com/46487696/98483102-c771e380-222b-11eb-8fd1-e4a7b0a94eae.png)

## Encryption and Replication

![Screenshot (549)](https://user-images.githubusercontent.com/46487696/98483129-f720eb80-222b-11eb-9bb0-1ea40a48b8fd.png)

## Comparion of azure and on-premises storage

![Screenshot (551)](https://user-images.githubusercontent.com/46487696/98483159-1586e700-222c-11eb-97e3-8439f035eac0.png)



## Shared Access Signature (SAS)

![Screenshot (558)](https://user-images.githubusercontent.com/46487696/98579191-47f41b00-22e4-11eb-8e75-d0cf2424539f.png)

Lets see how it looks =>

![Screenshot (559)](https://user-images.githubusercontent.com/46487696/98579419-a620fe00-22e4-11eb-8551-da1d43e52ae8.png)
![Screenshot (560)](https://user-images.githubusercontent.com/46487696/98579421-a7522b00-22e4-11eb-812c-229caa324b7a.png)
![Screenshot (561)](https://user-images.githubusercontent.com/46487696/98579425-a7eac180-22e4-11eb-8532-f2561b6f455d.png)




## Azure Security 

![Screenshot (572)](https://user-images.githubusercontent.com/46487696/98668851-77ebfe80-2376-11eb-8b58-503cc8b38c73.png)


## Cloud is a shared responsibility =>

![Screenshot (573)](https://user-images.githubusercontent.com/46487696/98668940-9d790800-2376-11eb-8255-c7e949a1eb28.png)


## AZURE ACTIVE DIRECTORY =>
* Single Sign on (SSO)
* Application Management
* Business to Business(B2B) identity Service
* Business to Customer(B2C) identity Service
* Device Management 

## Security Center => 

![Screenshot (589)](https://user-images.githubusercontent.com/46487696/99181154-ad1b9680-2752-11eb-8d5c-1ce068852a38.png)
![Screenshot (590)](https://user-images.githubusercontent.com/46487696/99181157-af7df080-2752-11eb-9aa4-4c0120085b18.png)
![Screenshot (591)](https://user-images.githubusercontent.com/46487696/99181159-b147b400-2752-11eb-94a6-5fdb54957a00.png)
![Screenshot (592)](https://user-images.githubusercontent.com/46487696/99181161-b1e04a80-2752-11eb-8c94-5b1889feb1b3.png)

## What is Azure Active Directory =>

![Screenshot (593)](https://user-images.githubusercontent.com/46487696/99181267-611d2180-2753-11eb-96c3-7396b7734d1f.png)

## RBAC =>

![Screenshot (594)](https://user-images.githubusercontent.com/46487696/99181277-81e57700-2753-11eb-95a1-b418ea8b53ae.png)

## Encryption =>

![Screenshot (595)](https://user-images.githubusercontent.com/46487696/99181309-a93c4400-2753-11eb-9650-593214a0cf80.png)
![Screenshot (596)](https://user-images.githubusercontent.com/46487696/99181312-a9d4da80-2753-11eb-9d53-dc8a3fcba240.png)
![Screenshot (597)](https://user-images.githubusercontent.com/46487696/99181315-aa6d7100-2753-11eb-82a9-20e7ae0d737d.png)

## DDOS =>

![Screenshot (598)](https://user-images.githubusercontent.com/46487696/99181324-c07b3180-2753-11eb-85c7-d2a41b42c8a4.png)
![Screenshot (599)](https://user-images.githubusercontent.com/46487696/99181326-c244f500-2753-11eb-834e-d4bb348e76cd.png)


## MONITOR AZURE INFRA

![Screenshot (611)](https://user-images.githubusercontent.com/46487696/99298561-e85fb780-286f-11eb-9e18-52f855be73d5.png)


## ROLE BASED ACCESS CONTROL (RBAC) AND AZURE POLICY

![Screenshot (611)](https://user-images.githubusercontent.com/46487696/99403522-90c55880-2910-11eb-8b6f-2fa02f2048e7.png)

![Screenshot (612)](https://user-images.githubusercontent.com/46487696/99403532-928f1c00-2910-11eb-8f0f-21bf1982febe.png)

![Screenshot (613)](https://user-images.githubusercontent.com/46487696/99403537-93c04900-2910-11eb-81cf-4bc05e6b8f5a.png)

![Screenshot (652)](https://user-images.githubusercontent.com/46487696/99403651-b6526200-2910-11eb-84b3-38b0f71466d3.png)

![Screenshot (653)](https://user-images.githubusercontent.com/46487696/99403656-b7838f00-2910-11eb-94aa-6f7ce9121a73.png)



## ENTERPRISE GOVERNANCE MANAGEMENT

![Screenshot (654)](https://user-images.githubusercontent.com/46487696/99420291-105c2300-2923-11eb-9d58-7c9636936242.png)


## AZURE BLUEPRINTS 

![Screenshot (655)](https://user-images.githubusercontent.com/46487696/99504179-29a5b380-29a5-11eb-8466-b32bab783e50.png)
![Screenshot (656)](https://user-images.githubusercontent.com/46487696/99504185-2ca0a400-29a5-11eb-9a7e-896ced5929ed.png)
![Screenshot (657)](https://user-images.githubusercontent.com/46487696/99504196-332f1b80-29a5-11eb-9fe1-3a6f3ba4e860.png)
![Screenshot (658)](https://user-images.githubusercontent.com/46487696/99504198-34604880-29a5-11eb-86ab-2e3daa4b9b0d.png)
![Screenshot (659)](https://user-images.githubusercontent.com/46487696/99504199-34f8df00-29a5-11eb-97eb-0f33c8387b9c.png)
![Screenshot (660)](https://user-images.githubusercontent.com/46487696/99504203-35917580-29a5-11eb-801e-03f5dc4701d4.png)



## AZURE MONITOR 


![Screenshot (661)](https://user-images.githubusercontent.com/46487696/99504305-5d80d900-29a5-11eb-9683-d81b8bc9d222.png)
![Screenshot (662)](https://user-images.githubusercontent.com/46487696/99504308-5f4a9c80-29a5-11eb-9527-02193bb279f5.png)
![Screenshot (663)](https://user-images.githubusercontent.com/46487696/99504309-5fe33300-29a5-11eb-987c-d933d2648f4a.png)
![Screenshot (664)](https://user-images.githubusercontent.com/46487696/99504609-c5cfba80-29a5-11eb-9467-07d7f36ee07f.png)
![Screenshot (665)](https://user-images.githubusercontent.com/46487696/99504314-61146000-29a5-11eb-8f17-cf7b9daa37b6.png)


## AZURE HEALTH

![Screenshot (667)](https://user-images.githubusercontent.com/46487696/99504472-99b43980-29a5-11eb-8a0a-9bd69d3781c7.png)


