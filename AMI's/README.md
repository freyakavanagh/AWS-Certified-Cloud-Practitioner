# EC2: AMI's

AMI = Amazon Machine Image

- They are a customization of an EC2 instance.
- Add our own software, configuration , OS, monitoring...
- Faster boot/config time because all the software is pre-packaged
- AMI's are built for a specific region (and can be copied across regions)

### You can copy EC2 instances from...
- A public AMI (AWS provided, the images we normally create instances from)
- Our own AMI: We make and maintain them ourselves
- An AWS Marketplace AMI: AMI made by someone else (potentially have to pay for it)

# Steps

1. Create instance with user data
2. Wait for the script to finish running
3. Select Image
4. Actions>Image and templates> create image
5. Wait for it to be made
6. We can then launch instances from the AMI
7. Remember to add code to AMI instance user data to start the programme