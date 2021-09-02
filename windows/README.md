# Windows Tips
### Debug SHA-1 & SHA-256 key
`keytool -list -v -keystore "%USERPROFILE%\.android\debug.keystore" -alias androiddebugkey -storepass android -keypass android`
