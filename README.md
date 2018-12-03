## EKS Kubernetes Events to Slack


**Ref :** https://github.com/bitnami-labs/kubewatch


### Instructions


#### 1. Create Slack Bot and Generate API Token

 - Create Slack bot  [https://my.slack.com/services/new/bot](https://my.slack.com/services/new/bot)
 - Set an username for your slack-bot
 - Note down **API Token** starts with **xoxb** 
 - Customize your slack-bot
	 - 	  Restrict API Token Usage - Better to restrict access to your Cluster Egress IP Addresses
- Invite slack-bot to your NOC slack Channel ( */join @slack-bot-name* )


#### 2. Setup Kubewatch

 - Clone git repository

    git clone https://github.com/dijeesh/eks-kubewatch.git

 - Edit ConfigMap and update your channel / API Token details

    channel: YOUR-CHANNEL
    token: SLACK-BOT-TOKEN

 - Apply configurations

     kubectl apply -f .

 
Done, you will now start getting Slack notificatiosn for Kubernetes Events.
