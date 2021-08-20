# Linux tips

## Enable sleep mode
```bash
   sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target
```


## Disable sleep mode
```bash
   sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
```

## Generate sha1 and sha-256
```bash
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android
```
