##  Laying the Foundation—Creating the First VPC for Otsego.
![Picture1](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/46f7d531-d245-4c50-a55a-5e6df7ee184a)

## Introduction
Good morning readers and welcome back to this cloud journey with me and my made-up company, Otsego Industries. The last time we were together, I had just created the account in AWS, gave my billing information, and then created the first Admin-level accounts to start building with, along with permissions and even an Admin group.  Now comes the fun part, creating the first VPC for Otsego.  Now let’s get to the meat of the issue.

## Prerequisites
When you first get into the cloud provider of your choice, you would think its just lift and shift your servers into the cloud and boom, it works! No issues, right?  Wrong.  That kind of thinking is something that we Administrators have had to impart to our users, our higher ups and indeed some of our fellow Administrators.  Just because you hear that moving to the cloud is easy, doesn’t mean you have to put in the work.  Before anything, you need to lay the foundation of your footprint into the cloud. What are you going to be need beforehand? Based on my own experience, yours may vary dear reader, this is what you will need:
o	The cloud provider of your choice
o	An account set up.
o	Username/password

## Documentation

Many of us in our chosen fields have had to change and adapt our way of thinking as well as the tools that we have at our disposal. Instead of having big bulky servers in our datacenter, miles and miles of cabling from switches and routers, storage arrays and power strips, we now have a few cabinets with servers, storage and cabling nicely organized feeding into our central network hub/switch/core router and a virtualization hypervisor (VMWare, Proxmox, Hyper-V) to now getting into the cloud itself. The foundation of the cloud, of your company footprint in the cloud, is the implementation of a VPC. 
	You might be scratching your head going “ok Eric, what are you talking about?  What is a VPC?”  Excellent question, and here is the barebones answer to your question.  A VPC or Virtual Private Cloud is typically defined as “the division of a service provider's public cloud multi-tenant architecture to support private cloud computing” (Gillis & Knapp, 2023).  Think of it this way: your company’s infrastructure is going to be occupying a section of the cloud providers equipment like you would occupy an apartment, but you would only be paying for what you consume in terms of compute, storage, databases, and networking. 
Now let us get to the fun part.  Using the credentials I created from the previous demonstration, I log into my admin account for Otsego in AWS, and I am greeted with our home page we all know and love: 

![Picture2](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/3169dcfd-ca25-4334-8c2e-368a4cbf403e)