# CloudFront CDN
⬡ Put CloudFront in front of your S3 static site. Enable HTTPS, understand caching and edge locations.

## STEPS

1. CloudFront → Create Distribution. Origin: your S3 website endpoint.
2. Default cache behaviour: Redirect HTTP to HTTPS. Set default root object: index.html.
3. After deploy (~5 mins): use the CloudFront domain — your site loads over HTTPS from edge.
4. Check Response Headers — see X-Cache: Hit from cloudfront on second load.
5. Create an Invalidation for /* — clears all cached content at edges.