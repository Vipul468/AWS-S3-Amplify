# 🚀 AWS Amplify Static Website Hosting

## 📌 Project Overview

This project demonstrates how to host a static website using **AWS Amplify**. The website is built using **HTML**, **CSS**, and an image (`docker-compose-lab.png`). AWS Amplify provides secure, scalable, and high-performance hosting backed by Amazon S3 and Amazon CloudFront.

---

# 🏗️ Architecture

```
                Developer
                    │
                    ▼
        HTML + CSS + Image
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

```
aws-amplify-project/
│
├── index.html
├── style.css
├── docker-compose-lab.png
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

    <img src="docker-compose-lab.png" alt="Docker Compose Lab">

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

img{
    width:900px;
    max-width:100%;
    margin-top:20px;
}
```

---

# 🔐 AWS Amplify S3 Bucket Policy

AWS Amplify automatically creates and manages the required S3 bucket policy for the hosting bucket.

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

> **Note:** AWS Amplify automatically generates and manages this bucket policy. The exact policy differs for each AWS account, application, and branch.

---

# 🚀 Deployment Steps

### Step 1

Create an S3 bucket.

---

### Step 2

Upload the following files:

- index.html
- style.css
- docker-compose-lab.png

---

### Step 3

Create a new AWS Amplify application.

---

### Step 4

Deploy the website using AWS Amplify.

---

### Step 5

Wait for the deployment to complete.

---

### Step 6

Open the generated Amplify URL.

Example:

```
https://main.xxxxxxxxx.amplifyapp.com
```

---

# ✨ Features

- Static Website Hosting
- Responsive Web Page
- Image Display
- HTTPS Enabled
- CloudFront CDN
- Fast Deployment
- Secure Hosting

---

# 📷 Output

The hosted website displays:

- Welcome Message
- Static Web Page
- Docker Compose Architecture Image

---

# 📚 Learning Outcomes

- AWS Amplify Hosting
- Amazon S3 Integration
- Static Website Deployment
- HTML & CSS
- CloudFront CDN
- HTTPS Hosting
- AWS Bucket Policy
- Static Asset Hosting

---

# 💡 Key Concepts

- Static Website Hosting
- Amazon S3 Object Storage
- AWS Amplify Hosting
- CloudFront Content Delivery Network (CDN)
- Secure HTTPS Deployment
- AWS Managed Bucket Policies

---

# 👨‍💻 Author

**Vipul Sharma**

**AWS | DevOps | Docker | Kubernetes | Terraform | Jenkins**
