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

## Assignment 3 - Final Project: Google Dataflow and Google Big Query Data Manipulation <a name="Assignment3"></a> -<a href="https://github.com/ReedOlm/CS4843/tree/main/CloudFormationDeployment">Link to Repository</a>
### Creation of a Dataflow and Big Query Pipeline to Manipulate Data (Line Counting)
<ul>
  <li>Using Cloud terminal we plugged in and executed our Java functions (files found in repository for reference)</li>
  <li><a href="https://drive.google.com/drive/folders/1J596Fjr2qEkI7WR1pLcxc1a0G233ykyX?usp=sharing">Video Demonstration Link</a></li>
  <li>Images of our Dataflow data pipeline charts setup:</li>
  
  ![architectureDiagram](/CloudFormationDeployment/architectureDiagram.PNG)
  
  ![architectureDiagram](/CloudFormationDeployment/architectureDiagram.PNG)
  
  ![architectureDiagram](/CloudFormationDeployment/architectureDiagram.PNG)
  
  <li><a href="https://console.cloud.google.com/storage/browser/_details/dataflow-cloudcomputingdataflow/linecount-00000-of-00001;tab=live_object?project=cloudcomputingdataflow">Google Cloud Storage Link, displaying data AFTER data is piped through Dataflow</a></li>
  <li><a href="https://storage.cloud.google.com/dataflow-cloudcomputingdataflow/linecount-00000-of-00001?_ga=2.228040859.-720083893.1649035167&_gac=1.258673528.1649045030.CjwKCAjwi6WSBhA-EiwA6Niok6GATVCoGJBljVJ8VtvwJfeyLIj5qKI0BZwgwkA3wEPyMWkrgm4RLhoC4RIQAvD_BwE">Verification that Google Dataflow successfully uploaded our data passed in from our Java script</a></li>
  <li>NOTE!! The link above will take users to a webpage containing an output stored in our Google Cloud Storage. The output should read 5525, indicating that our Java function has worked correctly, piped the output through Google Dataflow and successfully stored it in our Cloud Storage. The Google Cloud project will be deleted on June 15 as not overuse data on service.</li>

</ul>
