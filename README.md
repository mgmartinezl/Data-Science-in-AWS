# Research-topic: Services for data science at AWS

Written by:  
**Jose Carlos Badillo**   
**Gabriela Martinez**  

## Introduction: what is *_data science_* and why is it important?
Defining what data science is, is still a non-trivial task. One could say that this concept is related to the discipline of building smart applications that leverage the power of statistics, computer science and specific domain knowledge and produce valuable outputs from data. With regards to this, Mike Driscoll's, CEO of Metamarket, says:  
  
> _"Data science, as it’s practiced, is a blend of Red-Bull-fueled hacking and espresso-inspired statistics._  
  
> _But data science is not merely hacking—because when hackers finish debugging their Bash one-liners and Pig scripts, few of them care about non-Euclidean distance metrics._  
  
> _And data science is not merely statistics, because when statisticians finish theorizing the perfect model, few could read a tab-delimited file into R if their job depended on it._  
  
> _Data science is the civil engineering of data. Its acolytes possess a practical knowledge of tools and materials, coupled with a theoretical understanding of what’s possible"._

The previous is a very illustrative definition of data science that leads us to think that in the end, data science is a science but also an art, in which the so well-known _data scientists_ **know more about statistics than a computer scientist and more about computer hacking than a statistician.** [See more at [1]](https://www.oreilly.com/library/view/doing-data-science/9781449363871/ch01.html)

Approximately by 2016, the _data scientist_ position was considered as the "sexiest" job of the 21st century. Apparently, this new role was top in many aspects: scarse, interesting and well-paid. But, why was that figure so important? and ultimately, why is the concept of **data science** so important? In a nutshell, data science matters because it helps us make better decisions and be more accurately prepared for the future. If we simply think about evolution, information leads to better decisions, and better decisions will make species live longer. As for a cooking recipe, a data scientist would be a chef that gathers and mix a set of previously well-known ingredients to produce new or better food. 

As a consequence, data science is the extension of the scientific method applied to data in almost all fields of knowledge. From movies recommendations, fraud detection and financial risk prediction to preventive maintenance, data science has appeared to help us transform data into useful information, which in the end means increased wisdom. The following chart presents some key opportunities that data science offers to many of companies' current challenges:
  
![DS](https://github.com/mgmartinezl/Research-topic/blob/master/DataScience-UseCases.png)  
[Taken from: [2]](https://www.edureka.co/blog/what-is-data-science/)

Therefore, as may be expected, tech leader companies around the world have been working hard on the democratization of this concept, so that many other businesses and corporations can benefit themselves by making better decisions through data. In fact, data science is a business in which useful knowledge is sold as the most valuable product, something that most companies are willing to pay, as we are now aware of the fact that wrong decisions cost much more in the long term. [See more at [3]](https://www.forbes.com/sites/falonfatemi/2016/09/28/the-true-cost-of-a-bad-hire-its-more-than-you-think/#421ce09d4aa4)

**Amazon Web Services in the era of _data science_**  
Amazon Web Services is a whole ecosystem hosted by Amazon Inc. that offers on-demand cloud computing platforms to individuals, companies and governments through a pay-as-you-go basis. Also known as "AWS", this framework makes possible for its customers to access a variety of services in which data science utilities are included. The purpose of this brief repository is to approach the main products that AWS has disposed to perform _data science_, a concept that for the scope of this project will gather the following key topics:
  
* Data lakes
* Data analytics
* Machine learning
* Artificial intelligence

## 1. Data lakes, machine learning and analytics on top of AWS

AWS offers a set of services that allow companies create an environment that is able to process heterogeneous data and apply machine learning or analytics on it, as shown in the following schema:

![AWSStack](https://github.com/mgmartinezl/Research-topic/blob/master/DataLake-ML-Analytics-AWS.PNG)  
[Taken from: [4]](https://aws.amazon.com/big-data/datalakes-and-analytics/)

In the following sections, we will approach the different stages that the previous environment covers.

### 1.1. Data movement
Using AWS services for analytics or machine learning, requires first having the data in a centralized repository, called _lake_, which is located in the AWS cloud. Building a lake, however, is a further step that can only be completed once the data coming from different sources has been moved to the cloud. Therefore, AWS offers a comprehensive set of tools to perform data movement, depending on if the data needs to be processed in real-time or in batch.

#### 1.1.1. On-premises data movement
* [AWS Direct Connect](https://aws.amazon.com/directconnect/) solution aims to establish a dedicated network connection between local premises and the AWS cloud. This connection uses the standard 802.1q VLANs and hence can be partitioned into multiple virtual interfaces, which allows the access to both public and private resources through different IPs. This solutions works as follows:

![AWSDC](https://github.com/mgmartinezl/Research-topic/blob/master/AWS-Direct-Connect.png)

* [AWS Snowball](https://aws.amazon.com/snowball/) is a data transport solution for data in the scale of petabytes. According to AWS Snowball official website, _"customers today use Snowball to migrate analytics data, genomics data, video libraries, image repositories, backups, and to archive part of data center shutdowns, tape replacement or application migration projects"_. By creating a job in the AWS Management Console, a Snowball device will be shipped to the customer address, and no code or hardware purchasing is required. The whole process works as follows:

![AWSSnowball](https://github.com/mgmartinezl/Research-topic/blob/master/AWS-Snowball.png)

* Similarly, [AWS Snowmobile](https://aws.amazon.com/snowmobile/?nc2=h_m1) is a data transport solution built for an exabyte-scale. Each snowmobile (a 45-foot long ruggedized shipping container, pulled by a semi-trailer truck) can transfer up to 100PB, which makes easy _"to move massive volumes of data to the cloud, including video libraries, image repositories, or even a complete data center migration"_. AWS Snowmobile requires local installation and configuration by AWS experts. After setting up the connection and the network, data can be imported into Amazon S3 or Amazon Glacier.

#### 1.1.1. Real-time data movement
* [Amazon Kinesis](https://aws.amazon.com/kinesis/?nc2=h_m1) is a tool to collect, process and analyze streaming data in a real-time basis, _"such as video, audio, application logs, website clickstreams, and IoT telemetry data for machine learning, analytics, and other applications"_. It works as follows:

![Kinesis](https://github.com/mgmartinezl/Research-topic/blob/master/Amazon-Kinesis.png)

* [AWS IoT Core](https://aws.amazon.com/iot-core/?nc2=h_iot) is aanother real-time data capturing solution that focuses on Internet of Things devices data. This tool can connect billions of devices between them and also to other external endpoints or devices that use additional AWS services, such as AWS Lambda, Amazon Kinesis, Amazon S3, Amazon SageMaker, Amazon DynamoDB, Amazon CloudWatch, AWS CloudTrail, and Amazon QuickSight. Additionally, these apps can track the connected devices 100% of the time, even if they are not connected because the app _"stores the latest state of a connected device so that it can be read or set at anytime, making the device appear to your applications as if it were online all the time"_. The logic behind this concept is as shown:

**First, connect devices:**
![Connect](https://github.com/mgmartinezl/Research-topic/blob/master/AWS-IoT-connect.png)

**Second, secure connections and data:**
![Secure](https://github.com/mgmartinezl/Research-topic/blob/master/AWS-IoT-secure.png)

**Third, process collected data** according to predefined business rules:
![Process](https://github.com/mgmartinezl/Research-topic/blob/master/AWS-IoT-process.png)

### 1.2. Data lakes

#### 1.2.1. Object storage

#### 1.2.2. Backup and archive

#### 1.2.3. Data catalog

### 1.3. Analytics

#### 1.3.1. Interactive analytics

#### 1.3.2. Big data processing

#### 1.3.3. Data warehousing

#### 1.3.4. Real-time analytics

#### 1.3.5. Operational analytics

#### 1.3.5. Visualization

### 1.4. Machine learning

## 2. Artificial intelligence on top of AWS
