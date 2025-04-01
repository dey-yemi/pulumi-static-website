**# Fast Static Website Deployment with Pulumi**

Pulumi is a powerful Infrastructure as Code (IaC) platform that automates, secures, and manages cloud resources using familiar programming languages. This project demonstrates how to deploy a static website on **AWS** using **Pulumi** with **Python**.

---

## **Technologies Used**

- **Cloud Provider:** AWS
- **Key Services:** S3, CloudFront
- **Programming Language:** Python 3.x

## **Prerequisites**

Before getting started, ensure you have:
- An **AWS account** with a basic understanding of AWS services.
- Familiarity with **Linux commands**.
- A **Pulumi account** to access Pulumi Cloud.

---

## **Installation Steps**

### **1. Install Pulumi**
Run the following command in **PowerShell (Admin Mode):**
```sh
choco install pulumi
```
> *Ensure PowerShell is running as an administrator to avoid installation errors.*

### **2. Configure IAM Roles**
1. Log in to AWS **IAM Console** → Create a new user (**pulumi-deploy-user**).
2. Attach **AdministratorAccess** and **AmazonS3FullAccess** policies.
3. Download the **Access Key ID** and **Secret Access Key**.
4. Run the following command in **VS Code Terminal**:
```sh
aws configure
```
5. Enter the required AWS credentials.

### **3. Set Up Pulumi**
Authenticate with Pulumi Cloud:
```sh
pulumi login
```
Initialize a new **Pulumi AWS project**:
```sh
pulumi new aws-python
pip install pulumi pulumi-aws
```

---

## **Deploying the Static Website**

1. **Create a Directory for Website Files**
   - Download and extract the website template.
   - Move extracted files into the `website` directory.

2. **Update `__main__.py`**
   - Replace its content with the provided Pulumi Python script.

3. **Run Deployment Commands**
   - Preview deployment:
     ```sh
     pulumi preview
     ```
   - Deploy to AWS:
     ```sh
     pulumi up
     ```

> *If you encounter issues, ensure S3 Block Public Access is disabled.*

---

## **Accessing the Deployed Website**

- **CloudFront URL:** [https://d3hiuxztivmq3z.cloudfront.net/index.html](https://d3hiuxztivmq3z.cloudfront.net/index.html)
- **S3 Bucket URL:** [http://static-website-bucket-3167d8f.s3-website-us-east-1.amazonaws.com/](http://static-website-bucket-3167d8f.s3-website-us-east-1.amazonaws.com/)

---

## **Key Takeaways**

- Pulumi simplifies **cloud infrastructure automation**.
- AWS **S3 + CloudFront** enables scalable, secure, and cost-effective hosting.
- **Proper IAM role configuration** and **public access settings** are crucial for a seamless deployment.

---

### **Happy Deploying! 🚀**
