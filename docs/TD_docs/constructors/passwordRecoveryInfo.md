---
title: passwordRecoveryInfo
description: Contains information available to the user after requesting password recovery
---
## Constructor: passwordRecoveryInfo  
[Back to constructors index](index.md)



Contains information available to the user after requesting password recovery

### Attributes:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|recovery\_email\_pattern|[string](../types/string.md) | Yes|Pattern of email to which recovery mail was sent|



### Type: [PasswordRecoveryInfo](../types/PasswordRecoveryInfo.md)


### Example:

```
$passwordRecoveryInfo = ['_' => 'passwordRecoveryInfo', 'recovery_email_pattern' => 'string'];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "passwordRecoveryInfo", "recovery_email_pattern": "string"}
```


Or, if you're into Lua:  


```
passwordRecoveryInfo={_='passwordRecoveryInfo', recovery_email_pattern='string'}

```


