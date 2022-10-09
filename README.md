<h1>Setup Cross Region S3 Bucket Replication</h1>

<h2>Description</h2>
In this project, my company has been hosting critical infrastructure files in a S3 bucket named appconfig-prod-1 within the us-east-1 region. Due to compliance requirements, the files remain stored in the United States, and must remain available even in the case of catastrophic disasters. To ensure the files remain accessible at all times, I will be setting up Cross-Region Replication to appconfig-prod-2 located in the us-west-2 region.<br />


<h2>Environments Used </h2>

- <b>AWS S3</b>

<h2>Project walk-through:</h2>

<p align="center">
Locate the current S3 bucket in us-east-1 named appconfig-prod-1: <br/>
<img src="https://imgur.com/v1hjrxT.png" height="80%" width="80%" />
<br />
<br />
Copy the name of the current bucket, create a new bucket changing the name to appconfig-prod-2 and selecting us-west-2 region:  <br/>
<img src="https://imgur.com/BcXCtWx.png" height="80%" width="80%"
<br />
<br />
From within the 'Bucket management' tab in the us-east-1 bucket, create a replication rule. We will enable bucket versioning, specify rule scope, and choose the destination for the replication rule which is the appconfig-prod-2 bucket: <br/>
<img src="https://imgur.com/0tTg3Kt.png" height="80%" width="80%"
<br />
<br />
<img src="https://imgur.com/L2K0J75.png" height="80%" width="80%"
<br />
<br />
Upload file to bucket to test replication: <br/>
<img src="https://imgur.com/nJtSpV2.png" height="80%" width="80%"
<br />
<br />
<img src="https://imgur.com/hoZpmBT.png" height="80%" width="80%"
<br />
<br />
The file has successfully replicated to appconfig-prod-2: <br/>
<img src="https://imgur.com/S9YpzJC.png" height="80%" width="80%"
<br />
<br />
