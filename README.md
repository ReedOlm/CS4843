# CS4843 - A Repository Dedicated to Hosting My Assignments

## Table of Contents
[Assignment 0](#Assignment0)</br>
[Assignment 1](#Assignment1)</br>
[Assignment 2](#Assignment2)</br>
[Assignment 3](#Assignment3)

## Assignment 0 - basicCICD <a name="Assignment0"></a> - <a href="https://github.com/ReedOlm/CS4843/tree/main/basicCICD">Link to Repository</a>
### Establishing repository, virtual development environment in Cloud9, intro CI/CD

## Assignment 1 - KittiesOfTheWeek <a name="Assignment1"></a> - <a href="https://github.com/ReedOlm/CS4843/tree/main/KittiesOfTheWeek">Link to Repository</a>
### Static Cloudfront website using S3 bucket for hosting files
<ul>
  <li>Using basic html and css, created a static website to host pictures and videos of my cats</li>
  <li>Set up private S3 Bucket to store all site files.</li>
  <li>Launched Cloudfront distribution and pointed to the bucket as an origin</li>
  <li>Allowed HTTP GET/HEAD requests for site</li>
  <li>Set up IAM user group as best practice</li>
  <li>Used personal domain and AWS Certificate Manager to host Cloudfront distribution on my domain</li>
  <li>Set CNAMEs to point my domain to Cloudfront</li>
  <li>Personal domain that hosts Cloudfront site: https://www.reedolm.com</li>
</ul>

## Assignment 2 - Cloudformation Stack YAML Deployment <a name="Assignment2"></a> - <a href="https://github.com/ReedOlm/CS4843/tree/main/CloudFormationDeployment">Link to Repository</a>
### Creation of a Stack Using Cloudformation and AWS cli
<ul>
  <li>Using a bash script and the AWS cli, deployed 3 different stacks</li>
  <li>Deployed a scalable network framework using a YAML template, that split the us-east-1 servers into private/public subnets using CIDR</li>
  <li>This network framework included 2 VPCs, an InternetGateway, the aforementioned Subnets, a NAT with elastic ip's, and routing tables.</li>
  <li>Deployed a loadbalancing private webserver using a YAML template, with a configurable JSON parameter file to the 2 previously created us-east-1 private subnets using my own AMI/key values</li>
  <li>Created a final EC2 instance as a public Jumpbox inside of the VPC created for the network, and passed it the required keys to allow my personal computer's IP address to SSH into the jumpbox, then was able to ssh into both of my private EC2 servers</li>
  <li>Here is my drawing of what this system essentially looks like when fully deployed. (Has been taken down to avoid being charged by Amazon.):</li>
  ![architectureDiagram](/CloudFormationDeployment/architectureDiagram.PNG)

</ul>

## Assignment 3 - To Be Announced <a name="Assignment3"></a> - 
![Uploading architectureDiagram.PNG…]()
