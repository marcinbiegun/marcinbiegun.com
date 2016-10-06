---
layout: post
title: OmniFocus sync with Fastmail.fm using WebDAV
---

If you happen to use both OmniFocus nad FastMail, you can
store your encrypted OmniFocus data on FastMail servers. Besides email,
FastMail that also provides also a few other services, including WebDAV file
storage. WebDAV is availale on all paid plans.

Here's a quick tutorial how to set it up.

## Create safe FastMail app-password

Let's start with generating app-password for accessing WebDAV.

1. Sign to your FastMail account [https://www.fastmail.com/login](https://www.fastmail.com/login).

2. Go to "Settings" -> "Password & Security".

3. Under "App Passwords" section, click the "New App Password" button.

4. Select any "Device" type, in "Access" select "Files (FTP/WebDAV)".

5. Store the password temporarily, or just left the browser tab open for now.

## Connect OmniFocus on OSX

Let's sync the database from OSX client:

1. Open "Preferences".

2. In "Synchronization" tab select "Advanced (WebDAV)".

3. Put in this address: `https://webdav.fastmail.com/{{username}}/files/`, where `{{username}}`
   is your FastMail login, with "@" char replaced with ".", e.g. `mike.fastmail.fm`.

4. Click "Sync Now".

5. Your should be prompted for a password: use your FastMail login and
   the app-password previously generated.

6. If everything is fine, the app will successfully peform the first sync now.

7. Notice you didn't provide an encryption password yet - by default,
   OmniFocus uses the same password both for accessing WebDAV and as an
   key for encrypting the database.

   To set the ecnryption password, click "Show Sync Details...",
   go to  "Encryption" tab and set your encryption password there.

## Connect OmniFocus on iOS

1. Open "Settings" (pull down to find it), select "Sync Method" -> "Custom (WebDAV)"

2. Enter the same WebDAV credentials as previously on OSX: address, login and password.

3. If eveyrtihng went fine, you'll should be promptet for your encryption
   password.

## Sources:

* [OmniFocus OSX sync](https://support.omnigroup.com/documentation/omnifocus/mac/2.7/en/getting-synced)
* [OmniFocus iOS sync](https://support.omnigroup.com/documentation/omnifocus/ios/2.17/en/getting-synced)
* [FastMail WevDAV](https://www.fastmail.com/help/files/davnftp.html)

