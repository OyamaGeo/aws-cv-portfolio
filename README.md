# AWS Personal Portfolio Website

A personal portfolio website designed to showcase my professional profile, AWS certifications, cloud engineering projects, technical skills and CV.

The website is hosted on **Amazon S3** and delivered globally through **Amazon CloudFront**, using Origin Access Control (OAC) to securely connect CloudFront to a private S3 bucket.

## 🌐 Live Website

**[Visit My Portfolio](https://dz4l9g31rxi1e.cloudfront.net)**

## Project Overview

This project involved building and deploying a static portfolio website using AWS cloud services.

The primary goal was to gain practical experience with AWS storage, content delivery, access management and cloud deployment while creating an online professional presence.

## Architecture

```text
                 Website Visitors
                        |
                        v
                Amazon CloudFront
                 (HTTPS Delivery)
                        |
                        v
              Origin Access Control
                    (OAC)
                        |
                        v
                Amazon S3 Bucket
                 (Private Bucket)
                        |
          +-------------+-------------+
          |             |             |
       HTML Files    CSS Files     Images
          |
       CV PDF
```

## AWS Services Used

| AWS Service | Purpose |
| Amazon S3 | Stores website files and resources |
| Amazon CloudFront | Delivers website content through a global content delivery network |
| Origin Access Control (OAC) | Secures access between CloudFront and the private S3 bucket |
| S3 Bucket Policy | Grants the CloudFront distribution permission to retrieve website objects |

## Key Implementation Steps

1. Created an Amazon S3 bucket to store the portfolio website files.
2. Uploaded the website's HTML, CSS, images and CV PDF.
3. Configured an Amazon CloudFront distribution using the S3 bucket as its origin.
4. Configured Origin Access Control (OAC) to allow CloudFront to access the private S3 bucket.
5. Configured the S3 bucket policy to authorize the CloudFront distribution.
6. Set `index.html` as the default root object.
7. Used the default CloudFront domain with HTTPS.
8. Tested the homepage, CV page and downloadable CV document.

## Security Considerations

Security was an important part of this deployment.

- Kept the S3 bucket private.
- Used Origin Access Control (OAC) instead of making the bucket publicly accessible.
- Restricted S3 object access to the designated CloudFront distribution through a bucket policy.
- Used HTTPS through the default CloudFront domain.

## Technologies

- HTML5
- CSS3
- Amazon S3
- Amazon CloudFront
- AWS Origin Access Control
- Git
- GitHub

## Skills Demonstrated

- AWS S3 bucket configuration and object management.
- CloudFront distribution creation and configuration.
- Secure origin access using OAC.
- S3 bucket policy configuration.
- Static website deployment.
- Troubleshooting CloudFront and S3 access errors.
- Version control using Git and GitHub.

## Challenges and Lessons Learned

During deployment, I encountered an `AccessDenied` error when accessing the CloudFront distribution.

I investigated the S3 bucket policy, Origin Access Control configuration and default root object settings.

This troubleshooting process helped me understand how CloudFront communicates securely with a private S3 bucket and how to diagnose access-related deployment issues.

## Future Improvements

- Add direct links to individual GitHub project repositories.
- Improve website responsiveness and user experience.
- Add more AWS cloud engineering projects.
- Implement automated deployment using AWS CI/CD services.
