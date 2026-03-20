# How to create S3 Bucket & Static Website

## Steps
1. S3 → Create bucket. Name: cloudgrind-site-YOURNAME. Region: ap-south-1. Unblock public access.
2. Upload a simple index.html file. Set object ACL or bucket policy to allow public read.
3. Enable Static Website Hosting under Properties. Note the endpoint URL.
4. Open the URL — your site is live. Set up a bucket policy: s3:GetObject for *.
5. Explore versioning — enable it, upload same file again, view versions.


## Error 
- Mainly in bucket policy so check you fill the name in the bucket policy which is inside the permission.