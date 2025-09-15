# 🚀 AWS EC2 Guide and Interview Questions

## 📘 Introduction to EC2

**What is EC2, and why is it important?**

- Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.
- Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.
- Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.
- Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.

---

## 💡 EC2 Use Cases

- Deliver secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.
- Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively.
- Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing.
- Deliver the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects.

---

## 🧩 EC2 Instance Types

### General Purpose
General Purpose instances are designed to deliver a balance of compute, memory, and network resources. They are suitable for a wide range of applications, including web servers,
small databases, development and test environments, and more. 
**Use Cases:** Web servers, small databases, dev/test environments.

### Compute Optimized
Compute Optimized instances provide a higher ratio of compute power to memory. They excel in workloads that require high-performance processing such as batch processing, 
scientific modeling, gaming servers, and high-performance web servers.
**Use Cases:** Batch processing, scientific modeling, gaming servers.

### Memory Optimized
Memory Optimized instances are designed to handle memory-intensive workloads. They are suitable for applications that require large amounts of memory, such as in-memory databases,
real-time big data analytics, and high-performance computing.  
**Use Cases:** In-memory DBs, big data analytics, high-performance computing.

### Storage Optimized
Storage Optimized instances are optimized for applications that require high, sequential read and write access to large datasets. 
They are ideal for tasks like data warehousing, log processing, and distributed file systems. 
**Use Cases:** Data warehousing, log processing, file systems.

### Accelerated Computing
Accelerated Computing Instances typically come with one or more types of accelerators, such as Graphics Processing Units (GPUs),
Field Programmable Gate Arrays (FPGAs), or custom Application Specific Integrated Circuits (ASICs). 
These accelerators offload computationally intensive tasks from the main CPU, enabling faster and more efficient processing for specific workloads.
**Use Cases:** ML training/inference, video rendering, simulations.

---

## 🧬 EC2 Instance Families

| Family | Purpose |
|--------|---------|
| C      | Compute |
| D      | Dense Storage |
| F      | FPGA |
| G      | GPU |
| Hpc    | High Performance Computing |
| I      | I/O Optimized |
| Inf    | AWS Inferentia |
| M      | General Purpose (Most Use Cases) |
| P      | GPU for ML/DL |
| R      | Memory Optimized |
| T      | Burstable (Turbo) |
| Trn    | AWS Tranium (Training ML) |
| U      | Ultra High Memory |
| VT     | Video Transcoding |
| X      | Extra-large Memory |

---

## ⚙️ Instance Additional Capabilities

| Suffix | Meaning |
|--------|---------|
| a      | AMD CPUs |
| g      | AWS Graviton (ARM) |
| i      | Intel CPUs |
| d      | Instance Store Volumes |
| n      | Network / EBS Optimized |
| e      | Extra Memory / Storage |
| z      | High Performance CPUs |

---

## 🎯 EC2 Interview Questions and Answers

### 1. **What is EC2?**
EC2 (Elastic Compute Cloud) is a core AWS service that lets you rent virtual servers (instances) in the cloud to run applications. It's scalable, flexible, and supports a wide variety of workloads.

---

### 2. **What are EC2 instance types?**
Instance types are combinations of CPU, memory, storage, and network resources tailored to different use cases like compute-optimized, memory-optimized, etc.

---

### 3. **What is an AMI?**
An AMI (Amazon Machine Image) is a template with software configuration (OS, apps, data) used to launch EC2 instances.

---

### 4. **What is the difference between EBS and Instance Store?**
- **EBS:** Persistent block storage, survives instance stop/start.
- **Instance Store:** Temporary, data lost when instance is stopped or terminated.

---

### 5. **What is a Security Group?**
A Security Group is a virtual firewall that controls inbound and outbound traffic to EC2 instances. It's stateful and allows return traffic by default.

---

### 6. **What are Key Pairs?**
Used for SSH authentication. Public key is stored in AWS, private key is held by the user.

---

### 7. **What are EC2 pricing models?**
- On-Demand
- Reserved Instances
- Spot Instances
- Dedicated Hosts
- Savings Plans

---

### 8. **How to monitor EC2 instances?**
Using Amazon CloudWatch for:
- CPU utilization
- Disk I/O
- Network traffic
- Status checks
Also includes logs and alarms.

---

### 9. **What is Auto Scaling?**
Auto Scaling adjusts the number of instances based on demand. Helps with high availability and cost control.

---

