# XiaomiCleaner
Magisk module to remove some useless apps from Xiaomi K20 Pro Global ROM.

## Why?
The current K20 Global ROM has some leftover WiFi debugging which runs `tcpdump` on all interfaces (!) and logs your traffic to `/data/vendor/wlan_logs`, plus a diagnostic `cnss_diag` service which also generates excessive logging and uses CPU time.

This module replaces the `tcpdump` and `cnss_diag` binaries with a no-op script. It also removes the following system apps which do nothing useful for me.

```
/system/app/XiaomiServiceFramework
/system/app/HybridPlatform
/system/app/HybridAccessory
/system/app/facebook-appmanager
/system/app/Netflix_activation
/system/app/XMSFKeeper
/system/app/MiPicks
/system/app/YouDaoEngine
/system/app/AnalyticsCore
/system/app/SoterService
/system/app/Joyose
/system/priv-app/facebook-installer
/system/priv-app/facebook-services
```
