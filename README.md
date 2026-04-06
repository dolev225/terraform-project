## Terraform - setup

This repository automates the deployment of a EC2 instance and LB 

## 📦 Prerequisites
* [Terraform](https://www.terraform.io/downloads.html) v1.0.0+
* Configured AWS CLI (`aws configure`)
  
## Architecture
This project creates:
* Deploy an EC2 Instance in the Public Subnet
* Deploy an Application Load Balancer with Auto Scaling
* A **Security Group** allowing Port 80 (HTTP) and 22 (SSH).
* An **EC2 Instance** (t3.micro by default).

## 👩🏽‍🍳 The Process

I started by setting a VPC with CIDR block and define subnet affter I created them . I define routing tables and attach it to the vpc .

the next step was attach an Internet Gateway to the VPC and associate it with the public subnet so we can connter the the EC2 throw the ethernet.


Finally, I run a test. I run the test on AWS privet accont and connet to the dns of the LB and stress test too check the LB & Auto Sscaling.

Along the way, while building everything, I took notes on what I've learned so I don't miss out on it. I also documented the behind-the-scenes processes every time a feature was added.

This way, I understood what I've built. The funny thing is, as soon as I started to document what happened behind the scenes and the features I've added, it made me realize that we fully understand something once we've actually taken a step back, thought about it, and documented what we've done. I think this is a good practice to follow when learning something new.

## 📚 What I Learned

During this project, I've picked up important skills and a better understanding of complex ideas, which improved my logical thinking.

## 🚦 Running the Project

To run the project in your local environment, follow these steps:

1. Clone the repository to your local machine.
2. Run `npm install` or `yarn` in the project directory to install the required dependencies.
3. Run `npm run start` or `yarn start` to get the project started.
4. Open [http://localhost:5173](http://localhost:5173) (or the address shown in your console) in your web browser to view the app.
