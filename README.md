<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)

**Author:** mambotimothy25@gmail.com  
**Email:** mambotimothy25@gmail.com

---

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use S3 to host a static website. I'm doing this project to learn about AWS and cloud services and how they can be used to store objects in the cloud and even host websites.

### Tools and concepts

Amazon S3 stands for Amazon Simple Storage Service. The primary service on AWS for storing object files.

### Time, challenges, and wins

Amazon S3 was the primary storage service used for storing the index.html files and the NextWork-Everyone...love_files.

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open up S3 and then create a storage space inside to start storing website files.

### How long it took to create the bucket

Creating an S3 bucket took me less than five minutes.
I needed to learn a few new concepts like block public access and ACLs. 
But once that learning is done, I can create buckets in even shorter time in the future.

### Region selection

The Region I picked for my S3 bucket was Asia Pacific(Mumbai) ap-south-1 because the closest Region to where I live is in Africa (South Africa) af-south-1, which is unfortunately not supported for my account. Its best practice to pick the region closest to you because it lowers time to retrieve your things aka (latency) and costs although this is not important for this project. Nonetheless, best practice to keep.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two Amazon S3 buckets in the entire world can have the same name. They have to be completely unique regardless of the Region or the account ID.  
When you create a bucket, no other AWS account in the entire world can use your bucket's name unless you decide to delete the bucket.

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_ba6d42ad)

## Upload Website Files to S3

### What I did in this step

In this step, I will upload the website files into our S3 bucket.
This is important because no files equals no website.
Our bucket is still empty. I need to get files inside so that have a website to host.

### Files I uploaded

I uploaded two files to my S3 bucket- they were:
1.) Index.html file
This determines the structure i.e., what goes inside your website 
2.) NextWork - Everyone should be in a job they love_files
A folder of images and assets. This wil fill in the website with images and things to look at. 

I had to upload both files and folders into S3.

### How the files work together

Both files are necessary for this project as the index.html determines the structure, but the structure alone does not illustrate the contents of the website i.e, if index.html says insert image here. It might not have the actual image to display. You need to supply that image separately. That's why we have multiple files uploaded, the index.html file to direct what is inside the website page, but also a bunch of assets like images that the website is trying to display.

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_a265af88)

## Static Website Hosting on S3

### What I did in this step

In this step, I will.make mywebsite available to the world. This is called static website hosting and it is important because our website files will stay as just files and not turn into a website without the step. If we don't do the step.

### Understanding website hosting

Website hosting means putting our website files on a web server, which is a computer designed to turn the files into a website page that people can visit.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went into the properties tab of my bucket enabled static website hosting and I also labeled index.html as my I index document i.e., this is the document that I am trying to host.

### Access Control Lists (ACLs)

An ACL is a way to configure permission settings inside a bucket. 
For this particular project, I enabled ACLs so that I can control access to my website files later.
ACLs; there was a pop-up mentioning that AWS recommends disabling ACLs but we'll keep it enabled to learn how ACLs work and compare it with bucket policies later. 

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_c22c54c0)

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is a URL that takes you and anyone on the internet to the website that you're hosting.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an error is called 403 forbidden error. 
The reason for this error was that objects in a bucket are public by default, even though I'veswitched off block all public access. The website files themselves are still completely private.
I need to manage their access settings separately. They need to be public files too for the public to see the contents of our website.

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_22ce4daf)

## Success!

### What I did in this step

In this step, I will go into the files that I've uploaded into my bucket and make them public too, because this will enable me to actually view the contents of my website. Once that's done, my website is officially live! 

### How I resolved the 403 error

To resolve this connection 403 forbidden error, I updated the access settings of the files inside my bucket too. 
Using ACLs, I made my buckets file public. 
Once I checked my S3 bucket endpoint, I can see a webpage all loaded up.

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Bucket Policies

### What I did in this extension

In this project extension I'm about to. use bucket policies to control access to my bucket files. I'm doing this so that I can stop people from deleting the objects inside the file.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are rules that determine who is allowed or not allowed to do something. 
The benefit of using bucket policies is that you can have even greater control of the access of the actions or of the actions that people are or aren't allowed to do.
 While ACLs are useful for individual access for controlling individual access i.e. ACLs are useful for controlling public access to idividual objects inside the bucket.

![Image](https://nextwork.ai/serene_orange_proud_wolf/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_sm2sm2sm)

### What my bucket policy does

My bucket policy denies everyone from deleting my index.html file in the bucket. I tested this by trying to delete index.html and I saw a permission denied error.
This means my bucket policy worked. It successfully stopped me from deleting this object we wanted to protect.

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)*
