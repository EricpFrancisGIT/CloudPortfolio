## The Keys to the Kingdom....Creating the First Administrator Level IAM Account for Otsego Industries
![image](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/e1d3efc6-71b6-4804-800c-bb7d9505ad5f)

## Overview
The IT Director of Otsego Industries is looking to initiate some cost savings for the company.  I am a Senior System Administrator for the company Otsego Industries, and I have been tasked with the responsibility to consolidate the company’s aging IT infrastructure via virtualization.  I am currently evaluating cloud providers to show as a proof of concept to the Director, however before I start building/creating anything in the cloud, I am going to need to create some users/roles/groups.
## Introduction
Hello again and thank you for stopping to read this journey into virtualization/cloud computing for the company (fake/made up, obviously) that I am working for.  Now the direction that I was given by the IT Director for Otsego Industries was that we need to trim down some costs, and one of the things that I am looking to do is to incorporate a hybrid cloud model meaning that some pieces of the physical datacenter would still be active, while other pieces would be working solely in the cloud.
	I have decided that the first cloud provider that I will be engaging and creating these POC’s in is going to be Amazon Web Services (AWS).  Now it would be relatively simple to just sign up and start building things out under a root user, correct?   While that would seem rather prudent to do that, I will go about things a little more cautiously. I am going to treat this with the thought of “if all goes well, and the director approves, I could leave these built up and running without needing to tear it all down”. 
	But before I can build out, I will need to get some initial users created, then to make it a little easier I will create some groups and assign these users to that group. 

## Prerequisites
	Before any building commences, I will need to have the following prerequisites fulfilled in order to start, and I will also be sticking to the AWS Free Tier as much as possible. 
	-AWS Account
	-Billing address
	-Payment card.
	I provide these details during the setup process, along with a note to myself to turn off any computing instances or databases when not in use so that I am not getting charges on personal debit card.  

## Documentation
After the sign-up process, I can now build everything I want in my environment, yes?  NO I cannot, and the reason is simple: while building under the root account is the easy way to go, its also the riskiest way.  What happens if someone manages to get access to that root account, as in some of the news reports about S3 buckets being emptied or even viewed?  That cannot and must not happen, so therefor I must create my own Admin level account, along with a group that has the permissions assigned to it necessary for the administrator-level tasks.  So after I log in with my root user, I land here at the management console which I am certain we all have come to know intimately, but I need to get to where I am going to be creating these users.  So I navigate to the search button and enter in “IAM” in search, which yields the result shown here. 
![image](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/d599381c-ba5e-4743-8b11-4d7795944029)
Figure 1 IAM Search

Now I have arrived where I need to be, and the first thing I am going to do is create my own Admin level account.  However, I am going to want to create a User group and assign it the Administrator Access permission level, so when I start creating users, I can add them to the group and those users will be granted Administrator access to the entire account. So under Access Management, I click the “User groups” link and then select “Create Group”. 
![image](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/5e456c36-3599-41de-aab6-5eabd02e5e04)
Figure 2 IAM Group Creation

The Next screen I am presented with is where I can name this group, attach permission policies and even users if I had created any yet.  Again, keeping security in mind, I make the group name somewhat inconspicuous, I name it “Otsego_Behemoth”, I attach the administrator access policy and complete.  Now I go over to Users and select the “Create User” button like the one you see here: 
![image](https://github.com/EricpFrancisGIT/CloudPortfolio/assets/158304673/022c14fe-d0ee-4243-a204-f23c5513a4f2)
Figure 3 Creating User

	Now to create my user account, I am wanting to make it something unique and not to tip off anyone that this is an admin-level account, some naming it simply “Admin” or even “Otsego-admin” is not going to be utilized.  Instead, I am going to be using my own name, making sure to give it access to the AWS Console, otherwise I won’t be able to do much.   Seeing as how this is the first of many I will be doing, I am going to be creating an IAM user.  Should the director approve of this proof of concepts along with a migration to AWS, I could implement Identity Center at a later date.
	Finally, I am going to be entering my own password, keeping it safe in something like KeePass on my own system, but I am not going to change it just yet and I click next to advance to the next step.  Here is where I am going to add it to the Behemoth group and where I can download a CSV file.  Within this CSV file are my credentials and a console URL for me to use which will make it simpler and easier to sign-in.  With these credentials, I now can sign in with mine instead of using the root.  Now of course I could streamline this and automate the account creation process using something like terraform, however this is merely a proof of concept that I am using.  But do not worry gentle reader, I will be getting there where I will be using automation and terraform to help streamline everything as much as I am able to.
	I repeat this manual process, having created accounts for a couple other admins named 
Nergal and Orion, which I also download the credentials for and save them in a safe place to give to them at a later date. While it would be advantageous to tighten up on security, at this moment I will be holding off on that, at least until the Director gives the approval and we start migrating over.  That will be something to note for yourselves, dear reader, should you be faced with something like this.
	I now have the “Keys to the Kingdom” in my grasp, now comes the best part where I can flex my muscle and skills to “laying the foundation” for Otsego’s potential move into the cloud. But that will be an adventure for another time, dear reader.  Until then have a good day and a better weekend.


