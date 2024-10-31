## Note
This PHP project implements Tencent-RTC's UserSig authentication, providing a secure server-side method for generating signatures to protect the keys from leakage.

![](https://cloudcache.intl.tencent-cloud.com/cms/backend-cms/12569f72920411ef810152540055f650.png)


## Integration
You can use composer or source code integration.

#### composer integration
``` json
{
  "require": {
    "tencent/tls-sig-api-v2": "1.0"
  }
}
```

#### source code integration
Download `TLSSigAPIv2.php` to the project.

### Usage
``` php
<?php

require 'vendor/autoload.php'
// require_once "../src/TLSSigAPIv2.php"; // Source code integration uses relative paths

$api = new \Tencent\TLSSigAPIv2(1400000000, '5bd2850fff3ecb11d7c805251c51ee463a25727bddc2385f3fa8bfee1bb93b5e');
$sig = $api->genUserSig('xiaojun');
echo $sig . "\n";
```
