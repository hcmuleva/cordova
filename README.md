** Below list of commands **
1. Create Cordova project
    cordova create emeelanmast com.emeelan.mastjod emeelanmast
 2. cordova platform add android
 3. build project and copy dist/build to www folder.
 4. cordova build android --release
 5. Generate keytool
    keytool -genkey -v -keystore emeelanmast -alias emeelanmast -keyalg RSA -keysize 2048 -validity 10004

  6. jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore emeelanmast.keystore /Users/harishmuleva/projects/social/emeelanrefactor/release/emeelanmast/platforms/android/app/build/outputs/bundle/release/app-release.aab emeelanmast
 7. zipalign -v 4 app-release.aab emeelanmast

 8. It will require some std size of images.
 9. 
