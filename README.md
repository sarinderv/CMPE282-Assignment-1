# Sarinder Virk – CMPE 282 – Assignment #1

I used a Powershell script to load 300,000 accounts. Here are the steps I took:

## A.	Create Microsoft AD Directory Service in AWS
1.	Created 2 Subnets one with CIDR 10.0.0.0/25 and the other 10.0.0.1/25 in two separate availability zones
2.	Created a VPC with those two subnets
3.	Created a Microsoft AD Directory Service (Enterprise - 1 month free trial)

![image](https://user-images.githubusercontent.com/4393945/154877822-ae818d92-b2cd-4046-81f1-ab5c2f54f45e.png)

## B.	Bulk load CSV file containing 300,000 users
1.	Download data dump from https://raw.githubusercontent.com/datacharmer/test_db/master/load_employees.dump
2.	Massage the datadump into a CSV file containing the attribute fields to put into Active Directory
3.	Download a Powershell script from here: https://activedirectorypro.com/create-bulk-users-active-directory/#powershell
4.	Run the Powershell script to create the users one by one:

![image](https://user-images.githubusercontent.com/4393945/154877834-96a80845-2d86-4d0c-a9ed-0f5c5f04fe5a.png)

I let the script run for about 2 hours so far ...

Active Directory now has thousands of users:

![image](https://user-images.githubusercontent.com/4393945/154877724-4675d0d0-fbb8-4997-bab3-3501139a277f.png)

Check the count of users in Active Directory, is over 50,000:

![image](https://user-images.githubusercontent.com/4393945/154877853-b5f352ed-e9ad-45c9-b211-f949754fd8c6.png)
