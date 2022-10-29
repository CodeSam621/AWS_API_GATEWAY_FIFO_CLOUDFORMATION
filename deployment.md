    
### Tempalate

```powershell
#set($dedupId = $context.requestId)
#set($groupId = $input.json('$.data.jobNumber'))
Action=SendMessage&MessageBody=$input.body&MessageGroupId=$groupId&MessageDeduplicationId=$dedupId
```

```powershell
#set($dedupId = $context.requestId)\n#set($groupId = $input.json('$.data.jobNumber'))\nAction=SendMessage&MessageBody=$input.body&MessageGroupId=$groupId&MessageDeduplicationId=$dedupId
```


## Deplyment script:

```powershell
sam deploy --stack-name mydemo-stack --template-file ./my_serverless.template --capabilities CAPABILITY_IAM  --parameter-overrides EnvironmentType=dev
```
