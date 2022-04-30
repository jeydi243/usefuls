# Windows Tips

### Debug SHA-1 & SHA-256 key
`keytool -list -v -keystore "%USERPROFILE%\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android`
### Create a Keystore 
`keytool -genkey -v -keystore F:\Keystore\.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias < > -keypass upload -storepass `
