- CloudFormation has no awareness of any bootstrapping process which occurs on EC2 instance.

- Update with **disruption**: instance is going to be stopped and then started.
Instance will lose its public IPv4 address

- cloud-init-output is good for diagnosing normal bootstrapping using user data

cfn-init-command.log and cfn-init.log are good for diagnosing cfn-init processes