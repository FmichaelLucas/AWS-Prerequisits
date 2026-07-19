# Cloud Security using AWS IAM

**Project Link:** [Project](https://nextwork.ai/confident_navy_elegant_tuturiwhatu/docs/aws-security-iam)

**Author:** France Michael M. Abacial
**Current Email:** fmabacial@gmail.com

---
![Image](https://i.imgur.com/a8BBREV.png)
---

## Introducing Today's Project!

### Project overview
In this project, I will demonstrate... I'm doing this project to learn... how to set up my IAM account

### Tools and concepts
Services I used were... launching ec2 instances creating an IAM policy and creating an AWS account alias

Key concepts I learnt include... setting up policies and making clear levels of authorization

### Project reflection
This project took me approximately... 20 minutes 

The most challenging part was... creating an account alias because my internet failed to be stable at the given moment

It was most rewarding to... finish this project 

---

## Tags

### What I did in this step
In this step, I will... Launch two Amazon EC2 instances so that I can increase NextWork's computing power

### Understanding tags
Tags are... labels that can be attached to AWS resources for organization.

### My tag configuration
The tag I’ve used on my EC2 instances is called... "Env" with a value of "production" or "development" to label the instanced I've used in production vs development environments.

The value I’ve assigned for my instances are... "production"

![Image](https://i.imgur.com/L2nOjGf.png)

---

## IAM Policies

### What I did in this step
In this step, I will... set up permission policies.

because... we don't want our intern to accidentally shut down the platform or push their changes to the production environment while they're just testing things out.

### Understanding IAM policies
IAM policies or "Identity and Access Management policy" is a rule for who can do what with your AWS resources.

### The policy I set up
For this project, I’ve set up a policy using... JSON method

### Policy effect
I’ve created a policy that... will allow some actions like starting, stopping, and describing EC2 instances. While denying instances tagged with "Env = development" the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource
The Effect, Action, and Resource attributes of a JSON policy means... Effect can have two values - either Allow or Deny - to indicate whether the policy allows or denies a certain action. Action is a list of the actions that the policy allows or denies. Specifying the Resource in the lines means resources with the Env - development tag are impacted by my statement

## My JSON Policy
![Image](https://i.imgur.com/PJGdHTA.png)

---

## Account Alias

### What I did in this step
In this step, I will... create an AWS Account Alias

because... it would make it easier to remember and share my AWS console's login URL with others.

### Understanding account aliases
An account alias is... a friendly name for my AWS account that I can use instead of my account ID (which is usually a bunch of digits) to sign in to the AWS Management Console.

### Setting up my account alias
Creating an account alias took me... less than a minute

Now, my new AWS console sign-in URL is... nextwork-alias-france

![Image](https://i.imgur.com/G10BC6a.png)

---

## IAM Users and User Groups

### What I did in this step
In this step, I will... set up a dedicated IAM group for all NextWork interns

because... if I do so, I will then be able to manage all intern's permissions from one place.

### Understanding user groups
IAM user groups are... a collection/folder of IAM users. It allows me to manage permissions for all the users in my group at the same time by attaching policies to the group rather than individual users.

### Attaching policies to user groups
I attached the policy I created to this user group, which means... they will be granted permissions associated with that group.

### Understanding IAM users
IAM users are... the people that will get access to your resources/AWS account

---

## Logging in as an IAM User

### Observations from the IAM user dashboard
Once I logged in as my IAM user, I noticed... some of the dashboards denied my access

This was because... I was using an IAM account.

![image](https://i.imgur.com/nHicOVO.png)

---

## Testing IAM Policies

### What I did in this step
In this step, I will... Login into the AWS using the intern's IAM user

because... we would like to test the intern's access to your production and development instance.

### Testing policy actions
I tested my JSON IAM policy by... testing if I could stop certain instances

### Stopping the production instance
When I tried to stop the production instance... I was stopped the system

This was because... the account used did not have the proper authorization.

![Image](https://i.imgur.com/BxOmwsL.png)

### Stopping the development instance
Next, when I tried to stop the development instance... it worked

This was because... I had the proper authorization to perform this action.

![image](https://i.imgur.com/UIki89M.png)
