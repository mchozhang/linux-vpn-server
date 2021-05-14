# linux-vpn-server
deploy a vpn server (using pptp) on a linux system

## Using AWS cloudformation
prerequisite: 
* AWS account
* install aws-cli locally(optional, run the template on aws console if you don't)
* create your key pair for ssh login(optional)

```
aws cloudformation deploy \
 --template vpn-cloudformation.yaml \
 --stack-name vpn-stack \
 --parameter-overrides \
 KeyName=<your-keyname> \
 Username=<your-username> \
 VPNPassword=<your-password> \
 VPNPhrase=<your-phrase>
```

