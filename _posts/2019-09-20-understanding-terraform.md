---
layout: default
title: "Understanding Terraform"
blogs: blog1
---

# Understanding Terraform - My learnings so far.

---

As a junior developer, I am constantly trying to learn new things in attempt to better myself. At my last place of work, we went through a short period in which we migrated all of our services from Azure to AWS.  

When the DevOps team were gathering information about AWS, they realised that they could write their infrastructure as code, using Terraform. 

---

### What is Terraform?

Terraform is a tool that allows you to write your infrastructure as code; thus allowing you to build, change and version your infrastructure in a safe and easy manner. 

---

### How does it work?

As described by Terraform themselves on their website:

 "*Configuration files describe to Terraform the components needed to run a single application or your entire datacenter. Terraform generates an execution plan describing what it will do to reach the desired state, and then executes it to build the described infrastructure. As the configuration changes, Terraform is able to determine what changed and create incremental execution plans which can be applied.*"

Using Terraform is as simple as installing it on your machine and then adding a terraform user (with Programmatic Access) to your IAM Dashboard in the AWS Console. 

---

### What is an example of what you could use Terraform for?

At my last place of work, we had our production/live environment and our test/qa environment. Following typical practice, we always tried to keep our live environments (near enough) like for like. This ensures that you can perform accurate tests on the product(s) you wish to release.

However, prior to our shift to AWS and Terraform it was seemingly becoming more difficult to try and keep these two environments like for like. This was because of our expanding nature at the time. As we were making new services, we were also making the production environment larger and more complicated. 

Upon moving to Terraform, ensuring that the two environments were as similar as possible became a lot easier. This was due to the fact that you could define how you wanted your infrastructure to be in code.  In turn, allowing us to make them very similar in structure (the only differences between QA and LIVE were the resources used, i.e Load Balancers and size of instances). It also unlocked the potential to quickly create and delete new environments if we needed to. 

### Post by: **Callum Leeming, Junior Software Developer**