# ISOM 661
Summary notes from ISOM 661: Technology Bootcamp.

## R on the cloud using the AMI from class
I have shared an AMI as a 'Private Image' with every student from ISOM 661. It is equipped with an up to date version of RStudio server which you may use to run RStudio on your instance. 
* To find it go to EC2 in your AWS Console, then on the left hand side under Images click AMIs, and under the dropdown 'Owned by me' select 'Private Images'. You will see appear an image with the name Emory_R_AMI. Click 'Launch' to create a new instance using this image.
* Once your instance is running, in its description, copy the Public DNS (IPv4). Let's suppose it is
`ec2-54-173-90-61.compute-1.amazonaws.com`
for the remainder of this walk-through.
* Append :8787 to the end of the Public DNS of your instance and enter the address, for example https://ec2-54-173-99-67.compute-1.amazonaws.com:8787, in your browser address bar. If you used the correct address, then you will see the RStudio sign in page. Enter

user: ruser

password: Ch@ngeMe1

* Once RStudio opens, go to Tools, then Shell... At the command line, enter `passwd`. You will then be prompted to enter `(current) UNIX password:`. Enter Ch@ngeMe1. Then, you will be prompted for `New password:` and here you will enter whatever password you want to use for signing in to Rstudio on your instance. You should see output similar to what appears below.  
```
bash-4.2$ passwd
Changing password for user ruser.
Changing password for ruser.
(current) UNIX password: Change@Me1
New password: 
Retype new password: 
passwd: all authentication tokens updated successfully.
```
* When you are done using Rstudio, stop your instance so that you will not be charged for your instance. Whatever files you saved on your instance file system will persist, unless you delete the instance and the attached disk. Recall, after stopping your instance, you are still charged for storage of $0.10 per GB per month (the disk attached to the instance). The AMI is 30GB, which is included in the free tier. Note, 30GB is the current (08/31/2018) limit of free tier storage, see https://aws.amazon.com/free/ for details.


## AWS guides from class readings
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html
* https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instances-and-amis.html
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html
* https://aws.amazon.com/ec2/pricing/on-demand/


