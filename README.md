# 🚀 AWS Amplify Static Website Hosting

## 📌 Project Overview

This project demonstrates how to deploy a **Static Website** using **AWS Amplify**. The website is built with **HTML** and **CSS** and hosted securely using **Amazon S3**, **AWS Amplify**, and **Amazon CloudFront**.

---

# 🏗️ Architecture

```text
                Developer
                    │
                    ▼
          HTML + CSS + Images
                    │
                    ▼
             AWS Amplify
                    │
                    ▼
              Amazon S3
                    │
                    ▼
          Amazon CloudFront
                    │
                    ▼
              Live Website
```

---

# 🛠️ Technologies Used

- AWS Amplify
- Amazon S3
- Amazon CloudFront
- HTML5
- CSS3

---

# 📁 Project Structure

```text
aws-amplify-project/
│
├── index.html
├── style.css
└── README.md
```

---

# 📄 index.html

```html
<!DOCTYPE html>
<html>
<head>
    <title>My AWS Amplify Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>Welcome to AWS Amplify</h1>

    <p>Website hosted using S3 and Amplify.</p>

</body>
</html>
```

---

# 🎨 style.css

```css
body{
    text-align:center;
    font-family:Arial;
}

h1{
    color:green;
}
```

---

# 🔐 AWS Amplify S3 Bucket Policy

AWS Amplify automatically creates and manages the required bucket policy for its managed S3 bucket.

```json
{
  "Version": "2008-10-17",
  "Statement": [
    {
      "Sid": "AllowAmplifyToListPrefix",
      "Effect": "Allow",
      "Principal": {
        "Service": "amplify.amazonaws.com"
      },
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::amplify-lab-09-06-26"
    },
    {
      "Sid": "AllowAmplifyToReadPrefix",
      "Effect": "Allow",
      "Principal": {
        "Service": "amplify.amazonaws.com"
      },
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::amplify-lab-09-06-26/*"
    },
    {
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::amplify-lab-09-06-26/*",
      "Condition": {
        "Bool": {
          "aws:SecureTransport": "false"
        }
      }
    }
  ]
}
```

> **Note:** This policy is automatically created and managed by AWS Amplify. The policy varies depending on your AWS account, application, and deployment branch.

---

# 🚀 Deployment Steps

### Step 1

Create an Amazon S3 bucket.

### Step 2

Upload your static website files:

- `index.html`
- `style.css`

### Step 3

Create a new application in AWS Amplify.

### Step 4

Choose your deployment method (GitHub or Amazon S3).

### Step 5

Deploy the application and wait for the build to complete.

### Step 6

Access the live website using the generated Amplify URL.

Example:

```text
https://main.xxxxxxxxx.amplifyapp.com
```

---

# ✨ Features

- Static Website Hosting
- Secure HTTPS Hosting
- Amazon S3 Integration
- CloudFront CDN
- Fast Deployment
- Responsive Design

---

# 📚 Learning Outcomes

- AWS Amplify Hosting
- Amazon S3
- Static Website Deployment
- HTML & CSS
- CloudFront CDN
- HTTPS Hosting
- S3 Bucket Policy
- Secure Static Asset Hosting

---

# 💡 Key Concepts

- AWS Amplify
- Amazon S3
- Amazon CloudFront
- Static Website Hosting
- Continuous Deployment
- HTTPS
- Bucket Policies

---

# 👨‍💻 Author

**Vipul Sharma**

**AWS | DevOps | Docker | Kubernetes | Terraform | Jenkins**
