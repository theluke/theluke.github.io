---
marp: true
theme: default
paginate: true

---

# Exploiting IAM security misconfigurations

---
# Introduction

We will explore three common IAM security misconfigurations scenarios, discover how they can be exploited, and how easy it is to detect and correct them.

Identity and access management (IAM) misconfigurations are one of the most common concerns in cloud security. Over the last few years, we have seen how these security holes put organizations at increased risk of experiencing serious attacks on their Cloud accounts.

To some, cloud environments might look like safe places where security is set by default. However, the truth is that security follows a shared responsibility model. For example, you are in charge of securing AWS console access.

---
![bg](https://example.com/background.jpg)

But what if a misconfiguration over your users or roles is applied in your environment?

![image01](https://sysdig.com/wp-content/uploads/IAM-security-misconfiguration-01.png)

---
# Why IAM security misconfigurations is a big deal

AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and granularly manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.

From what IAM is about, we can easily agree this is a piece of our infrastructure we need to focus on. If this service is misconfigured, users or groups might cause huge damage to your infrastructure.

---

Due to the fine granularity of permissions available in the Cloud environments, applying the least privileges concept, so carefully giving exactly what a user needs to perform its actions, is absolutely fundamental. Just a misconfigured privilege could lead to an attacker escalating the privileges inside the environment.

![w:612 h:412](https://sysdig.com/wp-content/uploads/IAM-security-misconfiguration-02.png)

---

# IAM security misconfiguration scenarios
Scenario #1: A user can create a new policy version
In this scenario, an attacker who found valid credentials in Pastebin is able to access the cloud environment. It turns out that the compromised user has permission to create a new version of one of their IAM policies.

This allows the adversary to define their own custom permissions and gain full administrator access to the AWS account.
![image03](https://sysdig.com/wp-content/uploads/IAM-security-misconfiguration-03.png)

---
