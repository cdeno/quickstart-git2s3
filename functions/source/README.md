Instructions on how to build awscli into GitPullS3 module.

- Create EC2 Ubuntu 64bit
- ssh onto it
- $ sudo apt-get update && sudo apt-get install python-pip


And then follow:
https://alestic.com/2016/11/aws-lambda-awscli/

- Download the zip file using scp

This is the bundled python module that includes awscli

We can then merge in the GitPullS3 files into the root of the zip

E.g. `$ zip -X -r lambda.zip .`


Note:

Don't mess with the zip in a GUI. Use `zip` only to update the handler code.
Permissions can change using the gui


Resources
https://stackoverflow.com/questions/24849998/how-to-catch-exception-output-from-python-subprocess-check-output

https://stackoverflow.com/questions/43601226/how-can-i-run-the-aws-cli-in-an-aws-lambda-python-3-6-environment

https://github.com/alestic/aws-git-backed-static-website/blob/master/build-upload-aws-lambda-function

Alt

https://stackoverflow.com/questions/33513604/call-aws-cli-from-aws-lambda