aws cloudformation create-stack --stack-name network stack --region us-east-1 --parameter file://network-parameter.json --template-body file://network.yml
# For creating Network stack and Server Stack. Note: Create the Network stack first before creating the server stack. Check cloud formation events to see what is happening.

aws cloudformation create-stack --stack-name server stack --region us-east-1 --parameter file://server-parameter.json --template-body file://server.yml
# For creating server stack
aws cloudformation create-stack --stack-name network stack --region us-east-1 --parameter file://network-parameter.json --template-body file://network.yml
# For creating network stack
