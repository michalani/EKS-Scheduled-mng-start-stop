#  EKS-Scheduled-mng-start-stop

Example input via AWS CLI:

```
aws cloudformation update-stack --template-body file://main.yaml  --capabilities CAPABILITY_IAM --stack-name EKS-Scheduled-mng --parameters ParameterKey=ClusterName,ParameterValue=master-of-puppets-1 ParameterKey=ManagedNodeGroup,ParameterValue=mng3 ParameterKey=IncreaseByDesiredSize,ParameterValue=4 ParameterKey=DecreaseByDesiredSize,ParameterValue=0 ParameterKey=MorningCronSchedule,ParameterValue="cron(40 16 ? * MON-SUN *)" ParameterKey=EveningCronSchedule,ParameterValue="cron(43 16 ? * MON-SUN *)"A script to increase the MNG in the morning and decrease in the evening
```

A script to increase the MNG in the morning and decrease in the evening

Version: 2023.08.09