### 10. **What’s the difference between Stop and Terminate?**
- **Stop:** Instance shut down, can restart later.
- **Terminate:** Instance permanently deleted.

---

### 11. **What is EC2 User Data?**
Used to run scripts at instance launch. Ideal for bootstrapping software or setting environment configurations.

---

### 12. **What is EC2 Instance Metadata?**
Provides information about the instance (e.g., IP, region, IAM role) accessible from within the instance.

---

### 13. **What’s the difference between Spot and Reserved Instances?**
- **Spot:** Cheap, interruptible.
- **Reserved:** Long-term commitment, cost-effective for predictable workloads.

---

### 14. **How to recover a lost EC2 SSH Key?**
- Detach EBS root volume.
- Attach to another instance.
- Add new public key to `.ssh/authorized_keys`.
- Reattach and boot.

---

### 15. **How to secure EC2 instances?**
- Use IAM roles.
- Restrict Security Groups.
- Enable automatic patching.
- Encrypt data (EBS, TLS).
- Disable root login, use SSH keys.

---

### 16. **What is EC2 Hibernation?**
Saves instance memory + state to disk. Faster startup on resume. Supported only for specific instance types and OS.

---

### 17. **What is AWS Nitro System?**
A secure hypervisor and hardware offload system used for EC2. Ensures isolation, better performance, and monitoring.

---

### 18. **How does EC2 interact with VPC?**
Instances run inside a VPC. You define subnets, IP ranges, route tables, gateways, etc. Control connectivity and security at network level.

---

### 19. **What is EC2 Instance Lifecycle?**
States: `pending → running → stopping → stopped → terminating → terminated`.

---

### 20. **Best Practices for EC2 Cost Optimization**
- Use Spot for flexible workloads.
- Use Reserved/Savings Plans.
- Schedule shutdowns.
- Right-size instances.
- Monitor with Cost Explorer & Trusted Advisor.

---

## 📂 Summary

Amazon EC2 is the backbone of AWS compute. Mastering it is essential for any AWS practitioner, architect, or developer. The above knowledge, combined with hands-on experience, will help you ace interviews and build production-grade cloud architectures.

---

> ✅ **Pro Tip**: Always test EC2 configurations and cost implications in AWS Free Tier or using the pricing calculator before deploying at scale.


## 🛠️ Steps to Create an EC2 Instance on AWS

Follow these steps to launch a virtual server (EC2 instance) in AWS:

### 1. **Log into AWS Console**
Go to [https://console.aws.amazon.com](https://console.aws.amazon.com) and log in with your AWS credentials.

---

### 2. **Navigate to EC2 Dashboard**
- From the **Services** menu, select **EC2**.
- Click on **"Instances"** from the left sidebar.
- Click the **"Launch Instance"** button.

---

### 3. **Choose an Amazon Machine Image (AMI)**
- Select an AMI (e.g., Amazon Linux 2, Ubuntu, Windows Server).
- You can also use your custom AMI or one from AWS Marketplace.

---

### 4. **Choose Instance Type**
- Pick an instance type based on your workload (e.g., `t2.micro`, `m5.large`).
- AWS Free Tier eligible: `t2.micro` or `t3.micro`.

---

### 5. **Configure Instance Settings**
- Number of instances
- Network: Choose a **VPC** and **subnet**
- IAM role (optional but recommended)
- Enable monitoring (CloudWatch)
- Add **User Data** (optional) — run a script at launch.

---

### 6. **Add Storage**
- Add one or more **EBS volumes**
- Choose size, type (e.g., gp2, gp3), and whether to delete on termination
- Optionally encrypt the volume

---

### 7. **Configure Security Group**
- Set inbound rules: e.g., allow **SSH (port 22)** for Linux or **RDP (port 3389)** for Windows
- Restrict access using IPs (e.g., `My IP` or CIDR range)
- Set outbound rules (usually allow all)

---

### 8. **Choose Key Pair**
- Select an existing **Key Pair**, or create a new one
- Download and save the `.pem` file securely — **you cannot download it again**
- You’ll need it to SSH into the instance

---

### 9. **Review and Launch**
- Review all settings: AMI, instance type, security group, key pair, etc.
- Click **"Launch"**
- Your instance will be in `pending` state, then transition to `running`

---

### 10. **Connect to Your EC2 Instance**

#### For Linux:
```bash
ssh -i "your-key.pem" ec2-user@your-public-ip


