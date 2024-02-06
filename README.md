# device-uuid-liq
Simple browser device uuid generation plugin. Reworked to avoid build bugs.

## Installation

```bash
 $ yarn add device-uuid-liq
```

## Usage overview

```javascript
import UUID from 'device-uuid-liq';

const uuid = UUID.get();
```

#### Execute the plugin:
as a result example:
```
    e9dc90ac-d03d-4f01-a7bb-873e14556d8e
```

custom device uuid generation:
```javascript
const du = UUID.parse();
    const dua = [
        du.language,
        du.platform,
        du.os,
        du.cpuCores,
        du.isAuthoritative,
        du.silkAccelerated,
        du.isKindleFire,
        du.isDesktop,
        du.isMobile,
        du.isTablet,
        du.isWindows,
        du.isLinux,
        du.isLinux64,
        du.isMac,
        du.isiPad,
        du.isiPhone,
        du.isiPod,
        du.isSmartTV,
        du.pixelDepth,
        du.isTouchScreen
    ];
    const uuid = du.hashMD5(dua.join(':'));
```


module provides details such as the following:

```js
{
  "isMobile":false,
  "isDesktop":true,
  "isBot":false,
  .....
  "browser":"Chrome",
  "version":"17.0.963.79",
  "os":"Windows 7",
  "platform":"Microsoft Windows",
  "source":"Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/535.11 (KHTML, like Gecko) Chrome/17.0.963.79..."
}

```

### LICENSE

[MIT](LICENSE)
