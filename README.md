AWS Integration with AI Application

Overview

This repository contains code that integrates an AI application with AWS cloud services. The AI application is designed to launch EC2 instances on AWS using hand gestures detected by a webcam. This README provides an overview of the code and instructions for setting up the environment.

Prerequisites
Before running the code, ensure you have the following prerequisites in place:

Python and Libraries: Make sure you have Python 3.x installed on your system. Additionally, you will need the following Python libraries:

boto3: The AWS SDK for Python to interact with AWS services.
cv2: OpenCV for capturing webcam images and video processing.
cvzone: The HandTrackingModule from cvzone for hand gesture recognition.
You can install these libraries using pip:

pip install boto3 opencv-python-headless cvzone


AWS Credentials: Configure your AWS credentials properly to allow access to EC2 services. You can set up your AWS credentials by creating a ~/.aws/credentials file or by configuring environment variables.

Code Structure
The code is organized as follows:

aws_ai_integration.py: Python script that captures webcam images, performs hand gesture recognition, and launches EC2 instances on AWS based on detected gestures.
cvzone/HandTrackingModule.py: A module from the cvzone library used for hand tracking and gesture recognition.
Usage
Run the aws_ai_integration.py script to start the webcam and detect hand gestures.

python aws_ai_integration.py

Perform hand gestures as follows:

All Fingers Up: Launch 5 EC2 instances simultaneously.
Index Finger Up: Launch 1 EC2 instance.
Index and Middle Fingers Up: Launch 2 EC2 instances.
Other Gestures: No action.
Ensure that you have the necessary AWS IAM permissions to create EC2 instances. Adjust your AWS IAM role and permissions as needed.

AWS Configuration
To use this code with your AWS account, you'll need to modify the AWS configuration within the aws_ai_integration.py script. Update the following variables:

ImageId: The ID of the Amazon Machine Image (AMI) you want to use for the EC2 instances.
InstanceType: The EC2 instance type to launch.
AWS credentials: Ensure that your AWS credentials are correctly configured, either via the ~/.aws/credentials file or environment variables.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
The hand tracking and gesture recognition functionality are based on the cvzone library.

