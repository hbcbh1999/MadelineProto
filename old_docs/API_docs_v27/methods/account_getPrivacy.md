---
title: account.getPrivacy
description: account.getPrivacy parameters, return type and example
---
## Method: account.getPrivacy  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|key|[InputPrivacyKey](../types/InputPrivacyKey.md) | Yes|


### Return type: [account\_PrivacyRules](../types/account_PrivacyRules.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $MadelineProto->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$account_PrivacyRules = $MadelineProto->account->getPrivacy(['key' => InputPrivacyKey, ]);
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - account.getPrivacy
* params - `{"key": InputPrivacyKey, }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/account.getPrivacy`

Parameters:

key - Json encoded InputPrivacyKey



Or, if you're into Lua:

```
account_PrivacyRules = account.getPrivacy({key=InputPrivacyKey, })
```

