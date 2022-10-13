---
title: Attacking Active Directory serie -Part I
date: 2019-07-12
math: true
subtitle: What is active Directory?
image:
  placement: 2
  caption: ""
  filename: featured.jpg
---
# **High level overview of Active Directory**

Active Directory or AD is a windows-based directory service. It allows for centralized management of the authentication and authorization. It enables administrators to deploy role-based access control and least privilege efficiently. It stores information related to objects such as Computers,Users,Printers.Physically Active Directory is a collection of machines and servers connected inside of domains, that are a collective part of a bigger forest of domains, that make up the Active Directory network.

***But why using active Directory***

The majority of large companies use Active Directory because it allows for the control and monitoring of their user's computers through a single domain controller. It allows a single user to sign in to any computer on the active directory network and have access to his or her stored files and folders in the server, as well as the local storage on that machine. This allows for any user in the company to use any machine that the company owns, without having to set up multiple users on a machine. Active Directory does it all for you

## **Physical Active Directory Components**

The physical Active Directory is the servers and machines on-premise or in the Cloud

### Domain Controllers

* A server with the AD DS server role installed and that has been promoted to a domain controller
* Host a copy of the AD DS directory store
* Provide authentication and authorization services
* Replicate updates to other domain controllers in the domain and forest
* Allow administrative access to manage user accounts and network resources

### AD DS Data Store

* Contains the database files and process that store and mange directory information for users,services and application
* Consists of the Ntds.dit file
* stored by defualt in the %SystemRoot%\NTDS folder on all domain controllers
* Only accessible through the domain controller process and protocols



## Logical Active Directory Components

### Domains

* Manage and group objects in an organization
* An administrative boundary for applying policies to groups of objects
* A replication boundary for replicating data between domain controllers
* An authentication and authorization boundary that provides a way to limit the scope of access to resources

### Trees

* A hierarchy of domains
* create a two-way transitive trust with other domains
* share a contiguous namespace with the parents domain

### Forests

* A collection of domain trees
* Share a common schema
* Share a common configuration partition
* Share the Enterprise Admins and Schema Admins groups

### Organization Units

* AD containers that can contain users,groups,computers, etc...
* Represent the organization hierarchically and logically
* Manage a collection of objects in a consistent way
* Apply policies

### Trust

* Provide a mechanism for users to gain access to resources in another domain
* All domains in a forest trust all other domains in the forest (can extend outside of the forest)

There are two types of trusts that determine how the domains communicate.

* Directional - The direction of the trust flows from a trusting domain to a trusted domain
* Transitive - The trust relationship expands beyond just two domains to include other trusted domains

### Domain Policies

* dictate how the server operates and what rules it will and will not follow
* The policies apply to a domain as a whole

### AD DS Schema

* Defines every type of object that can be stores in the directory
* Enforces rules regarded Object creation and configuration



## Active Directory Domain Authentication

* LDAP - Lightweight Directory Access Protocol; provides communication between applications and directory services
* Certificate Services - allows the domain controller to create, validate, and revoke public key certificates
* DNS, LLMNR, NBT-NS - Domain Name Services for identifying IP hostnames



## Active Directory Domain Authentication

There are two main types of authentication in place for Active Directory: NTLM and Kerberos.

* Kerberos - The default authentication service for Active Directory uses ticket-granting tickets and service tickets to authenticate users and give users access to other resources across the domain.
* NTLM - default Windows authentication protocol uses an encrypted challenge/response protocol