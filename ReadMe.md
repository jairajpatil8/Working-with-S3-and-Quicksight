<h1 align="center">Create a dashboard with AWS S3 and Quicksight</h1>
  

<B>PRE-REQUISITES</B>
  <br>

To complete this project, you will need the following: <br>
- AWS Account<br>
- IAM S3 Policy Attached to Your User<br>

<B>Step 1 — Login to your AWS console</B>
 <p align="center">
  <img width="600" src="https://github.com/jairajpatil8/Hosting-static-website-on-s3/blob/main/s3-images/login.png">
</p>

<b>Step 2 — Navigate to S3</b>
 <p align="center">
  <img width="600" src="https://github.com/jairajpatil8/Hosting-static-website-on-s3/blob/main/s3-images/s3.png">
</p>
<b>Step 3 - Click on Create Bucket</b>

- Enter Bucket Name<br>

- Select your Region<br>
  
- leave the rest to default and click Create Bucket<br>
<b>step 4 - upload Content</b>
- Replace your Bucket Name in manifest.txt file<br>
<p align="center">
  <img width="600" src="">
</p>
<b> Step 5 -  Add bucket Policy</b>
```diff
{
  "Version": "2012-10-17",
  "Statement": [
      {
          "Sid": "AllowQuickSightAccess",
          "Effect": "Allow",
          "Principal": {
              "Service": "quicksight.amazonaws.com"
          },
          "Action": [
              "s3:GetObject",
              "s3:ListBucket"
          ],
          "Resource": [
              "arn:aws:s3:::your-bucket-name",
              "arn:aws:s3:::your-bucket-name/*"
          ]
      }
  ]
}
```
<br>
- <b> Remember to replace your Bucket Name in "arn:aws:s3:::your-bucket-name",
  "arn:aws:s3:::your-bucket-name/*" </b><br>
  <b>Step 6 - Open Quicksight in a new Tab</b><br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Sign up for free trail <br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Enter you Details<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Enable IAM and S3 Roles<br>
  <p align="center">
    <img width="600" src="">
  </p>

  <b>step 7 - Quicksight Dashborad</b>
  <p align="center">
    <img width="600" src="">
  </p>
  - Navigate to datasets<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Click on S3<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Visulize <br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Interactive Sheet<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Drag brand in to sheet 1
  <p align="center">
    <img width="600" src="">
  </p>
  - Sort the data based on your metric<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - I am sorting the data to find the highest selling brand <br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Play around to create the optimal dashbord <br>
  <b>Step 8 - Remember to Cleanup to avoid charges</b>
  - Click the top right icon, select manage quicksight<br>
  <p align="center">
    <img width="600" src="">
  </p>
  - Account Settings, Account Termination <br>
  <p align="center">
    <img width="600" src="">
  </p>
 - confirm<br>



  






  