# Resume Updater


##Summary

I put together a tool that will automatically update my resume hosted on AWS S3 platform with the local copy of my resume.

Tech stack:
-  Python3
- boto3 python module
- when-changed(https://github.com/joh/when-changed) python module
- Unix ampersand background processor

## Installation

- Make sure you have your S3 config file setup https://docs.aws.amazon.com/cli/latest/userguide/cli-config-files.html
- Make sure you put your twilio creds in the config.ini file
- ``` git clone https://github.com/mababio/python_stuff.git ```
- Navigate to resume_updater directory
- ``` python3 setup.py install ```
- ``` pip3 installhttps://github.com/joh/when-changed/archive/master.zip ```

## Usage

- Run this  ``` when-changed [FILE_Trigger] -c 'resume_updater [FILE_TO_Upload]' & ```

- And any changes made to  ``` [FILE_Trigger]``` will trigger ``` [FILE_TO_Upload] ``` to be uploaded

- So to have your resume automatically updated in S3, you'll need to make the ``` [FILE_Trigger]``` be the resume file as well as ```[FILE_TO_Upload]```
