# Day 02

### **Q: What is AWS IAM, and why is it important?**

AWS IAM (Identity and Access Management) is a service provided by Amazon Web Services that helps you control access to your AWS resources. It allows you to manage user identities, permissions, and policies. IAM is important because it enhances security by ensuring that only authorized individuals or entities have access to your AWS resources, helping you enforce the principle of least privilege and maintain a secure environment.

---

### **Q: What is the difference between IAM users and IAM roles?**

IAM users represent individual people or entities that need access to your AWS resources. They have their own credentials and are typically associated with long-term access. On the other hand, IAM roles are used to grant temporary access to AWS resources, usually for applications or services. Roles have associated policies and can be assumed by trusted entities to access resources securely.

---

### **Q: What are IAM policies, and how do they work?**

IAM policies are JSON documents that define permissions. They specify what actions are allowed or denied on AWS resources and can be attached to IAM users, groups, or roles. Policies control access by matching the actions requested by a user or entity with the actions allowed or denied in the policy. If a requested action matches an allowed action in the policy, access is granted; otherwise, it is denied.

---

### **Q: What is the principle of least privilege, and why is it important in IAM?**

The principle of least privilege states that users should be granted only the permissions necessary to perform their tasks and nothing more. It is important in IAM because it minimizes the risk of unauthorized access and limits the potential damage that could be caused by a compromised account. Following the principle of least privilege helps maintain a secure environment by ensuring that users have only the permissions they need to perform their job responsibilities.

---

### **Q: What is an AWS managed policy?**

An AWS managed policy is a predefined policy created and managed by AWS. These policies cover common use cases and provide predefined permissions for specific AWS services or actions. AWS managed policies are maintained and updated by AWS, ensuring they stay up to date with new AWS services and features. They can be attached to IAM users, groups, or roles in your AWS account.

--- 

## 🔐 AWS IAM Core Concepts

### **👤 IAM Users**
An **IAM user** is an **individual identity** within your AWS account. It represents a **single person or application** that needs to interact with AWS services. Each user has **permanent credentials** (username, password, access keys) and can have **permissions** assigned directly or through groups.

> 🔸 **Use case**: Developers, admins, or automated systems requiring long-term access.

---

### **👥 IAM Groups**
An **IAM group** is a **collection of IAM users**. Groups allow you to assign the **same set of permissions** to multiple users efficiently by attaching policies to the group instead of each individual user.

> 🔸 **Use case**: Granting common permissions to teams like DevOps, QA, or Finance.

---

### **🎭 IAM Roles**
An **IAM role** is an **identity with specific permissions** that can be **assumed by users, services, or applications**. Roles provide **temporary security credentials** and are used for **cross-account access**, **federated identity**, or **service-to-service access**.

> 🔸 **Use case**: EC2 accessing S3, Lambda invoking DynamoDB, or granting temporary access to a third party.

---

### **📜 IAM Policies**
An **IAM policy** is a **JSON document** that defines what **actions** are **allowed or denied** on which **AWS resources**. Policies are attached to **users**, **groups**, or **roles** and are the core of **permission management** in AWS.

> 🔸 **Use case**: Allowing `s3:PutObject` on a specific bucket, denying `ec2:TerminateInstances`, or enabling full admin access.

---

📝 **Summary Table**

| Concept       | Description                                   | Credentials | Permissions Scope         |
|---------------|-----------------------------------------------|-------------|----------------------------|
| **User**      | Single AWS identity for a person/app          | Yes         | Direct or via group        |
| **Group**     | Set of users with shared permissions          | No          | Through attached policies  |
| **Role**      | Assumable identity for temporary access       | Temporary   | Through attached policies  |
| **Policy**    | Defines permissions using JSON                | N/A         | Attached to user/group/role|


