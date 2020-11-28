## website
release url: https://yafei.woyangnia.com/  
git hub demo url: https://zspengyou.github.io/love/



## source 
original repo: https://github.com/arunboy/love  
original demo: https://arunboy.github.io/love/  

new repo: https://github.com/zspengyou/love  
new demo: https://yafei.woyangnia.com/  

## architecture

domain provider: https://www.godaddy.com/  

website architecture CloudFront+S3:
https://aws.amazon.com/premiumsupport/knowledge-center/cloudfront-serve-static-website/  

HTTPS certificate is using AWS ACM: https://aws.amazon.com/certificate-manager/  

**note**: 
current cache default time 24 hours, which means that the website will get updated 24 hours after we update the HTML/JS/CSS in S3 bucket.  


## task dashboard
https://trello.com/b/G6mWogIJ/jaywebsite


## website update/deploy

**update a folder**

```
aws --profile personalAccount s3 cp /Users/jayzho/jayWorkspace/jayzhoGithub/love/img s3://content.jiageiwoba.com/img --recursive
aws --profile personalAccount s3 cp /Users/jayzho/jayWorkspace/jayzhoGithub/love/script s3://content.jiageiwoba.com/script --recursive
aws --profile personalAccount s3 cp /Users/jayzho/jayWorkspace/jayzhoGithub/love/css s3://content.jiageiwoba.com/css --recursive

```

**update a file**

```
aws --profile personalAccount s3 cp /Users/jayzho/jayWorkspace/jayzhoGithub/love/index.html s3://content.jiageiwoba.com/index.html 
aws --profile personalAccount s3 cp /Users/jayzho/jayWorkspace/jayzhoGithub/love/img/1firework.jpg s3://content.jiageiwoba.com/img/1firework.jpg 
```



