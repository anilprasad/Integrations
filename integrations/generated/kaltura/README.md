# @datafire/kaltura

Client library for Kaltura VPaaS

## Installation and Usage
```bash
npm install --save datafire @datafire/kaltura
```

```js
let datafire = require('datafire');
let kaltura = require('@datafire/kaltura').actions;

let account = {
  ks: "",
}
let context = new datafire.Context({
  accounts: {
    kaltura: account,
  }
})


kaltura.widget.list({}, context).then(data => {
  console.log(data);
})
```

## Description
The Kaltura VPaaS API

## Actions
### accessControl.add
Add new Access Control Profile


```js
kaltura.accessControl.add({}, context)
```


### accessControl.delete
Delete Access Control Profile by id


```js
kaltura.accessControl.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### accessControl.get
Get Access Control Profile by id


```js
kaltura.accessControl.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### accessControl.list
List Access Control Profiles by filter and pager


```js
kaltura.accessControl.list({}, context)
```


### accessControl.update
Update Access Control Profile by id


```js
kaltura.accessControl.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* accessControl[name] (string) - The name of the Access Control Profile
* accessControl[systemName] (string) - System name of the Access Control Profile
* accessControl[description] (string) - The description of the Access Control Profile
* accessControl[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* accessControl[restrictions] (array)

### accessControlProfile.add
Add new access control profile


```js
kaltura.accessControlProfile.add({}, context)
```


### accessControlProfile.delete
Delete access control profile by id


```js
kaltura.accessControlProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### accessControlProfile.get
Get access control profile by id


```js
kaltura.accessControlProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### accessControlProfile.list
List access control profiles by filter and pager


```js
kaltura.accessControlProfile.list({}, context)
```


### accessControlProfile.update
Update access control profile by id


```js
kaltura.accessControlProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* accessControlProfile[name] (string) - The name of the Access Control Profile
* accessControlProfile[systemName] (string) - System name of the Access Control Profile
* accessControlProfile[description] (string) - The description of the Access Control Profile
* accessControlProfile[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* accessControlProfile[rules] (array)

### adminUser.login
Get an admin session using admin email and password (Used for login to the KMC application)


```js
kaltura.adminUser.login({
  "email": "",
  "password": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* email (string) **required**
* password (string) **required**
* partnerId (integer)

### adminUser.resetPassword
Reset admin user password and send it to the users email address


```js
kaltura.adminUser.resetPassword({
  "email": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* email (string) **required**

### adminUser.setInitialPassword
Set initial users password


```js
kaltura.adminUser.setInitialPassword({
  "hashKey": "",
  "newPassword": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* hashKey (string) **required**
* newPassword (string) **required** - new password to set

### adminUser.updatePassword
Update admin user password and email


```js
kaltura.adminUser.updatePassword({
  "email": "",
  "password": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* email (string) **required**
* password (string) **required**
* newEmail (string) - Optional, provide only when you want to update the email
* newPassword (string)

### analytics.query
report query action allows to get a analytics data for specific query dimensions, metrics and filters.


```js
kaltura.analytics.query({}, context)
```


### annotation.add
Allows you to add an annotation object associated with an entry


```js
kaltura.annotation.add({}, context)
```


### annotation.addFromBulk
Allows you to add multiple cue points objects by uploading XML that contains multiple cue point definitions


```js
kaltura.annotation.addFromBulk({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**

### annotation.clone
Clone cuePoint with id to given entry


```js
kaltura.annotation.clone({
  "id": "",
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* entryId (string) **required**

### annotation.count
count cue point objects by filter


```js
kaltura.annotation.count({}, context)
```


### annotation.delete
delete cue point by id, and delete all children cue points


```js
kaltura.annotation.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### annotation.get
Retrieve an CuePoint object by id


```js
kaltura.annotation.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### annotation.list
List annotation objects by filter and pager


```js
kaltura.annotation.list({}, context)
```


### annotation.serveBulk
Download multiple cue points objects as XML definitions


```js
kaltura.annotation.serveBulk({}, context)
```


### annotation.update
Update annotation by id


```js
kaltura.annotation.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* annotation[entryId] (string) - `insertOnly`
* annotation[triggeredAt] (integer)
* annotation[tags] (string)
* annotation[startTime] (integer) - Start time in milliseconds
* annotation[partnerData] (string)
* annotation[partnerSortValue] (integer)
* annotation[forceStop] (integer) - Enum Type: `KalturaNullableBoolean`
* annotation[thumbOffset] (integer)
* annotation[systemName] (string)
* annotation[objectType] (string)
* annotation[parentId] (string) - `insertOnly`
* annotation[text] (string)
* annotation[endTime] (integer) - End time in milliseconds
* annotation[isPublic] (integer) - Enum Type: `KalturaNullableBoolean`
* annotation[searchableOnEntry] (integer) - Enum Type: `KalturaNullableBoolean`
* annotation[protocolType] (string) - `insertOnly`
* annotation[sourceUrl] (string)
* annotation[adType] (string) - Enum Type: `KalturaAdType`
* annotation[title] (string)
* annotation[duration] (integer) - Duration in milliseconds
* annotation[quizUserEntryId] (string) - `insertOnly`
* annotation[answerKey] (string)
* annotation[correctAnswerKeys] (array)
* annotation[code] (string)
* annotation[description] (string)
* annotation[eventType] (string) - Enum Type: `KalturaEventType`
* annotation[optionalAnswers] (array)
* annotation[hint] (string)
* annotation[question] (string)
* annotation[explanation] (string)
* annotation[assetId] (string)
* annotation[subType] (integer) - Enum Type: `KalturaThumbCuePointSubType`

### annotation.updateStatus
Update cuePoint status by id


```js
kaltura.annotation.updateStatus({
  "id": "",
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* status (integer) **required** - Enum Type: `KalturaCuePointStatus`

### appToken.add
Add new application authentication token


```js
kaltura.appToken.add({}, context)
```


### appToken.delete
Delete application authentication token by id


```js
kaltura.appToken.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### appToken.get
Get application authentication token by id


```js
kaltura.appToken.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### appToken.list
List application authentication tokens by filter and pager


```js
kaltura.appToken.list({}, context)
```


### appToken.startSession
Starts a new KS (kaltura Session) based on application authentication token id


```js
kaltura.appToken.startSession({
  "id": "",
  "tokenHash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - application token id
* tokenHash (string) **required** - hashed token, built of sha1 on current KS concatenated with the application token
* userId (string) - session user id, will be ignored if a different user id already defined on the application token
* type (integer) - Enum Type: `KalturaSessionType`
* expiry (integer) - session expiry (in seconds), could be overwritten by shorter expiry of the application token and the session-expiry that defined on the application token

### appToken.update
Update application authentication token by id


```js
kaltura.appToken.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* appToken[expiry] (integer) - Expiry time of current token (unix timestamp in seconds)
* appToken[sessionType] (integer) - Enum Type: `KalturaSessionType`
* appToken[sessionUserId] (string) - User id of KS (Kaltura Session) that created using the current token
* appToken[sessionDuration] (integer) - Expiry duration of KS (Kaltura Session) that created using the current token (in seconds)
* appToken[sessionPrivileges] (string) - Comma separated privileges to be applied on KS (Kaltura Session) that created using the current token
* appToken[hashType] (string) - Enum Type: `KalturaAppTokenHashType`

### aspera.getFaspUrl



```js
kaltura.aspera.getFaspUrl({
  "flavorAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* flavorAssetId (string) **required**

### attachmentAsset.add
Add attachment asset


```js
kaltura.attachmentAsset.add({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* attachmentAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* attachmentAsset[fileExt] (string) - `insertOnly`
* attachmentAsset[partnerData] (string) - Partner private data
* attachmentAsset[partnerDescription] (string) - Partner friendly description
* attachmentAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* attachmentAsset[filename] (string) - The filename of the attachment asset content
* attachmentAsset[title] (string) - Attachment asset title
* attachmentAsset[format] (string) - Enum Type: `KalturaAttachmentType`
* attachmentAsset[objectType] (string)
* attachmentAsset[accuracy] (number) - The accuracy of the transcript - values between 0 and 1
* attachmentAsset[humanVerified] (integer) - Enum Type: `KalturaNullableBoolean`
* attachmentAsset[language] (string) - Enum Type: `KalturaLanguage`
* attachmentAsset[providerType] (string) - Enum Type: `KalturaTranscriptProviderType`

### attachmentAsset.delete



```js
kaltura.attachmentAsset.delete({
  "attachmentAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* attachmentAssetId (string) **required**

### attachmentAsset.get



```js
kaltura.attachmentAsset.get({
  "attachmentAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* attachmentAssetId (string) **required**

### attachmentAsset.getRemotePaths
Get remote storage existing paths for the asset


```js
kaltura.attachmentAsset.getRemotePaths({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### attachmentAsset.getUrl
Get download URL for the asset


```js
kaltura.attachmentAsset.getUrl({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* storageId (integer)

### attachmentAsset.list
List attachment Assets by filter and pager


```js
kaltura.attachmentAsset.list({}, context)
```


### attachmentAsset.serve
Serves attachment by its id


```js
kaltura.attachmentAsset.serve({
  "attachmentAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* attachmentAssetId (string) **required**
* serveOptions[download] (boolean)
* serveOptions[referrer] (string)

### attachmentAsset.setContent
Update content of attachment asset


```js
kaltura.attachmentAsset.setContent({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* contentResource[objectType] (string)
* contentResource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[forceAsyncDownload] (boolean) - Force Import Job
* contentResource[assetId] (string) - ID of the source asset
* contentResource[entryId] (string) - ID of the source entry
* contentResource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[objectId] (string) - The object id of the file sync object
* contentResource[version] (string) - The version of the file sync object
* contentResource[resource][objectType] (string)
* contentResource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][assetId] (string) - ID of the source asset
* contentResource[resource][entryId] (string) - ID of the source entry
* contentResource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][objectType] (string)
* contentResource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][objectType] (string)
* contentResource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][resources] (array)
* contentResource[resource][resource][resource][content] (string) - Textual content
* contentResource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resource][resources] (array)
* contentResource[resource][resource][content] (string) - Textual content
* contentResource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resources] (array)
* contentResource[resource][content] (string) - Textual content
* contentResource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][privateKey] (string) - SSH private key
* contentResource[resource][publicKey] (string) - SSH public key
* contentResource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resources] (array)
* contentResource[content] (string) - Textual content
* contentResource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[privateKey] (string) - SSH private key
* contentResource[publicKey] (string) - SSH public key
* contentResource[keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[localFilePath] (string) - Full path to the local file
* contentResource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[fileData] (string) - Represents the $_FILE
* contentResource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### attachmentAsset.update
Update attachment asset


```js
kaltura.attachmentAsset.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* attachmentAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* attachmentAsset[fileExt] (string) - `insertOnly`
* attachmentAsset[partnerData] (string) - Partner private data
* attachmentAsset[partnerDescription] (string) - Partner friendly description
* attachmentAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* attachmentAsset[filename] (string) - The filename of the attachment asset content
* attachmentAsset[title] (string) - Attachment asset title
* attachmentAsset[format] (string) - Enum Type: `KalturaAttachmentType`
* attachmentAsset[objectType] (string)
* attachmentAsset[accuracy] (number) - The accuracy of the transcript - values between 0 and 1
* attachmentAsset[humanVerified] (integer) - Enum Type: `KalturaNullableBoolean`
* attachmentAsset[language] (string) - Enum Type: `KalturaLanguage`
* attachmentAsset[providerType] (string) - Enum Type: `KalturaTranscriptProviderType`

### attUverse.getFeed



```js
kaltura.attUverse.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### auditTrail.add
Allows you to add an audit trail object and audit trail content associated with Kaltura object


```js
kaltura.auditTrail.add({}, context)
```


### auditTrail.get
Retrieve an audit trail object by id


```js
kaltura.auditTrail.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### auditTrail.list
List audit trail objects by filter and pager


```js
kaltura.auditTrail.list({}, context)
```


### avn.getFeed



```js
kaltura.avn.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### baseEntry.add
Generic add entry, should be used when the uploaded entry type is not known.


```js
kaltura.baseEntry.add({}, context)
```


### baseEntry.addContent
Attach content resource to entry in status NO_MEDIA


```js
kaltura.baseEntry.addContent({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* resource[objectType] (string)
* resource[resource][objectType] (string)
* resource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][assetId] (string) - ID of the source asset
* resource[resource][entryId] (string) - ID of the source entry
* resource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][objectId] (string) - The object id of the file sync object
* resource[resource][version] (string) - The version of the file sync object
* resource[resource][resource][objectType] (string)
* resource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][objectType] (string)
* resource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][resources] (array)
* resource[resource][resource][resource][content] (string) - Textual content
* resource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resource][resources] (array)
* resource[resource][resource][content] (string) - Textual content
* resource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resources] (array)
* resource[resource][content] (string) - Textual content
* resource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][privateKey] (string) - SSH private key
* resource[resource][publicKey] (string) - SSH public key
* resource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][localFilePath] (string) - Full path to the local file
* resource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][fileData] (string) - Represents the $_FILE
* resource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resources] (array)
* resource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[forceAsyncDownload] (boolean) - Force Import Job
* resource[assetId] (string) - ID of the source asset
* resource[entryId] (string) - ID of the source entry
* resource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[fileSyncObjectType] (integer) - The object type of the file sync object
* resource[objectSubType] (integer) - The object sub-type of the file sync object
* resource[objectId] (string) - The object id of the file sync object
* resource[version] (string) - The version of the file sync object
* resource[content] (string) - Textual content
* resource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[privateKey] (string) - SSH private key
* resource[publicKey] (string) - SSH public key
* resource[keyPassphrase] (string) - Passphrase for SSH keys
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### baseEntry.addFromUploadedFile
Generic add entry using an uploaded file, should be used when the uploaded entry type is not known.


```js
kaltura.baseEntry.addFromUploadedFile({
  "uploadTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entry[name] (string) - Entry name (Min 1 chars)
* entry[description] (string) - Entry description
* entry[userId] (string) - The ID of the user who is the owner of this entry
* entry[creatorId] (string) - `insertOnly`
* entry[tags] (string) - Entry tags
* entry[adminTags] (string) - Entry admin tags can be updated only by administrators
* entry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* entry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* entry[type] (string) - Enum Type: `KalturaEntryType`
* entry[groupId] (integer)
* entry[partnerData] (string) - Can be used to store various partner related data as a string
* entry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* entry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* entry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* entry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* entry[referenceId] (string) - Entry external reference id
* entry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* entry[conversionProfileId] (integer) - Override the default ingestion profile
* entry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* entry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* entry[operationAttributes] (array)
* entry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* entry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* entry[templateEntryId] (string) - `insertOnly`
* entry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* entry[objectType] (string)
* entry[dataContent] (string) - The data of the entry
* entry[retrieveDataContentByGet] (boolean) - `insertOnly`
* entry[documentType] (integer) - `insertOnly`
* entry[msDuration] (integer) - The duration in miliseconds
* entry[playlistContent] (string) - Content of the playlist - 
* entry[filters] (array)
* entry[totalResults] (integer) - Maximum count of results to be returned in playlist execution
* entry[playlistType] (integer) - Enum Type: `KalturaPlaylistType`
* entry[mediaType] (integer) - `insertOnly`
* entry[conversionQuality] (string) - `insertOnly`
* entry[sourceType] (string) - `insertOnly`
* entry[searchProviderType] (integer) - `insertOnly`
* entry[searchProviderId] (string) - `insertOnly`
* entry[creditUserName] (string) - The user name used for credits
* entry[creditUrl] (string) - The URL for credits
* entry[streams] (array)
* entry[editorType] (integer) - Enum Type: `KalturaEditorType`
* entry[externalSourceType] (string) - `insertOnly`
* entry[offlineMessage] (string) - The message to be presented when the stream is offline
* entry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* entry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* entry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* entry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* entry[liveStreamConfigurations] (array)
* entry[recordedEntryId] (string) - Recorded entry id
* entry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* entry[publishConfigurations] (array)
* entry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* entry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* entry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* entry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* entry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* entry[playlistId] (string) - Playlist id to be played
* entry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* entry[bitrates] (array)
* entry[primaryBroadcastingUrl] (string)
* entry[secondaryBroadcastingUrl] (string)
* entry[primaryRtspBroadcastingUrl] (string)
* entry[secondaryRtspBroadcastingUrl] (string)
* entry[streamName] (string)
* entry[streamUrl] (string) - The stream url
* entry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* entry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* entry[encodingIP1] (string) - The broadcast primary ip
* entry[encodingIP2] (string) - The broadcast secondary ip
* entry[streamPassword] (string) - The broadcast password
* uploadTokenId (string) **required**
* type (string) - Enum Type: `KalturaEntryType`

### baseEntry.anonymousRank
Anonymously rank an entry, no validation is done on duplicate rankings.


```js
kaltura.baseEntry.anonymousRank({
  "entryId": "",
  "rank": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* rank (integer) **required**

### baseEntry.approve
Approve the entry and mark the pending flags (if any) as moderated (this will make the entry playable).


```js
kaltura.baseEntry.approve({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### baseEntry.clone
Clone an entry with optional attributes to apply to the clone


```js
kaltura.baseEntry.clone({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Id of entry to clone

### baseEntry.count
Count base entries by filter.


```js
kaltura.baseEntry.count({}, context)
```


### baseEntry.delete
Delete an entry.


```js
kaltura.baseEntry.delete({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Entry id to delete

### baseEntry.export



```js
kaltura.baseEntry.export({
  "entryId": "",
  "storageProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* storageProfileId (integer) **required**

### baseEntry.flag
Flag inappropriate entry for moderation.


```js
kaltura.baseEntry.flag({}, context)
```


### baseEntry.get
Get base entry by ID.


```js
kaltura.baseEntry.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Entry id
* version (integer) - Desired version of the data

### baseEntry.getByIds
Get an array of KalturaBaseEntry objects by a comma-separated list of ids.


```js
kaltura.baseEntry.getByIds({
  "entryIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryIds (string) **required** - Comma separated string of entry ids

### baseEntry.getContextData
This action delivers entry-related data, based on the user's context: access control, restriction, playback format and storage information.


```js
kaltura.baseEntry.getContextData({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* contextDataParams[referrer] (string) - URL to be used to test domain conditions.
* contextDataParams[ip] (string) - IP to be used to test geographic location conditions.
* contextDataParams[ks] (string) - Kaltura session to be used to test session and user conditions.
* contextDataParams[userAgent] (string) - Browser or client application to be used to test agent conditions.
* contextDataParams[time] (integer) - Unix timestamp (In seconds) to be used to test entry scheduling, keep null to use now.
* contextDataParams[contexts] (array)
* contextDataParams[hashes] (array)
* contextDataParams[flavorAssetId] (string) - Id of the current flavor.
* contextDataParams[flavorTags] (string) - The tags of the flavors that should be used for playback.
* contextDataParams[streamerType] (string) - Playback streamer type: RTMP, HTTP, appleHttps, rtsp, sl.
* contextDataParams[mediaProtocol] (string) - Protocol of the specific media object.
* contextDataParams[objectType] (string)

### baseEntry.getPlaybackContext
This action delivers all data relevant for player


```js
kaltura.baseEntry.getPlaybackContext({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* contextDataParams[referrer] (string) - URL to be used to test domain conditions.
* contextDataParams[ip] (string) - IP to be used to test geographic location conditions.
* contextDataParams[ks] (string) - Kaltura session to be used to test session and user conditions.
* contextDataParams[userAgent] (string) - Browser or client application to be used to test agent conditions.
* contextDataParams[time] (integer) - Unix timestamp (In seconds) to be used to test entry scheduling, keep null to use now.
* contextDataParams[contexts] (array)
* contextDataParams[hashes] (array)
* contextDataParams[flavorAssetId] (string) - Id of the current flavor.
* contextDataParams[flavorTags] (string) - The tags of the flavors that should be used for playback.
* contextDataParams[streamerType] (string) - Playback streamer type: RTMP, HTTP, appleHttps, rtsp, sl.
* contextDataParams[mediaProtocol] (string) - Protocol of the specific media object.

### baseEntry.getRemotePaths
Get remote storage existing paths for the asset.


```js
kaltura.baseEntry.getRemotePaths({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### baseEntry.index
Index an entry by id.


```js
kaltura.baseEntry.index({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* shouldUpdate (boolean)

### baseEntry.list
List base entries by filter with paging support.


```js
kaltura.baseEntry.list({}, context)
```


### baseEntry.listByReferenceId
List base entries by filter according to reference id


```js
kaltura.baseEntry.listByReferenceId({
  "refId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* refId (string) **required** - Entry Reference ID
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### baseEntry.listFlags
List all pending flags for the entry.


```js
kaltura.baseEntry.listFlags({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### baseEntry.reject
Reject the entry and mark the pending flags (if any) as moderated (this will make the entry non-playable).


```js
kaltura.baseEntry.reject({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### baseEntry.update
Update base entry. Only the properties that were set will be updated.


```js
kaltura.baseEntry.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Entry id to update
* baseEntry[name] (string) - Entry name (Min 1 chars)
* baseEntry[description] (string) - Entry description
* baseEntry[userId] (string) - The ID of the user who is the owner of this entry
* baseEntry[creatorId] (string) - `insertOnly`
* baseEntry[tags] (string) - Entry tags
* baseEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* baseEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* baseEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* baseEntry[type] (string) - Enum Type: `KalturaEntryType`
* baseEntry[groupId] (integer)
* baseEntry[partnerData] (string) - Can be used to store various partner related data as a string
* baseEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* baseEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* baseEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* baseEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* baseEntry[referenceId] (string) - Entry external reference id
* baseEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* baseEntry[conversionProfileId] (integer) - Override the default ingestion profile
* baseEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* baseEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* baseEntry[operationAttributes] (array)
* baseEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* baseEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* baseEntry[templateEntryId] (string) - `insertOnly`
* baseEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* baseEntry[objectType] (string)
* baseEntry[dataContent] (string) - The data of the entry
* baseEntry[retrieveDataContentByGet] (boolean) - `insertOnly`
* baseEntry[documentType] (integer) - `insertOnly`
* baseEntry[msDuration] (integer) - The duration in miliseconds
* baseEntry[playlistContent] (string) - Content of the playlist - 
* baseEntry[filters] (array)
* baseEntry[totalResults] (integer) - Maximum count of results to be returned in playlist execution
* baseEntry[playlistType] (integer) - Enum Type: `KalturaPlaylistType`
* baseEntry[mediaType] (integer) - `insertOnly`
* baseEntry[conversionQuality] (string) - `insertOnly`
* baseEntry[sourceType] (string) - `insertOnly`
* baseEntry[searchProviderType] (integer) - `insertOnly`
* baseEntry[searchProviderId] (string) - `insertOnly`
* baseEntry[creditUserName] (string) - The user name used for credits
* baseEntry[creditUrl] (string) - The URL for credits
* baseEntry[streams] (array)
* baseEntry[editorType] (integer) - Enum Type: `KalturaEditorType`
* baseEntry[externalSourceType] (string) - `insertOnly`
* baseEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* baseEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* baseEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* baseEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* baseEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* baseEntry[liveStreamConfigurations] (array)
* baseEntry[recordedEntryId] (string) - Recorded entry id
* baseEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* baseEntry[publishConfigurations] (array)
* baseEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* baseEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* baseEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* baseEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* baseEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* baseEntry[playlistId] (string) - Playlist id to be played
* baseEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* baseEntry[bitrates] (array)
* baseEntry[primaryBroadcastingUrl] (string)
* baseEntry[secondaryBroadcastingUrl] (string)
* baseEntry[primaryRtspBroadcastingUrl] (string)
* baseEntry[secondaryRtspBroadcastingUrl] (string)
* baseEntry[streamName] (string)
* baseEntry[streamUrl] (string) - The stream url
* baseEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* baseEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* baseEntry[encodingIP1] (string) - The broadcast primary ip
* baseEntry[encodingIP2] (string) - The broadcast secondary ip
* baseEntry[streamPassword] (string) - The broadcast password

### baseEntry.updateContent
Update the content resource associated with the entry.


```js
kaltura.baseEntry.updateContent({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Entry id to update
* resource[objectType] (string)
* resource[resource][objectType] (string)
* resource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][assetId] (string) - ID of the source asset
* resource[resource][entryId] (string) - ID of the source entry
* resource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][objectId] (string) - The object id of the file sync object
* resource[resource][version] (string) - The version of the file sync object
* resource[resource][resource][objectType] (string)
* resource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][objectType] (string)
* resource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][resources] (array)
* resource[resource][resource][resource][content] (string) - Textual content
* resource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resource][resources] (array)
* resource[resource][resource][content] (string) - Textual content
* resource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resources] (array)
* resource[resource][content] (string) - Textual content
* resource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][privateKey] (string) - SSH private key
* resource[resource][publicKey] (string) - SSH public key
* resource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][localFilePath] (string) - Full path to the local file
* resource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][fileData] (string) - Represents the $_FILE
* resource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resources] (array)
* resource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[forceAsyncDownload] (boolean) - Force Import Job
* resource[assetId] (string) - ID of the source asset
* resource[entryId] (string) - ID of the source entry
* resource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[fileSyncObjectType] (integer) - The object type of the file sync object
* resource[objectSubType] (integer) - The object sub-type of the file sync object
* resource[objectId] (string) - The object id of the file sync object
* resource[version] (string) - The version of the file sync object
* resource[content] (string) - Textual content
* resource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[privateKey] (string) - SSH private key
* resource[publicKey] (string) - SSH public key
* resource[keyPassphrase] (string) - Passphrase for SSH keys
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* conversionProfileId (integer) - The conversion profile id to be used on the entry
* advancedOptions[keepManualThumbnails] (integer) - If true manually created thumbnails will not be deleted on entry replacement
* advancedOptions[pluginOptionItems] (array)

### baseEntry.updateThumbnailFromSourceEntry
Update entry thumbnail from a different entry by a specified time offset (in seconds).


```js
kaltura.baseEntry.updateThumbnailFromSourceEntry({
  "entryId": "",
  "sourceEntryId": "",
  "timeOffset": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* sourceEntryId (string) **required** - Media entry id
* timeOffset (integer) **required** - Time offset (in seconds)

### baseEntry.updateThumbnailFromUrl
Update entry thumbnail using url.


```js
kaltura.baseEntry.updateThumbnailFromUrl({
  "entryId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* url (string) **required** - file url

### baseEntry.updateThumbnailJpeg
Update entry thumbnail using a raw jpeg file.


```js
kaltura.baseEntry.updateThumbnailJpeg({
  "entryId": "",
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* fileData (string) **required** - Jpeg file data

### baseEntry.upload
Upload a file to Kaltura, that can be used to create an entry.


```js
kaltura.baseEntry.upload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required** - The file data

### batch.addBulkUploadResult
batch addBulkUploadResultAction action adds KalturaBulkUploadResult to the DB


```js
kaltura.batch.addBulkUploadResult({}, context)
```


### batch.addMediaInfo
batch addMediaInfoAction action saves a media info object


```js
kaltura.batch.addMediaInfo({}, context)
```


### batch.checkEntryIsDone
batch checkEntryIsDone Check weather a specified entry is done converting and changes it to ready.


```js
kaltura.batch.checkEntryIsDone({
  "batchJobId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* batchJobId (string) **required** - The entry to check

### batch.checkFileExists
batch checkFileExists action check if the file exists


```js
kaltura.batch.checkFileExists({
  "localPath": "",
  "size": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* localPath (string) **required**
* size (number) **required**

### batch.cleanExclusiveJobs
batch cleanExclusiveJobs action mark as fatal error all expired jobs


```js
kaltura.batch.cleanExclusiveJobs({}, context)
```


### batch.countBulkUploadEntries
Returns total created entries count and total error entries count


```js
kaltura.batch.countBulkUploadEntries({
  "bulkUploadJobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* bulkUploadJobId (integer) **required** - The id of the bulk upload job
* bulkUploadObjectType (string) - Enum Type: `KalturaBulkUploadObjectType`

### batch.freeExclusiveJob
batch freeExclusiveJobAction action allows to get a generic BatchJob


```js
kaltura.batch.freeExclusiveJob({
  "id": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - The id of the job
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`
* resetExecutionAttempts (boolean) - Resets the job execution attampts to zero

### batch.getBulkUploadLastResult
batch getBulkUploadLastResultAction action returns the last result of the bulk upload


```js
kaltura.batch.getBulkUploadLastResult({
  "bulkUploadJobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* bulkUploadJobId (integer) **required** - The id of the bulk upload job

### batch.getExclusiveAlmostDone
batch getExclusiveAlmostDone action allows to get a BatchJob that wait for remote closure


```js
kaltura.batch.getExclusiveAlmostDone({
  "maxExecutionTime": 0,
  "numberOfJobs": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* maxExecutionTime (integer) **required** - The maximum time in seconds the job reguarly take. Is used for the locking mechanism when determining an unexpected termination of a batch-process.
* numberOfJobs (integer) **required** - The maximum number of jobs to return.
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[idEqual] (integer)
* filter[idGreaterThanOrEqual] (integer)
* filter[partnerIdEqual] (integer)
* filter[partnerIdIn] (string)
* filter[partnerIdNotIn] (string)
* filter[createdAtGreaterThanOrEqual] (integer)
* filter[createdAtLessThanOrEqual] (integer)
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[executionAttemptsGreaterThanOrEqual] (integer)
* filter[executionAttemptsLessThanOrEqual] (integer)
* filter[lockVersionGreaterThanOrEqual] (integer)
* filter[lockVersionLessThanOrEqual] (integer)
* filter[entryIdEqual] (string)
* filter[jobTypeEqual] (string) - Enum Type: `KalturaBatchJobType`
* filter[jobTypeIn] (string)
* filter[jobTypeNotIn] (string)
* filter[jobSubTypeEqual] (integer)
* filter[jobSubTypeIn] (string)
* filter[jobSubTypeNotIn] (string)
* filter[statusEqual] (integer) - Enum Type: `KalturaBatchJobStatus`
* filter[statusIn] (string)
* filter[statusNotIn] (string)
* filter[priorityGreaterThanOrEqual] (integer)
* filter[priorityLessThanOrEqual] (integer)
* filter[priorityEqual] (integer)
* filter[priorityIn] (string)
* filter[priorityNotIn] (string)
* filter[batchVersionGreaterThanOrEqual] (integer)
* filter[batchVersionLessThanOrEqual] (integer)
* filter[batchVersionEqual] (integer)
* filter[queueTimeGreaterThanOrEqual] (integer)
* filter[queueTimeLessThanOrEqual] (integer)
* filter[finishTimeGreaterThanOrEqual] (integer)
* filter[finishTimeLessThanOrEqual] (integer)
* filter[errTypeEqual] (integer) - Enum Type: `KalturaBatchJobErrorTypes`
* filter[errTypeIn] (string)
* filter[errTypeNotIn] (string)
* filter[errNumberEqual] (integer)
* filter[errNumberIn] (string)
* filter[errNumberNotIn] (string)
* filter[estimatedEffortLessThan] (integer)
* filter[estimatedEffortGreaterThan] (integer)
* filter[urgencyLessThanOrEqual] (integer)
* filter[urgencyGreaterThanOrEqual] (integer)
* filter[objectType] (string)
* filter[jobTypeAndSubTypeIn] (string)
* jobType (string) - Enum Type: `KalturaBatchJobType`

### batch.getExclusiveJobs
batch getExclusiveJobsAction action allows to get a BatchJob


```js
kaltura.batch.getExclusiveJobs({
  "maxExecutionTime": 0,
  "numberOfJobs": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* maxExecutionTime (integer) **required** - The maximum time in seconds the job reguarly take. Is used for the locking mechanism when determining an unexpected termination of a batch-process.
* numberOfJobs (integer) **required** - The maximum number of jobs to return.
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[idEqual] (integer)
* filter[idGreaterThanOrEqual] (integer)
* filter[partnerIdEqual] (integer)
* filter[partnerIdIn] (string)
* filter[partnerIdNotIn] (string)
* filter[createdAtGreaterThanOrEqual] (integer)
* filter[createdAtLessThanOrEqual] (integer)
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[executionAttemptsGreaterThanOrEqual] (integer)
* filter[executionAttemptsLessThanOrEqual] (integer)
* filter[lockVersionGreaterThanOrEqual] (integer)
* filter[lockVersionLessThanOrEqual] (integer)
* filter[entryIdEqual] (string)
* filter[jobTypeEqual] (string) - Enum Type: `KalturaBatchJobType`
* filter[jobTypeIn] (string)
* filter[jobTypeNotIn] (string)
* filter[jobSubTypeEqual] (integer)
* filter[jobSubTypeIn] (string)
* filter[jobSubTypeNotIn] (string)
* filter[statusEqual] (integer) - Enum Type: `KalturaBatchJobStatus`
* filter[statusIn] (string)
* filter[statusNotIn] (string)
* filter[priorityGreaterThanOrEqual] (integer)
* filter[priorityLessThanOrEqual] (integer)
* filter[priorityEqual] (integer)
* filter[priorityIn] (string)
* filter[priorityNotIn] (string)
* filter[batchVersionGreaterThanOrEqual] (integer)
* filter[batchVersionLessThanOrEqual] (integer)
* filter[batchVersionEqual] (integer)
* filter[queueTimeGreaterThanOrEqual] (integer)
* filter[queueTimeLessThanOrEqual] (integer)
* filter[finishTimeGreaterThanOrEqual] (integer)
* filter[finishTimeLessThanOrEqual] (integer)
* filter[errTypeEqual] (integer) - Enum Type: `KalturaBatchJobErrorTypes`
* filter[errTypeIn] (string)
* filter[errTypeNotIn] (string)
* filter[errNumberEqual] (integer)
* filter[errNumberIn] (string)
* filter[errNumberNotIn] (string)
* filter[estimatedEffortLessThan] (integer)
* filter[estimatedEffortGreaterThan] (integer)
* filter[urgencyLessThanOrEqual] (integer)
* filter[urgencyGreaterThanOrEqual] (integer)
* filter[objectType] (string)
* filter[jobTypeAndSubTypeIn] (string)
* jobType (string) - Enum Type: `KalturaBatchJobType`
* maxJobToPullForCache (integer) - The number of job to pull to cache

### batch.getExclusiveNotificationJobs
batch getExclusiveNotificationJob action allows to get a BatchJob of type NOTIFICATION


```js
kaltura.batch.getExclusiveNotificationJobs({
  "maxExecutionTime": 0,
  "numberOfJobs": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* maxExecutionTime (integer) **required** - The maximum time in seconds the job reguarly take. Is used for the locking mechanism when determining an unexpected termination of a batch-process.
* numberOfJobs (integer) **required** - The maximum number of jobs to return.
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[idEqual] (integer)
* filter[idGreaterThanOrEqual] (integer)
* filter[partnerIdEqual] (integer)
* filter[partnerIdIn] (string)
* filter[partnerIdNotIn] (string)
* filter[createdAtGreaterThanOrEqual] (integer)
* filter[createdAtLessThanOrEqual] (integer)
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[executionAttemptsGreaterThanOrEqual] (integer)
* filter[executionAttemptsLessThanOrEqual] (integer)
* filter[lockVersionGreaterThanOrEqual] (integer)
* filter[lockVersionLessThanOrEqual] (integer)
* filter[entryIdEqual] (string)
* filter[jobTypeEqual] (string) - Enum Type: `KalturaBatchJobType`
* filter[jobTypeIn] (string)
* filter[jobTypeNotIn] (string)
* filter[jobSubTypeEqual] (integer)
* filter[jobSubTypeIn] (string)
* filter[jobSubTypeNotIn] (string)
* filter[statusEqual] (integer) - Enum Type: `KalturaBatchJobStatus`
* filter[statusIn] (string)
* filter[statusNotIn] (string)
* filter[priorityGreaterThanOrEqual] (integer)
* filter[priorityLessThanOrEqual] (integer)
* filter[priorityEqual] (integer)
* filter[priorityIn] (string)
* filter[priorityNotIn] (string)
* filter[batchVersionGreaterThanOrEqual] (integer)
* filter[batchVersionLessThanOrEqual] (integer)
* filter[batchVersionEqual] (integer)
* filter[queueTimeGreaterThanOrEqual] (integer)
* filter[queueTimeLessThanOrEqual] (integer)
* filter[finishTimeGreaterThanOrEqual] (integer)
* filter[finishTimeLessThanOrEqual] (integer)
* filter[errTypeEqual] (integer) - Enum Type: `KalturaBatchJobErrorTypes`
* filter[errTypeIn] (string)
* filter[errTypeNotIn] (string)
* filter[errNumberEqual] (integer)
* filter[errNumberIn] (string)
* filter[errNumberNotIn] (string)
* filter[estimatedEffortLessThan] (integer)
* filter[estimatedEffortGreaterThan] (integer)
* filter[urgencyLessThanOrEqual] (integer)
* filter[urgencyGreaterThanOrEqual] (integer)
* filter[objectType] (string)
* filter[jobTypeAndSubTypeIn] (string)

### batch.getQueueSize
batch getQueueSize action get the queue size for job type


```js
kaltura.batch.getQueueSize({}, context)
```


### batch.logConversion
Add the data to the flavor asset conversion log, creates it if doesn't exists


```js
kaltura.batch.logConversion({
  "flavorAssetId": "",
  "data": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* flavorAssetId (string) **required**
* data (string) **required**

### batch.resetJobExecutionAttempts
batch resetJobExecutionAttempts action resets the execution attempts of the job


```js
kaltura.batch.resetJobExecutionAttempts({
  "id": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - The id of the job
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`

### batch.suspendJobs
batch suspendJobs action suspends jobs from running.


```js
kaltura.batch.suspendJobs({}, context)
```


### batch.updateBulkUploadResults
batch updateBulkUploadResults action adds KalturaBulkUploadResult to the DB


```js
kaltura.batch.updateBulkUploadResults({
  "bulkUploadJobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* bulkUploadJobId (integer) **required** - The id of the bulk upload job

### batch.updateExclusiveConvertCollectionJob
batch updateExclusiveConvertCollectionJobAction action updates a BatchJob of type CONVERT_PROFILE that was claimed using the getExclusiveConvertJobs


```js
kaltura.batch.updateExclusiveConvertCollectionJob({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - The id of the job to free
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* job[entryId] (string)
* job[entryName] (string)
* job[jobSubType] (integer)
* job[data][objectType] (string)
* job[data][entryIds] (string) - Comma separated list of entry ids
* job[data][flavorParamsId] (integer) - Flavor params id to use for conversion
* job[data][puserId] (string) - The id of the requesting user
* job[data][fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* job[data][objectData][objectType] (string)
* job[data][objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries
* job[data][srcFileSyncLocalPath] (string)
* job[data][actualSrcFileSyncLocalPath] (string) - The translated path as used by the scheduler
* job[data][srcFileSyncRemoteUrl] (string)
* job[data][thumbParamsOutputId] (integer)
* job[data][thumbAssetId] (string)
* job[data][srcAssetId] (string)
* job[data][srcAssetType] (string) - Enum Type: `KalturaAssetType`
* job[data][thumbPath] (string)
* job[data][srcFiles] (array)
* job[data][destFilePath] (string) - Output file
* job[data][flavorAssetId] (string) - Flavor asset to be ingested with the output
* job[data][offset] (number) - Clipping offset in seconds
* job[data][duration] (number) - Clipping duration in seconds
* job[data][concatenatedDuration] (number) - duration of the concated video
* job[data][srcFileSyncs] (array)
* job[data][engineVersion] (integer)
* job[data][flavorParamsOutputId] (integer)
* job[data][flavorParamsOutput][partnerId] (integer)
* job[data][flavorParamsOutput][name] (string) - The name of the Flavor Params
* job[data][flavorParamsOutput][systemName] (string) - System name of the Flavor Params
* job[data][flavorParamsOutput][description] (string) - The description of the Flavor Params
* job[data][flavorParamsOutput][tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* job[data][flavorParamsOutput][requiredPermissions] (array)
* job[data][flavorParamsOutput][sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* job[data][flavorParamsOutput][remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* job[data][flavorParamsOutput][mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* job[data][flavorParamsOutput][sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* job[data][flavorParamsOutput][videoCodec] (string) - Enum Type: `KalturaVideoCodec`
* job[data][flavorParamsOutput][videoBitrate] (integer) - The video bitrate (in KBits) of the Flavor Params
* job[data][flavorParamsOutput][audioCodec] (string) - Enum Type: `KalturaAudioCodec`
* job[data][flavorParamsOutput][audioBitrate] (integer) - The audio bitrate (in KBits) of the Flavor Params
* job[data][flavorParamsOutput][audioChannels] (integer) - The number of audio channels for "downmixing"
* job[data][flavorParamsOutput][audioSampleRate] (integer) - The audio sample rate of the Flavor Params
* job[data][flavorParamsOutput][width] (integer) - The desired width of the Flavor Params
* job[data][flavorParamsOutput][height] (integer) - The desired height of the Flavor Params
* job[data][flavorParamsOutput][frameRate] (number) - The frame rate of the Flavor Params
* job[data][flavorParamsOutput][gopSize] (integer) - The gop size of the Flavor Params
* job[data][flavorParamsOutput][conversionEngines] (string) - The list of conversion engines (comma separated)
* job[data][flavorParamsOutput][conversionEnginesExtraParams] (string) - The list of conversion engines extra params (separated with "|")
* job[data][flavorParamsOutput][twoPass] (boolean)
* job[data][flavorParamsOutput][deinterlice] (integer)
* job[data][flavorParamsOutput][rotate] (integer)
* job[data][flavorParamsOutput][operators] (string)
* job[data][flavorParamsOutput][engineVersion] (integer)
* job[data][flavorParamsOutput][format] (string) - Enum Type: `KalturaContainerFormat`
* job[data][flavorParamsOutput][aspectRatioProcessingMode] (integer)
* job[data][flavorParamsOutput][forceFrameToMultiplication16] (integer)
* job[data][flavorParamsOutput][isGopInSec] (integer)
* job[data][flavorParamsOutput][isAvoidVideoShrinkFramesizeToSource] (integer)
* job[data][flavorParamsOutput][isAvoidVideoShrinkBitrateToSource] (integer)
* job[data][flavorParamsOutput][isVideoFrameRateForLowBrAppleHls] (integer)
* job[data][flavorParamsOutput][multiStream] (string)
* job[data][flavorParamsOutput][anamorphicPixels] (number)
* job[data][flavorParamsOutput][isAvoidForcedKeyFrames] (integer)
* job[data][flavorParamsOutput][forcedKeyFramesMode] (integer)
* job[data][flavorParamsOutput][isCropIMX] (integer)
* job[data][flavorParamsOutput][optimizationPolicy] (integer)
* job[data][flavorParamsOutput][maxFrameRate] (integer)
* job[data][flavorParamsOutput][videoConstantBitrate] (integer)
* job[data][flavorParamsOutput][videoBitrateTolerance] (integer)
* job[data][flavorParamsOutput][watermarkData] (string)
* job[data][flavorParamsOutput][subtitlesData] (string)
* job[data][flavorParamsOutput][isEncrypted] (integer)
* job[data][flavorParamsOutput][contentAwareness] (number)
* job[data][flavorParamsOutput][clipOffset] (integer)
* job[data][flavorParamsOutput][clipDuration] (integer)
* job[data][flavorParamsOutput][flavorParamsId] (integer)
* job[data][flavorParamsOutput][commandLinesStr] (string)
* job[data][flavorParamsOutput][flavorParamsVersion] (string)
* job[data][flavorParamsOutput][flavorAssetId] (string)
* job[data][flavorParamsOutput][flavorAssetVersion] (string)
* job[data][flavorParamsOutput][readyBehavior] (integer)
* job[data][flavorParamsOutput][objectType] (string)
* job[data][flavorParamsOutput][densityWidth] (integer)
* job[data][flavorParamsOutput][densityHeight] (integer)
* job[data][flavorParamsOutput][sizeWidth] (integer)
* job[data][flavorParamsOutput][sizeHeight] (integer)
* job[data][flavorParamsOutput][depth] (integer)
* job[data][flavorParamsOutput][readonly] (boolean)
* job[data][flavorParamsOutput][flashVersion] (integer)
* job[data][flavorParamsOutput][poly2Bitmap] (boolean)
* job[data][flavorParamsOutput][widevineDistributionStartDate] (integer) - License distribution window start date
* job[data][flavorParamsOutput][widevineDistributionEndDate] (integer) - License distribution window end date
* job[data][entryId] (string) - Live stream entry id
* job[data][assetId] (string)
* job[data][mediaServerIndex] (string) - Enum Type: `KalturaEntryServerNodeType`
* job[data][fileIndex] (integer) - The index of the file within the entry
* job[data][srcFilePath] (string) - The recorded live media
* job[data][endTime] (number) - Duration of the live entry including all recorded segments including the current
* job[data][destDataFilePath] (string) - The data output file
* job[data][inputFileSyncLocalPath] (string)
* job[data][thumbHeight] (integer) - The height of last created thumbnail, will be used to comapare if this thumbnail is the best we can have
* job[data][thumbBitrate] (integer) - The bit rate of last created thumbnail, will be used to comapare if this thumbnail is the best we can have
* job[data][filter][orderBy] (string)
* job[data][filter][advancedSearch][objectType] (string)
* job[data][filter][advancedSearch][value] (string)
* job[data][filter][advancedSearch][categoriesMatchOr] (string)
* job[data][filter][advancedSearch][categoryEntryStatusIn] (string)
* job[data][filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* job[data][filter][advancedSearch][categoryIdEqual] (integer)
* job[data][filter][advancedSearch][memberIdEq] (string)
* job[data][filter][advancedSearch][memberIdIn] (string)
* job[data][filter][advancedSearch][memberPermissionsMatchOr] (string)
* job[data][filter][advancedSearch][memberPermissionsMatchAnd] (string)
* job[data][filter][advancedSearch][noDistributionProfiles] (boolean)
* job[data][filter][advancedSearch][distributionProfileId] (integer)
* job[data][filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* job[data][filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* job[data][filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* job[data][filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* job[data][filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* job[data][filter][advancedSearch][contentLike] (string)
* job[data][filter][advancedSearch][contentMultiLikeOr] (string)
* job[data][filter][advancedSearch][contentMultiLikeAnd] (string)
* job[data][filter][advancedSearch][cuePointsFreeText] (string)
* job[data][filter][advancedSearch][cuePointTypeIn] (string)
* job[data][filter][advancedSearch][cuePointSubTypeEqual] (integer)
* job[data][filter][advancedSearch][watermarkId] (integer)
* job[data][filter][advancedSearch][indexIdGreaterThan] (integer)
* job[data][filter][advancedSearch][depthGreaterThanEqual] (integer)
* job[data][filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][filter][advancedSearch][field] (string)
* job[data][filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* job[data][filter][advancedSearch][items] (array)
* job[data][filter][advancedSearch][idEqual] (string)
* job[data][filter][advancedSearch][idIn] (string)
* job[data][filter][advancedSearch][userIdEqual] (string)
* job[data][filter][advancedSearch][userIdIn] (string)
* job[data][filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* job[data][filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* job[data][filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* job[data][filter][advancedSearch][extendedStatusIn] (string)
* job[data][filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* job[data][filter][advancedSearch][not] (boolean)
* job[data][filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* job[data][filter][advancedSearch][metadataProfileId] (integer)
* job[data][fromPartnerId] (integer) - Id of the partner to copy from
* job[data][toPartnerId] (integer) - Id of the partner to copy to
* job[data][localFileSyncPath] (string)
* job[data][distributionProfileId] (integer)
* job[data][distributionProfile][providerType] (string) - `insertOnly`
* job[data][distributionProfile][name] (string)
* job[data][distributionProfile][status] (integer) - Enum Type: `KalturaDistributionProfileStatus`
* job[data][distributionProfile][submitEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][updateEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][deleteEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][reportEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][autoCreateFlavors] (string) - Comma separated flavor params ids that should be auto converted
* job[data][distributionProfile][autoCreateThumb] (string) - Comma separated thumbnail params ids that should be auto generated
* job[data][distributionProfile][optionalFlavorParamsIds] (string) - Comma separated flavor params ids that should be submitted if ready
* job[data][distributionProfile][requiredFlavorParamsIds] (string) - Comma separated flavor params ids that required to be ready before submission
* job[data][distributionProfile][optionalThumbDimensions] (array)
* job[data][distributionProfile][requiredThumbDimensions] (array)
* job[data][distributionProfile][optionalAssetDistributionRules] (array)
* job[data][distributionProfile][requiredAssetDistributionRules] (array)
* job[data][distributionProfile][sunriseDefaultOffset] (integer) - If entry distribution sunrise not specified that will be the default since entry creation time, in seconds
* job[data][distributionProfile][sunsetDefaultOffset] (integer) - If entry distribution sunset not specified that will be the default since entry creation time, in seconds
* job[data][distributionProfile][recommendedStorageProfileForDownload] (integer) - The best external storage to be used to download the asset files from
* job[data][distributionProfile][recommendedDcForDownload] (integer) - The best Kaltura data center to be used to download the asset files to
* job[data][distributionProfile][recommendedDcForExecute] (integer) - The best Kaltura data center to be used to execute the distribution job
* job[data][distributionProfile][objectType] (string)
* job[data][distributionProfile][fieldConfigArray] (array)
* job[data][distributionProfile][itemXpathsToExtend] (array)
* job[data][distributionProfile][useCategoryEntries] (boolean) - When checking custom XSLT conditions using the fieldConfigArray - address only categories associated with the entry via the categoryEntry object
* job[data][distributionProfile][apikey] (string)
* job[data][distributionProfile][email] (string)
* job[data][distributionProfile][sftpPass] (string)
* job[data][distributionProfile][sftpLogin] (string)
* job[data][distributionProfile][accountId] (string)
* job[data][distributionProfile][metadataProfileId] (integer)
* job[data][distributionProfile][genericProviderId] (integer) - `insertOnly`
* job[data][distributionProfile][submitAction][protocol] (integer) - Enum Type: `KalturaDistributionProtocol`
* job[data][distributionProfile][submitAction][serverUrl] (string)
* job[data][distributionProfile][submitAction][serverPath] (string)
* job[data][distributionProfile][submitAction][username] (string)
* job[data][distributionProfile][submitAction][password] (string)
* job[data][distributionProfile][submitAction][ftpPassiveMode] (boolean)
* job[data][distributionProfile][submitAction][httpFieldName] (string)
* job[data][distributionProfile][submitAction][httpFileName] (string)
* job[data][distributionProfile][xsl] (string)
* job[data][distributionProfile][ftpHost] (string)
* job[data][distributionProfile][ftpUsername] (string)
* job[data][distributionProfile][ftpPassword] (string)
* job[data][distributionProfile][ftpPath] (string)
* job[data][distributionProfile][channelTitle] (string)
* job[data][distributionProfile][flavorAssetFilenameXslt] (string)
* job[data][distributionProfile][thumbnailAssetFilenameXslt] (string)
* job[data][distributionProfile][assetFilenameXslt] (string)
* job[data][distributionProfile][feedTitle] (string)
* job[data][distributionProfile][feedLink] (string)
* job[data][distributionProfile][feedDescription] (string)
* job[data][distributionProfile][feedLastBuildDate] (string)
* job[data][distributionProfile][itemLink] (string)
* job[data][distributionProfile][cPlatformTvSeries] (array)
* job[data][distributionProfile][cPlatformTvSeriesField] (string)
* job[data][distributionProfile][shouldIncludeCuePoints] (boolean)
* job[data][distributionProfile][shouldIncludeCaptions] (boolean)
* job[data][distributionProfile][shouldAddThumbExtension] (boolean)
* job[data][distributionProfile][targetServiceUrl] (string)
* job[data][distributionProfile][targetAccountId] (integer)
* job[data][distributionProfile][targetLoginId] (string)
* job[data][distributionProfile][targetLoginPassword] (string)
* job[data][distributionProfile][metadataXslt] (string)
* job[data][distributionProfile][metadataXpathsTriggerUpdate] (array)
* job[data][distributionProfile][distributeCaptions] (boolean)
* job[data][distributionProfile][distributeCuePoints] (boolean)
* job[data][distributionProfile][distributeRemoteFlavorAssetContent] (boolean)
* job[data][distributionProfile][distributeRemoteThumbAssetContent] (boolean)
* job[data][distributionProfile][distributeRemoteCaptionAssetContent] (boolean)
* job[data][distributionProfile][mapAccessControlProfileIds] (array)
* job[data][distributionProfile][mapConversionProfileIds] (array)
* job[data][distributionProfile][mapMetadataProfileIds] (array)
* job[data][distributionProfile][mapStorageProfileIds] (array)
* job[data][distributionProfile][mapFlavorParamsIds] (array)
* job[data][distributionProfile][mapThumbParamsIds] (array)
* job[data][distributionProfile][mapCaptionParamsIds] (array)
* job[data][distributionProfile][user] (string)
* job[data][distributionProfile][password] (string)
* job[data][distributionProfile][geoBlockingMapping] (integer) - Enum Type: `KalturaDailymotionGeoBlockingMapping`
* job[data][distributionProfile][channelLink] (string)
* job[data][distributionProfile][channelDescription] (string)
* job[data][distributionProfile][cuePointsProvider] (string)
* job[data][distributionProfile][itemsPerPage] (string)
* job[data][distributionProfile][ignoreSchedulingInFeed] (boolean)
* job[data][distributionProfile][apiAuthorizeUrl] (string)
* job[data][distributionProfile][pageId] (string)
* job[data][distributionProfile][pageAccessToken] (string)
* job[data][distributionProfile][userAccessToken] (string)
* job[data][distributionProfile][state] (string)
* job[data][distributionProfile][permissions] (string)
* job[data][distributionProfile][reRequestPermissions] (integer)
* job[data][distributionProfile][contentOwner] (string)
* job[data][distributionProfile][upstreamVideoId] (string)
* job[data][distributionProfile][upstreamNetworkName] (string)
* job[data][distributionProfile][upstreamNetworkId] (string)
* job[data][distributionProfile][categoryId] (string)
* job[data][distributionProfile][replaceGroup] (boolean)
* job[data][distributionProfile][replaceAirDates] (boolean)
* job[data][distributionProfile][protocol] (integer) - `insertOnly`
* job[data][distributionProfile][host] (string)
* job[data][distributionProfile][port] (integer)
* job[data][distributionProfile][basePath] (string)
* job[data][distributionProfile][username] (string)
* job[data][distributionProfile][passphrase] (string)
* job[data][distributionProfile][sftpPublicKey] (string)
* job[data][distributionProfile][sftpPrivateKey] (string)
* job[data][distributionProfile][disableMetadata] (boolean)
* job[data][distributionProfile][metadataFilenameXslt] (string)
* job[data][distributionProfile][asperaPublicKey] (string)
* job[data][distributionProfile][asperaPrivateKey] (string)
* job[data][distributionProfile][sendMetadataAfterAssets] (boolean)
* job[data][distributionProfile][sftpHost] (string)
* job[data][distributionProfile][seriesChannel] (string)
* job[data][distributionProfile][seriesPrimaryCategory] (string)
* job[data][distributionProfile][seriesAdditionalCategories] (array)
* job[data][distributionProfile][seasonNumber] (string)
* job[data][distributionProfile][seasonSynopsis] (string)
* job[data][distributionProfile][seasonTuneInInformation] (string)
* job[data][distributionProfile][videoMediaType] (string)
* job[data][distributionProfile][disableEpisodeNumberCustomValidation] (boolean)
* job[data][distributionProfile][asperaHost] (string)
* job[data][distributionProfile][asperaLogin] (string)
* job[data][distributionProfile][asperaPass] (string)
* job[data][distributionProfile][domain] (string)
* job[data][distributionProfile][ftpLogin] (string)
* job[data][distributionProfile][ftpPass] (string)
* job[data][distributionProfile][providerName] (string)
* job[data][distributionProfile][providerId] (string)
* job[data][distributionProfile][copyright] (string)
* job[data][distributionProfile][entitlements] (string)
* job[data][distributionProfile][rating] (string)
* job[data][distributionProfile][itemType] (string)
* job[data][distributionProfile][csId] (string)
* job[data][distributionProfile][source] (string)
* job[data][distributionProfile][sourceFriendlyName] (string)
* job[data][distributionProfile][pageGroup] (string)
* job[data][distributionProfile][sourceFlavorParamsId] (integer)
* job[data][distributionProfile][wmvFlavorParamsId] (integer)
* job[data][distributionProfile][flvFlavorParamsId] (integer)
* job[data][distributionProfile][slFlavorParamsId] (integer)
* job[data][distributionProfile][slHdFlavorParamsId] (integer)
* job[data][distributionProfile][msnvideoCat] (string)
* job[data][distributionProfile][msnvideoTop] (string)
* job[data][distributionProfile][msnvideoTopCat] (string)
* job[data][distributionProfile][channelLanguage] (string)
* job[data][distributionProfile][channelCopyright] (string)
* job[data][distributionProfile][channelImageTitle] (string)
* job[data][distributionProfile][channelImageUrl] (string)
* job[data][distributionProfile][channelImageLink] (string)
* job[data][distributionProfile][itemMediaRating] (string)
* job[data][distributionProfile][ips] (string)
* job[data][distributionProfile][certificateKey] (string)
* job[data][distributionProfile][bodyXslt] (string)
* job[data][distributionProfile][sftpBasePath] (string)
* job[data][distributionProfile][channelManagingEditor] (string)
* job[data][distributionProfile][channelImageWidth] (string)
* job[data][distributionProfile][channelImageHeight] (string)
* job[data][distributionProfile][channelGenerator] (string)
* job[data][distributionProfile][channelRating] (string)
* job[data][distributionProfile][feedSubtitle] (string)
* job[data][distributionProfile][feedAuthorName] (string)
* job[data][distributionProfile][feedLanguage] (string)
* job[data][distributionProfile][feedCopyright] (string)
* job[data][distributionProfile][feedImageTitle] (string)
* job[data][distributionProfile][feedImageUrl] (string)
* job[data][distributionProfile][feedImageLink] (string)
* job[data][distributionProfile][feedImageWidth] (integer)
* job[data][distributionProfile][feedImageHeight] (integer)
* job[data][distributionProfile][ingestUrl] (string)
* job[data][distributionProfile][tags] (array)
* job[data][distributionProfile][xsltFile] (string)
* job[data][distributionProfile][domainName] (string) - The name of the Domain that the Upload User should have access to, Used for authentication.
* job[data][distributionProfile][channelGuid] (string) - The Channel GUID assigned to this Publication Rule. Must be a valid Channel in the Domain that was used in authentication.
* job[data][distributionProfile][apiHostUrl] (string) - The API host URL that the Upload User should have access to, Used for HTTP content submission.
* job[data][distributionProfile][domainGuid] (string) - The GUID of the Customer Domain in the Unicorn system obtained by contacting your Unicorn representative.
* job[data][distributionProfile][adFreeApplicationGuid] (string) - The GUID for the application in which to record metrics and enforce business rules obtained through your Unicorn representative.
* job[data][distributionProfile][remoteAssetParamsId] (integer) - The flavor-params that will be used for the remote asset.
* job[data][distributionProfile][storageProfileId] (string) - The remote storage that should be used for the remote asset.
* job[data][distributionProfile][backgroundImageWide] (string)
* job[data][distributionProfile][backgroundImageStandard] (string)
* job[data][distributionProfile][entitlement] (string)
* job[data][distributionProfile][priority] (string)
* job[data][distributionProfile][allowStreaming] (string)
* job[data][distributionProfile][streamingPriceCode] (string)
* job[data][distributionProfile][allowDownload] (string)
* job[data][distributionProfile][downloadPriceCode] (string)
* job[data][distributionProfile][contactTelephone] (string)
* job[data][distributionProfile][contactEmail] (string)
* job[data][distributionProfile][processFeed] (integer) - Enum Type: `KalturaYahooDistributionProcessFeedActionStatus`
* job[data][distributionProfile][feedSpecVersion] (string) - Enum Type: `KalturaYouTubeDistributionFeedSpecVersion`
* job[data][distributionProfile][notificationEmail] (string)
* job[data][distributionProfile][sftpPort] (integer)
* job[data][distributionProfile][sftpBaseDir] (string)
* job[data][distributionProfile][ownerName] (string)
* job[data][distributionProfile][defaultCategory] (string)
* job[data][distributionProfile][allowComments] (string)
* job[data][distributionProfile][allowEmbedding] (string)
* job[data][distributionProfile][allowRatings] (string)
* job[data][distributionProfile][allowResponses] (string)
* job[data][distributionProfile][commercialPolicy] (string)
* job[data][distributionProfile][ugcPolicy] (string)
* job[data][distributionProfile][target] (string)
* job[data][distributionProfile][adServerPartnerId] (string)
* job[data][distributionProfile][enableAdServer] (boolean)
* job[data][distributionProfile][allowPreRollAds] (boolean)
* job[data][distributionProfile][allowPostRollAds] (boolean)
* job[data][distributionProfile][strict] (string)
* job[data][distributionProfile][overrideManualEdits] (string)
* job[data][distributionProfile][urgentReference] (string)
* job[data][distributionProfile][allowSyndication] (string)
* job[data][distributionProfile][hideViewCount] (string)
* job[data][distributionProfile][allowAdsenseForVideo] (string)
* job[data][distributionProfile][allowInvideo] (string)
* job[data][distributionProfile][allowMidRollAds] (boolean)
* job[data][distributionProfile][instreamStandard] (string)
* job[data][distributionProfile][instreamTrueview] (string)
* job[data][distributionProfile][claimType] (string)
* job[data][distributionProfile][blockOutsideOwnership] (string)
* job[data][distributionProfile][captionAutosync] (string)
* job[data][distributionProfile][deleteReference] (boolean)
* job[data][distributionProfile][releaseClaims] (boolean)
* job[data][distributionProfile][googleClientId] (string)
* job[data][distributionProfile][googleClientSecret] (string)
* job[data][distributionProfile][googleTokenData] (string)
* job[data][distributionProfile][assumeSuccess] (boolean)
* job[data][distributionProfile][privacyStatus] (string)
* job[data][dropFolderId] (integer)
* job[data][dropFolderFileIds] (string)
* job[data][parsedSlug] (string)
* job[data][contentMatchPolicy] (integer) - Enum Type: `KalturaDropFolderContentFileHandlerMatchPolicy`
* job[data][conversionProfileId] (integer)
* job[data][parsedUserId] (string)
* job[data][templateId] (integer)
* job[data][contentParameters] (array)
* job[data][srcFileUrl] (string)
* job[data][destFileLocalPath] (string)
* job[data][fileSize] (integer)
* job[data][metadataId] (integer)
* job[data][changedCategoryId] (integer)
* job[data][deletedPrivacyContexts] (string)
* job[data][addedPrivacyContexts] (string)
* job[data][providerType] (string) - Enum Type: `KalturaIntegrationProviderType`
* job[data][providerData][objectType] (string)
* job[data][providerData][entryId] (string) - Entry ID
* job[data][providerData][flavorAssetId] (string) - Flavor ID
* job[data][providerData][captionAssetFormats] (string) - Caption formats
* job[data][providerData][priority] (string) - Enum Type: `KalturaCielo24Priority`
* job[data][providerData][fidelity] (string) - Enum Type: `KalturaCielo24Fidelity`
* job[data][providerData][spokenLanguage] (string) - Enum Type: `KalturaLanguage`
* job[data][providerData][replaceMediaContent] (boolean) - should replace remote media content
* job[data][providerData][additionalParameters] (string) - additional parameters to send to Cielo24
* job[data][providerData][metadataProfileId] (integer) - ID of the metadata profile for the extracted term metadata
* job[data][providerData][transcriptAssetId] (string) - ID of the transcript asset
* job[data][providerData][voicebaseApiKey] (string) - Voicebase API key to fetch transcript tokens
* job[data][providerData][voicebaseApiPassword] (string) - Voicebase API password to fetch transcript tokens
* job[data][providerData][exampleUrl] (string) - Just an example
* job[data][providerData][transcriptId] (string) - input Transcript-asset ID
* job[data][timeReference] (integer)
* job[data][timeZoneOffset] (integer)
* job[data][outputPath] (string)
* job[data][recipientEmail] (string)
* job[data][vodEntryId] (string) - $vod Entry Id
* job[data][liveEntryId] (string) - live Entry Id
* job[data][totalVodDuration] (number) - total VOD Duration
* job[data][lastSegmentDuration] (number) - last Segment Duration
* job[data][amfArray] (string) - amf Array File Path
* job[data][lastCuePointSyncTime] (integer) - last live to vod sync time
* job[data][lastSegmentDrift] (integer) - last segment drift
* job[data][mailType] (string) - Enum Type: `KalturaMailType`
* job[data][mailPriority] (integer)
* job[data][status] (integer) - Enum Type: `KalturaMailJobStatus`
* job[data][recipientName] (string)
* job[data][recipientId] (integer) - kuserId
* job[data][fromName] (string)
* job[data][fromEmail] (string)
* job[data][bodyParams] (string)
* job[data][subjectParams] (string)
* job[data][templatePath] (string)
* job[data][language] (string) - Enum Type: `KalturaLanguageCode`
* job[data][campaignId] (integer)
* job[data][minSendDate] (integer)
* job[data][isHtml] (boolean)
* job[data][separator] (string)
* job[data][srcCategoryId] (integer) - Source category id
* job[data][destCategoryId] (integer) - Destination category id
* job[data][lastMovedCategoryId] (integer) - Saves the last category id that its entries moved completely
* job[data][lastMovedCategoryPageIndex] (integer) - Saves the last page index of the child categories filter pager
* job[data][lastMovedCategoryEntryPageIndex] (integer) - Saves the last page index of the category entries filter pager
* job[data][moveFromChildren] (boolean) - All entries from all child categories will be moved as well
* job[data][destCategoryFullIds] (string) - Destination categories fallback ids
* job[data][userId] (string)
* job[data][type] (integer) - Enum Type: `KalturaNotificationType`
* job[data][typeAsString] (string)
* job[data][objectId] (string)
* job[data][data] (string)
* job[data][numberOfAttempts] (integer)
* job[data][notificationResult] (string)
* job[data][objType] (integer) - Enum Type: `KalturaNotificationObjectType`
* job[data][captionAssetId] (string)
* job[data][multiLanaguageCaptionAssetId] (string)
* job[data][fileLocation] (string)
* job[data][streamID] (string)
* job[data][backupStreamID] (string)
* job[data][rtmp] (string)
* job[data][encoderIP] (string)
* job[data][backupEncoderIP] (string)
* job[data][encoderPassword] (string)
* job[data][encoderUsername] (string)
* job[data][endDate] (integer)
* job[data][returnVal] (string)
* job[data][mediaType] (integer)
* job[data][primaryBroadcastingUrl] (string)
* job[data][secondaryBroadcastingUrl] (string)
* job[data][streamName] (string)
* job[data][maxResults] (integer)
* job[data][resultsFilePath] (string)
* job[data][referenceTime] (integer)
* job[data][serverUrl] (string)
* job[data][serverUsername] (string)
* job[data][serverPassword] (string)
* job[data][serverPrivateKey] (string)
* job[data][serverPublicKey] (string)
* job[data][serverPassPhrase] (string)
* job[data][ftpPassiveMode] (boolean)
* job[data][srcFileSyncId] (string)
* job[data][destFileSyncStoredPath] (string)
* job[data][categoryId] (integer) - category id
* job[data][lastUpdatedCategoryEntryCreatedAt] (integer) - Saves the last category entry creation date that was updated
* job[data][lastUpdatedCategoryCreatedAt] (integer) - Saves the last sub category creation date that was updated
* job[data][srcXslPath] (string)
* job[data][srcVersion] (integer)
* job[data][destVersion] (integer)
* job[data][destXsdPath] (string)
* job[data][metadataProfileId] (integer)
* job[data][scanResult] (integer) - Enum Type: `KalturaVirusScanJobResult`
* job[data][virusFoundAction] (integer) - Enum Type: `KalturaVirusFoundAction`
* job[data][syncMode] (integer) - Enum Type: `KalturaWidevineRepositorySyncMode`
* job[data][wvAssetIds] (string)
* job[data][modifiedAttributes] (string)
* job[data][monitorSyncCompletion] (integer)
* job[data][columns] (array)
* job[data][eventsType] (integer) - Enum Type: `KalturaScheduleEventType`
* job[data][destDirLocalPath] (string)
* job[data][destDirRemoteUrl] (string)
* job[data][destFileName] (string)
* job[data][inputXmlLocalPath] (string)
* job[data][inputXmlRemoteUrl] (string)
* job[data][commandLinesStr] (string)
* job[data][flavors] (array)
* job[data][destFileSyncLocalPath] (string)
* job[data][destFileSyncRemoteUrl] (string)
* job[data][logFileSyncLocalPath] (string)
* job[data][logFileSyncRemoteUrl] (string)
* job[data][remoteMediaId] (string)
* job[data][customData] (string)
* job[data][extraDestFileSyncs] (array)
* job[data][engineMessage] (string)
* job[data][calculateComplexity] (boolean)
* job[data][extractId3Tags] (boolean)
* job[data][detectGOP] (integer)
* job[data][createThumb] (boolean) - Indicates if a thumbnail should be created
* job[data][thumbOffset] (integer) - The position of the thumbnail in the media file
* job[data][keepDistributionItem] (boolean) - Flag signifying that the associated distribution item should not be moved to 'removed' status
* job[data][plays] (integer)
* job[data][views] (integer)
* job[data][description] (string)
* job[data][webexHostId] (string)
* job[data][server][name] (string)
* job[data][server][systemName] (string)
* job[data][server][description] (string)
* job[data][server][dc] (integer) - The dc of the server
* job[data][server][objectType] (string)
* job[data][server][host] (string)
* job[data][server][port] (integer)
* job[data][server][protocol] (string) - Enum Type: `KalturaActivitiBusinessProcessServerProtocol`
* job[data][server][username] (string)
* job[data][server][password] (string)
* job[data][to][objectType] (string)
* job[data][to][categoryUserFilter][orderBy] (string)
* job[data][to][categoryUserFilter][categoryIdEqual] (integer)
* job[data][to][categoryUserFilter][categoryIdIn] (string)
* job[data][to][categoryUserFilter][userIdEqual] (string)
* job[data][to][categoryUserFilter][userIdIn] (string)
* job[data][to][categoryUserFilter][permissionLevelEqual] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* job[data][to][categoryUserFilter][permissionLevelIn] (string)
* job[data][to][categoryUserFilter][statusEqual] (integer) - Enum Type: `KalturaCategoryUserStatus`
* job[data][to][categoryUserFilter][statusIn] (string)
* job[data][to][categoryUserFilter][createdAtGreaterThanOrEqual] (integer)
* job[data][to][categoryUserFilter][createdAtLessThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updatedAtGreaterThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updatedAtLessThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updateMethodEqual] (integer) - Enum Type: `KalturaUpdateMethodType`
* job[data][to][categoryUserFilter][updateMethodIn] (string)
* job[data][to][categoryUserFilter][categoryFullIdsStartsWith] (string)
* job[data][to][categoryUserFilter][categoryFullIdsEqual] (string)
* job[data][to][categoryUserFilter][permissionNamesMatchAnd] (string)
* job[data][to][categoryUserFilter][permissionNamesMatchOr] (string)
* job[data][to][categoryUserFilter][permissionNamesNotContains] (string)
* job[data][to][categoryUserFilter][categoryDirectMembers] (boolean) - Return the list of categoryUser that are not inherited from parent category - only the direct categoryUsers.
* job[data][to][categoryUserFilter][freeText] (string) - Free text search on user id or screen name
* job[data][to][categoryUserFilter][relatedGroupsByUserId] (string) - Return a list of categoryUser that related to the userId in this field by groups
* job[data][to][emailRecipients] (array)
* job[data][to][filter][orderBy] (string)
* job[data][to][filter][partnerIdEqual] (integer)
* job[data][to][filter][typeEqual] (integer) - Enum Type: `KalturaUserType`
* job[data][to][filter][typeIn] (string)
* job[data][to][filter][screenNameLike] (string)
* job[data][to][filter][screenNameStartsWith] (string)
* job[data][to][filter][emailLike] (string)
* job[data][to][filter][emailStartsWith] (string)
* job[data][to][filter][tagsMultiLikeOr] (string)
* job[data][to][filter][tagsMultiLikeAnd] (string)
* job[data][to][filter][statusEqual] (integer) - Enum Type: `KalturaUserStatus`
* job[data][to][filter][statusIn] (string)
* job[data][to][filter][createdAtGreaterThanOrEqual] (integer)
* job[data][to][filter][createdAtLessThanOrEqual] (integer)
* job[data][to][filter][firstNameStartsWith] (string)
* job[data][to][filter][lastNameStartsWith] (string)
* job[data][to][filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][to][filter][idOrScreenNameStartsWith] (string)
* job[data][to][filter][idEqual] (string)
* job[data][to][filter][idIn] (string)
* job[data][to][filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][to][filter][roleIdEqual] (string)
* job[data][to][filter][roleIdsEqual] (string)
* job[data][to][filter][roleIdsIn] (string)
* job[data][to][filter][firstNameOrLastNameStartsWith] (string)
* job[data][to][filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* job[data][to][filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* job[data][to][filter][objectType] (string)
* job[data][url] (string) - Remote server URL
* job[data][method] (integer) - Enum Type: `KalturaHttpNotificationMethod`
* job[data][timeout] (integer) - The maximum number of seconds to allow cURL functions to execute.
* job[data][connectTimeout] (integer) - The number of seconds to wait while trying to connect.
* job[data][username] (string) - A username to use for the connection.
* job[data][password] (string) - A password to use for the connection.
* job[data][authenticationMethod] (integer) - Enum Type: `KalturaHttpNotificationAuthenticationMethod`
* job[data][sslVersion] (integer) - Enum Type: `KalturaHttpNotificationSslVersion`
* job[data][sslCertificate] (string) - SSL certificate to verify the peer with.
* job[data][sslCertificateType] (string) - Enum Type: `KalturaHttpNotificationCertificateType`
* job[data][sslCertificatePassword] (string) - The password required to use the certificate.
* job[data][sslEngine] (string) - The identifier for the crypto engine of the private SSL key specified in ssl key.
* job[data][sslEngineDefault] (string) - The identifier for the crypto engine used for asymmetric crypto operations.
* job[data][sslKeyType] (string) - Enum Type: `KalturaHttpNotificationSslKeyType`
* job[data][sslKey] (string) - Private SSL key.
* job[data][sslKeyPassword] (string) - The secret password needed to use the private SSL key specified in ssl key.
* job[data][customHeaders] (array)
* job[data][signSecret] (string) - The secret to sign the notification with
* job[data][privateKey] (string)
* job[data][publicKey] (string)
* job[data][passPhrase] (string)
* job[data][dropFolderFileId] (integer)
* job[data][wsdlUsername] (string)
* job[data][wsdlPassword] (string)
* job[data][cpcode] (string)
* job[data][emailId] (string)
* job[data][primaryContact] (string)
* job[data][secondaryContact] (string)
* job[data][streamId] (integer)
* job[data][systemUserName] (string)
* job[data][systemPassword] (string)
* job[data][domainName] (string)
* job[data][dvrEnabled] (integer) - Enum Type: `KalturaDVRStatus`
* job[data][dvrWindow] (integer)
* job[data][streamType] (string) - Enum Type: `KalturaAkamaiUniversalStreamType`
* job[data][notificationEmail] (string)
* job[data][provisioningParams] (array)
* job[data][userName] (string)
* job[data][protocol] (string) - http / https
* job[data][ksType] (integer) - Enum Type: `KalturaSessionType`
* job[data][userRoles] (array)
* job[data][cachedObjectType] (string) - Class name
* job[data][startObjectKey] (string)
* job[data][endObjectKey] (string)
* job[data][force] (boolean)
* job[data][createLink] (boolean)
* job[data][contentMoid] (string) - Unique Kontiki MOID for the content uploaded to Kontiki
* job[data][serviceToken] (string)
* job[data][filesPermissionInS3] (string) - Enum Type: `KalturaAmazonS3StorageProfileFilesPermissionLevel`
* job[data][s3Region] (string)
* job[data][sseType] (string)
* job[data][sseKmsKeyId] (string)
* job[data][signatureType] (string)
* job[data][endPoint] (string)

### batch.updateExclusiveJob
batch updateExclusiveJobAction action updates a BatchJob of extended type that was claimed using the getExclusiveJobs


```js
kaltura.batch.updateExclusiveJob({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - The id of the job to free
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* job[entryId] (string)
* job[entryName] (string)
* job[jobSubType] (integer)
* job[data][objectType] (string)
* job[data][entryIds] (string) - Comma separated list of entry ids
* job[data][flavorParamsId] (integer) - Flavor params id to use for conversion
* job[data][puserId] (string) - The id of the requesting user
* job[data][fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* job[data][objectData][objectType] (string)
* job[data][objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries
* job[data][srcFileSyncLocalPath] (string)
* job[data][actualSrcFileSyncLocalPath] (string) - The translated path as used by the scheduler
* job[data][srcFileSyncRemoteUrl] (string)
* job[data][thumbParamsOutputId] (integer)
* job[data][thumbAssetId] (string)
* job[data][srcAssetId] (string)
* job[data][srcAssetType] (string) - Enum Type: `KalturaAssetType`
* job[data][thumbPath] (string)
* job[data][srcFiles] (array)
* job[data][destFilePath] (string) - Output file
* job[data][flavorAssetId] (string) - Flavor asset to be ingested with the output
* job[data][offset] (number) - Clipping offset in seconds
* job[data][duration] (number) - Clipping duration in seconds
* job[data][concatenatedDuration] (number) - duration of the concated video
* job[data][srcFileSyncs] (array)
* job[data][engineVersion] (integer)
* job[data][flavorParamsOutputId] (integer)
* job[data][flavorParamsOutput][partnerId] (integer)
* job[data][flavorParamsOutput][name] (string) - The name of the Flavor Params
* job[data][flavorParamsOutput][systemName] (string) - System name of the Flavor Params
* job[data][flavorParamsOutput][description] (string) - The description of the Flavor Params
* job[data][flavorParamsOutput][tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* job[data][flavorParamsOutput][requiredPermissions] (array)
* job[data][flavorParamsOutput][sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* job[data][flavorParamsOutput][remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* job[data][flavorParamsOutput][mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* job[data][flavorParamsOutput][sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* job[data][flavorParamsOutput][videoCodec] (string) - Enum Type: `KalturaVideoCodec`
* job[data][flavorParamsOutput][videoBitrate] (integer) - The video bitrate (in KBits) of the Flavor Params
* job[data][flavorParamsOutput][audioCodec] (string) - Enum Type: `KalturaAudioCodec`
* job[data][flavorParamsOutput][audioBitrate] (integer) - The audio bitrate (in KBits) of the Flavor Params
* job[data][flavorParamsOutput][audioChannels] (integer) - The number of audio channels for "downmixing"
* job[data][flavorParamsOutput][audioSampleRate] (integer) - The audio sample rate of the Flavor Params
* job[data][flavorParamsOutput][width] (integer) - The desired width of the Flavor Params
* job[data][flavorParamsOutput][height] (integer) - The desired height of the Flavor Params
* job[data][flavorParamsOutput][frameRate] (number) - The frame rate of the Flavor Params
* job[data][flavorParamsOutput][gopSize] (integer) - The gop size of the Flavor Params
* job[data][flavorParamsOutput][conversionEngines] (string) - The list of conversion engines (comma separated)
* job[data][flavorParamsOutput][conversionEnginesExtraParams] (string) - The list of conversion engines extra params (separated with "|")
* job[data][flavorParamsOutput][twoPass] (boolean)
* job[data][flavorParamsOutput][deinterlice] (integer)
* job[data][flavorParamsOutput][rotate] (integer)
* job[data][flavorParamsOutput][operators] (string)
* job[data][flavorParamsOutput][engineVersion] (integer)
* job[data][flavorParamsOutput][format] (string) - Enum Type: `KalturaContainerFormat`
* job[data][flavorParamsOutput][aspectRatioProcessingMode] (integer)
* job[data][flavorParamsOutput][forceFrameToMultiplication16] (integer)
* job[data][flavorParamsOutput][isGopInSec] (integer)
* job[data][flavorParamsOutput][isAvoidVideoShrinkFramesizeToSource] (integer)
* job[data][flavorParamsOutput][isAvoidVideoShrinkBitrateToSource] (integer)
* job[data][flavorParamsOutput][isVideoFrameRateForLowBrAppleHls] (integer)
* job[data][flavorParamsOutput][multiStream] (string)
* job[data][flavorParamsOutput][anamorphicPixels] (number)
* job[data][flavorParamsOutput][isAvoidForcedKeyFrames] (integer)
* job[data][flavorParamsOutput][forcedKeyFramesMode] (integer)
* job[data][flavorParamsOutput][isCropIMX] (integer)
* job[data][flavorParamsOutput][optimizationPolicy] (integer)
* job[data][flavorParamsOutput][maxFrameRate] (integer)
* job[data][flavorParamsOutput][videoConstantBitrate] (integer)
* job[data][flavorParamsOutput][videoBitrateTolerance] (integer)
* job[data][flavorParamsOutput][watermarkData] (string)
* job[data][flavorParamsOutput][subtitlesData] (string)
* job[data][flavorParamsOutput][isEncrypted] (integer)
* job[data][flavorParamsOutput][contentAwareness] (number)
* job[data][flavorParamsOutput][clipOffset] (integer)
* job[data][flavorParamsOutput][clipDuration] (integer)
* job[data][flavorParamsOutput][flavorParamsId] (integer)
* job[data][flavorParamsOutput][commandLinesStr] (string)
* job[data][flavorParamsOutput][flavorParamsVersion] (string)
* job[data][flavorParamsOutput][flavorAssetId] (string)
* job[data][flavorParamsOutput][flavorAssetVersion] (string)
* job[data][flavorParamsOutput][readyBehavior] (integer)
* job[data][flavorParamsOutput][objectType] (string)
* job[data][flavorParamsOutput][densityWidth] (integer)
* job[data][flavorParamsOutput][densityHeight] (integer)
* job[data][flavorParamsOutput][sizeWidth] (integer)
* job[data][flavorParamsOutput][sizeHeight] (integer)
* job[data][flavorParamsOutput][depth] (integer)
* job[data][flavorParamsOutput][readonly] (boolean)
* job[data][flavorParamsOutput][flashVersion] (integer)
* job[data][flavorParamsOutput][poly2Bitmap] (boolean)
* job[data][flavorParamsOutput][widevineDistributionStartDate] (integer) - License distribution window start date
* job[data][flavorParamsOutput][widevineDistributionEndDate] (integer) - License distribution window end date
* job[data][entryId] (string) - Live stream entry id
* job[data][assetId] (string)
* job[data][mediaServerIndex] (string) - Enum Type: `KalturaEntryServerNodeType`
* job[data][fileIndex] (integer) - The index of the file within the entry
* job[data][srcFilePath] (string) - The recorded live media
* job[data][endTime] (number) - Duration of the live entry including all recorded segments including the current
* job[data][destDataFilePath] (string) - The data output file
* job[data][inputFileSyncLocalPath] (string)
* job[data][thumbHeight] (integer) - The height of last created thumbnail, will be used to comapare if this thumbnail is the best we can have
* job[data][thumbBitrate] (integer) - The bit rate of last created thumbnail, will be used to comapare if this thumbnail is the best we can have
* job[data][filter][orderBy] (string)
* job[data][filter][advancedSearch][objectType] (string)
* job[data][filter][advancedSearch][value] (string)
* job[data][filter][advancedSearch][categoriesMatchOr] (string)
* job[data][filter][advancedSearch][categoryEntryStatusIn] (string)
* job[data][filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* job[data][filter][advancedSearch][categoryIdEqual] (integer)
* job[data][filter][advancedSearch][memberIdEq] (string)
* job[data][filter][advancedSearch][memberIdIn] (string)
* job[data][filter][advancedSearch][memberPermissionsMatchOr] (string)
* job[data][filter][advancedSearch][memberPermissionsMatchAnd] (string)
* job[data][filter][advancedSearch][noDistributionProfiles] (boolean)
* job[data][filter][advancedSearch][distributionProfileId] (integer)
* job[data][filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* job[data][filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* job[data][filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* job[data][filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* job[data][filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* job[data][filter][advancedSearch][contentLike] (string)
* job[data][filter][advancedSearch][contentMultiLikeOr] (string)
* job[data][filter][advancedSearch][contentMultiLikeAnd] (string)
* job[data][filter][advancedSearch][cuePointsFreeText] (string)
* job[data][filter][advancedSearch][cuePointTypeIn] (string)
* job[data][filter][advancedSearch][cuePointSubTypeEqual] (integer)
* job[data][filter][advancedSearch][watermarkId] (integer)
* job[data][filter][advancedSearch][indexIdGreaterThan] (integer)
* job[data][filter][advancedSearch][depthGreaterThanEqual] (integer)
* job[data][filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][filter][advancedSearch][field] (string)
* job[data][filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* job[data][filter][advancedSearch][items] (array)
* job[data][filter][advancedSearch][idEqual] (string)
* job[data][filter][advancedSearch][idIn] (string)
* job[data][filter][advancedSearch][userIdEqual] (string)
* job[data][filter][advancedSearch][userIdIn] (string)
* job[data][filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* job[data][filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* job[data][filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* job[data][filter][advancedSearch][extendedStatusIn] (string)
* job[data][filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* job[data][filter][advancedSearch][not] (boolean)
* job[data][filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* job[data][filter][advancedSearch][metadataProfileId] (integer)
* job[data][fromPartnerId] (integer) - Id of the partner to copy from
* job[data][toPartnerId] (integer) - Id of the partner to copy to
* job[data][localFileSyncPath] (string)
* job[data][distributionProfileId] (integer)
* job[data][distributionProfile][providerType] (string) - `insertOnly`
* job[data][distributionProfile][name] (string)
* job[data][distributionProfile][status] (integer) - Enum Type: `KalturaDistributionProfileStatus`
* job[data][distributionProfile][submitEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][updateEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][deleteEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][reportEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* job[data][distributionProfile][autoCreateFlavors] (string) - Comma separated flavor params ids that should be auto converted
* job[data][distributionProfile][autoCreateThumb] (string) - Comma separated thumbnail params ids that should be auto generated
* job[data][distributionProfile][optionalFlavorParamsIds] (string) - Comma separated flavor params ids that should be submitted if ready
* job[data][distributionProfile][requiredFlavorParamsIds] (string) - Comma separated flavor params ids that required to be ready before submission
* job[data][distributionProfile][optionalThumbDimensions] (array)
* job[data][distributionProfile][requiredThumbDimensions] (array)
* job[data][distributionProfile][optionalAssetDistributionRules] (array)
* job[data][distributionProfile][requiredAssetDistributionRules] (array)
* job[data][distributionProfile][sunriseDefaultOffset] (integer) - If entry distribution sunrise not specified that will be the default since entry creation time, in seconds
* job[data][distributionProfile][sunsetDefaultOffset] (integer) - If entry distribution sunset not specified that will be the default since entry creation time, in seconds
* job[data][distributionProfile][recommendedStorageProfileForDownload] (integer) - The best external storage to be used to download the asset files from
* job[data][distributionProfile][recommendedDcForDownload] (integer) - The best Kaltura data center to be used to download the asset files to
* job[data][distributionProfile][recommendedDcForExecute] (integer) - The best Kaltura data center to be used to execute the distribution job
* job[data][distributionProfile][objectType] (string)
* job[data][distributionProfile][fieldConfigArray] (array)
* job[data][distributionProfile][itemXpathsToExtend] (array)
* job[data][distributionProfile][useCategoryEntries] (boolean) - When checking custom XSLT conditions using the fieldConfigArray - address only categories associated with the entry via the categoryEntry object
* job[data][distributionProfile][apikey] (string)
* job[data][distributionProfile][email] (string)
* job[data][distributionProfile][sftpPass] (string)
* job[data][distributionProfile][sftpLogin] (string)
* job[data][distributionProfile][accountId] (string)
* job[data][distributionProfile][metadataProfileId] (integer)
* job[data][distributionProfile][genericProviderId] (integer) - `insertOnly`
* job[data][distributionProfile][submitAction][protocol] (integer) - Enum Type: `KalturaDistributionProtocol`
* job[data][distributionProfile][submitAction][serverUrl] (string)
* job[data][distributionProfile][submitAction][serverPath] (string)
* job[data][distributionProfile][submitAction][username] (string)
* job[data][distributionProfile][submitAction][password] (string)
* job[data][distributionProfile][submitAction][ftpPassiveMode] (boolean)
* job[data][distributionProfile][submitAction][httpFieldName] (string)
* job[data][distributionProfile][submitAction][httpFileName] (string)
* job[data][distributionProfile][xsl] (string)
* job[data][distributionProfile][ftpHost] (string)
* job[data][distributionProfile][ftpUsername] (string)
* job[data][distributionProfile][ftpPassword] (string)
* job[data][distributionProfile][ftpPath] (string)
* job[data][distributionProfile][channelTitle] (string)
* job[data][distributionProfile][flavorAssetFilenameXslt] (string)
* job[data][distributionProfile][thumbnailAssetFilenameXslt] (string)
* job[data][distributionProfile][assetFilenameXslt] (string)
* job[data][distributionProfile][feedTitle] (string)
* job[data][distributionProfile][feedLink] (string)
* job[data][distributionProfile][feedDescription] (string)
* job[data][distributionProfile][feedLastBuildDate] (string)
* job[data][distributionProfile][itemLink] (string)
* job[data][distributionProfile][cPlatformTvSeries] (array)
* job[data][distributionProfile][cPlatformTvSeriesField] (string)
* job[data][distributionProfile][shouldIncludeCuePoints] (boolean)
* job[data][distributionProfile][shouldIncludeCaptions] (boolean)
* job[data][distributionProfile][shouldAddThumbExtension] (boolean)
* job[data][distributionProfile][targetServiceUrl] (string)
* job[data][distributionProfile][targetAccountId] (integer)
* job[data][distributionProfile][targetLoginId] (string)
* job[data][distributionProfile][targetLoginPassword] (string)
* job[data][distributionProfile][metadataXslt] (string)
* job[data][distributionProfile][metadataXpathsTriggerUpdate] (array)
* job[data][distributionProfile][distributeCaptions] (boolean)
* job[data][distributionProfile][distributeCuePoints] (boolean)
* job[data][distributionProfile][distributeRemoteFlavorAssetContent] (boolean)
* job[data][distributionProfile][distributeRemoteThumbAssetContent] (boolean)
* job[data][distributionProfile][distributeRemoteCaptionAssetContent] (boolean)
* job[data][distributionProfile][mapAccessControlProfileIds] (array)
* job[data][distributionProfile][mapConversionProfileIds] (array)
* job[data][distributionProfile][mapMetadataProfileIds] (array)
* job[data][distributionProfile][mapStorageProfileIds] (array)
* job[data][distributionProfile][mapFlavorParamsIds] (array)
* job[data][distributionProfile][mapThumbParamsIds] (array)
* job[data][distributionProfile][mapCaptionParamsIds] (array)
* job[data][distributionProfile][user] (string)
* job[data][distributionProfile][password] (string)
* job[data][distributionProfile][geoBlockingMapping] (integer) - Enum Type: `KalturaDailymotionGeoBlockingMapping`
* job[data][distributionProfile][channelLink] (string)
* job[data][distributionProfile][channelDescription] (string)
* job[data][distributionProfile][cuePointsProvider] (string)
* job[data][distributionProfile][itemsPerPage] (string)
* job[data][distributionProfile][ignoreSchedulingInFeed] (boolean)
* job[data][distributionProfile][apiAuthorizeUrl] (string)
* job[data][distributionProfile][pageId] (string)
* job[data][distributionProfile][pageAccessToken] (string)
* job[data][distributionProfile][userAccessToken] (string)
* job[data][distributionProfile][state] (string)
* job[data][distributionProfile][permissions] (string)
* job[data][distributionProfile][reRequestPermissions] (integer)
* job[data][distributionProfile][contentOwner] (string)
* job[data][distributionProfile][upstreamVideoId] (string)
* job[data][distributionProfile][upstreamNetworkName] (string)
* job[data][distributionProfile][upstreamNetworkId] (string)
* job[data][distributionProfile][categoryId] (string)
* job[data][distributionProfile][replaceGroup] (boolean)
* job[data][distributionProfile][replaceAirDates] (boolean)
* job[data][distributionProfile][protocol] (integer) - `insertOnly`
* job[data][distributionProfile][host] (string)
* job[data][distributionProfile][port] (integer)
* job[data][distributionProfile][basePath] (string)
* job[data][distributionProfile][username] (string)
* job[data][distributionProfile][passphrase] (string)
* job[data][distributionProfile][sftpPublicKey] (string)
* job[data][distributionProfile][sftpPrivateKey] (string)
* job[data][distributionProfile][disableMetadata] (boolean)
* job[data][distributionProfile][metadataFilenameXslt] (string)
* job[data][distributionProfile][asperaPublicKey] (string)
* job[data][distributionProfile][asperaPrivateKey] (string)
* job[data][distributionProfile][sendMetadataAfterAssets] (boolean)
* job[data][distributionProfile][sftpHost] (string)
* job[data][distributionProfile][seriesChannel] (string)
* job[data][distributionProfile][seriesPrimaryCategory] (string)
* job[data][distributionProfile][seriesAdditionalCategories] (array)
* job[data][distributionProfile][seasonNumber] (string)
* job[data][distributionProfile][seasonSynopsis] (string)
* job[data][distributionProfile][seasonTuneInInformation] (string)
* job[data][distributionProfile][videoMediaType] (string)
* job[data][distributionProfile][disableEpisodeNumberCustomValidation] (boolean)
* job[data][distributionProfile][asperaHost] (string)
* job[data][distributionProfile][asperaLogin] (string)
* job[data][distributionProfile][asperaPass] (string)
* job[data][distributionProfile][domain] (string)
* job[data][distributionProfile][ftpLogin] (string)
* job[data][distributionProfile][ftpPass] (string)
* job[data][distributionProfile][providerName] (string)
* job[data][distributionProfile][providerId] (string)
* job[data][distributionProfile][copyright] (string)
* job[data][distributionProfile][entitlements] (string)
* job[data][distributionProfile][rating] (string)
* job[data][distributionProfile][itemType] (string)
* job[data][distributionProfile][csId] (string)
* job[data][distributionProfile][source] (string)
* job[data][distributionProfile][sourceFriendlyName] (string)
* job[data][distributionProfile][pageGroup] (string)
* job[data][distributionProfile][sourceFlavorParamsId] (integer)
* job[data][distributionProfile][wmvFlavorParamsId] (integer)
* job[data][distributionProfile][flvFlavorParamsId] (integer)
* job[data][distributionProfile][slFlavorParamsId] (integer)
* job[data][distributionProfile][slHdFlavorParamsId] (integer)
* job[data][distributionProfile][msnvideoCat] (string)
* job[data][distributionProfile][msnvideoTop] (string)
* job[data][distributionProfile][msnvideoTopCat] (string)
* job[data][distributionProfile][channelLanguage] (string)
* job[data][distributionProfile][channelCopyright] (string)
* job[data][distributionProfile][channelImageTitle] (string)
* job[data][distributionProfile][channelImageUrl] (string)
* job[data][distributionProfile][channelImageLink] (string)
* job[data][distributionProfile][itemMediaRating] (string)
* job[data][distributionProfile][ips] (string)
* job[data][distributionProfile][certificateKey] (string)
* job[data][distributionProfile][bodyXslt] (string)
* job[data][distributionProfile][sftpBasePath] (string)
* job[data][distributionProfile][channelManagingEditor] (string)
* job[data][distributionProfile][channelImageWidth] (string)
* job[data][distributionProfile][channelImageHeight] (string)
* job[data][distributionProfile][channelGenerator] (string)
* job[data][distributionProfile][channelRating] (string)
* job[data][distributionProfile][feedSubtitle] (string)
* job[data][distributionProfile][feedAuthorName] (string)
* job[data][distributionProfile][feedLanguage] (string)
* job[data][distributionProfile][feedCopyright] (string)
* job[data][distributionProfile][feedImageTitle] (string)
* job[data][distributionProfile][feedImageUrl] (string)
* job[data][distributionProfile][feedImageLink] (string)
* job[data][distributionProfile][feedImageWidth] (integer)
* job[data][distributionProfile][feedImageHeight] (integer)
* job[data][distributionProfile][ingestUrl] (string)
* job[data][distributionProfile][tags] (array)
* job[data][distributionProfile][xsltFile] (string)
* job[data][distributionProfile][domainName] (string) - The name of the Domain that the Upload User should have access to, Used for authentication.
* job[data][distributionProfile][channelGuid] (string) - The Channel GUID assigned to this Publication Rule. Must be a valid Channel in the Domain that was used in authentication.
* job[data][distributionProfile][apiHostUrl] (string) - The API host URL that the Upload User should have access to, Used for HTTP content submission.
* job[data][distributionProfile][domainGuid] (string) - The GUID of the Customer Domain in the Unicorn system obtained by contacting your Unicorn representative.
* job[data][distributionProfile][adFreeApplicationGuid] (string) - The GUID for the application in which to record metrics and enforce business rules obtained through your Unicorn representative.
* job[data][distributionProfile][remoteAssetParamsId] (integer) - The flavor-params that will be used for the remote asset.
* job[data][distributionProfile][storageProfileId] (string) - The remote storage that should be used for the remote asset.
* job[data][distributionProfile][backgroundImageWide] (string)
* job[data][distributionProfile][backgroundImageStandard] (string)
* job[data][distributionProfile][entitlement] (string)
* job[data][distributionProfile][priority] (string)
* job[data][distributionProfile][allowStreaming] (string)
* job[data][distributionProfile][streamingPriceCode] (string)
* job[data][distributionProfile][allowDownload] (string)
* job[data][distributionProfile][downloadPriceCode] (string)
* job[data][distributionProfile][contactTelephone] (string)
* job[data][distributionProfile][contactEmail] (string)
* job[data][distributionProfile][processFeed] (integer) - Enum Type: `KalturaYahooDistributionProcessFeedActionStatus`
* job[data][distributionProfile][feedSpecVersion] (string) - Enum Type: `KalturaYouTubeDistributionFeedSpecVersion`
* job[data][distributionProfile][notificationEmail] (string)
* job[data][distributionProfile][sftpPort] (integer)
* job[data][distributionProfile][sftpBaseDir] (string)
* job[data][distributionProfile][ownerName] (string)
* job[data][distributionProfile][defaultCategory] (string)
* job[data][distributionProfile][allowComments] (string)
* job[data][distributionProfile][allowEmbedding] (string)
* job[data][distributionProfile][allowRatings] (string)
* job[data][distributionProfile][allowResponses] (string)
* job[data][distributionProfile][commercialPolicy] (string)
* job[data][distributionProfile][ugcPolicy] (string)
* job[data][distributionProfile][target] (string)
* job[data][distributionProfile][adServerPartnerId] (string)
* job[data][distributionProfile][enableAdServer] (boolean)
* job[data][distributionProfile][allowPreRollAds] (boolean)
* job[data][distributionProfile][allowPostRollAds] (boolean)
* job[data][distributionProfile][strict] (string)
* job[data][distributionProfile][overrideManualEdits] (string)
* job[data][distributionProfile][urgentReference] (string)
* job[data][distributionProfile][allowSyndication] (string)
* job[data][distributionProfile][hideViewCount] (string)
* job[data][distributionProfile][allowAdsenseForVideo] (string)
* job[data][distributionProfile][allowInvideo] (string)
* job[data][distributionProfile][allowMidRollAds] (boolean)
* job[data][distributionProfile][instreamStandard] (string)
* job[data][distributionProfile][instreamTrueview] (string)
* job[data][distributionProfile][claimType] (string)
* job[data][distributionProfile][blockOutsideOwnership] (string)
* job[data][distributionProfile][captionAutosync] (string)
* job[data][distributionProfile][deleteReference] (boolean)
* job[data][distributionProfile][releaseClaims] (boolean)
* job[data][distributionProfile][googleClientId] (string)
* job[data][distributionProfile][googleClientSecret] (string)
* job[data][distributionProfile][googleTokenData] (string)
* job[data][distributionProfile][assumeSuccess] (boolean)
* job[data][distributionProfile][privacyStatus] (string)
* job[data][dropFolderId] (integer)
* job[data][dropFolderFileIds] (string)
* job[data][parsedSlug] (string)
* job[data][contentMatchPolicy] (integer) - Enum Type: `KalturaDropFolderContentFileHandlerMatchPolicy`
* job[data][conversionProfileId] (integer)
* job[data][parsedUserId] (string)
* job[data][templateId] (integer)
* job[data][contentParameters] (array)
* job[data][srcFileUrl] (string)
* job[data][destFileLocalPath] (string)
* job[data][fileSize] (integer)
* job[data][metadataId] (integer)
* job[data][changedCategoryId] (integer)
* job[data][deletedPrivacyContexts] (string)
* job[data][addedPrivacyContexts] (string)
* job[data][providerType] (string) - Enum Type: `KalturaIntegrationProviderType`
* job[data][providerData][objectType] (string)
* job[data][providerData][entryId] (string) - Entry ID
* job[data][providerData][flavorAssetId] (string) - Flavor ID
* job[data][providerData][captionAssetFormats] (string) - Caption formats
* job[data][providerData][priority] (string) - Enum Type: `KalturaCielo24Priority`
* job[data][providerData][fidelity] (string) - Enum Type: `KalturaCielo24Fidelity`
* job[data][providerData][spokenLanguage] (string) - Enum Type: `KalturaLanguage`
* job[data][providerData][replaceMediaContent] (boolean) - should replace remote media content
* job[data][providerData][additionalParameters] (string) - additional parameters to send to Cielo24
* job[data][providerData][metadataProfileId] (integer) - ID of the metadata profile for the extracted term metadata
* job[data][providerData][transcriptAssetId] (string) - ID of the transcript asset
* job[data][providerData][voicebaseApiKey] (string) - Voicebase API key to fetch transcript tokens
* job[data][providerData][voicebaseApiPassword] (string) - Voicebase API password to fetch transcript tokens
* job[data][providerData][exampleUrl] (string) - Just an example
* job[data][providerData][transcriptId] (string) - input Transcript-asset ID
* job[data][timeReference] (integer)
* job[data][timeZoneOffset] (integer)
* job[data][outputPath] (string)
* job[data][recipientEmail] (string)
* job[data][vodEntryId] (string) - $vod Entry Id
* job[data][liveEntryId] (string) - live Entry Id
* job[data][totalVodDuration] (number) - total VOD Duration
* job[data][lastSegmentDuration] (number) - last Segment Duration
* job[data][amfArray] (string) - amf Array File Path
* job[data][lastCuePointSyncTime] (integer) - last live to vod sync time
* job[data][lastSegmentDrift] (integer) - last segment drift
* job[data][mailType] (string) - Enum Type: `KalturaMailType`
* job[data][mailPriority] (integer)
* job[data][status] (integer) - Enum Type: `KalturaMailJobStatus`
* job[data][recipientName] (string)
* job[data][recipientId] (integer) - kuserId
* job[data][fromName] (string)
* job[data][fromEmail] (string)
* job[data][bodyParams] (string)
* job[data][subjectParams] (string)
* job[data][templatePath] (string)
* job[data][language] (string) - Enum Type: `KalturaLanguageCode`
* job[data][campaignId] (integer)
* job[data][minSendDate] (integer)
* job[data][isHtml] (boolean)
* job[data][separator] (string)
* job[data][srcCategoryId] (integer) - Source category id
* job[data][destCategoryId] (integer) - Destination category id
* job[data][lastMovedCategoryId] (integer) - Saves the last category id that its entries moved completely
* job[data][lastMovedCategoryPageIndex] (integer) - Saves the last page index of the child categories filter pager
* job[data][lastMovedCategoryEntryPageIndex] (integer) - Saves the last page index of the category entries filter pager
* job[data][moveFromChildren] (boolean) - All entries from all child categories will be moved as well
* job[data][destCategoryFullIds] (string) - Destination categories fallback ids
* job[data][userId] (string)
* job[data][type] (integer) - Enum Type: `KalturaNotificationType`
* job[data][typeAsString] (string)
* job[data][objectId] (string)
* job[data][data] (string)
* job[data][numberOfAttempts] (integer)
* job[data][notificationResult] (string)
* job[data][objType] (integer) - Enum Type: `KalturaNotificationObjectType`
* job[data][captionAssetId] (string)
* job[data][multiLanaguageCaptionAssetId] (string)
* job[data][fileLocation] (string)
* job[data][streamID] (string)
* job[data][backupStreamID] (string)
* job[data][rtmp] (string)
* job[data][encoderIP] (string)
* job[data][backupEncoderIP] (string)
* job[data][encoderPassword] (string)
* job[data][encoderUsername] (string)
* job[data][endDate] (integer)
* job[data][returnVal] (string)
* job[data][mediaType] (integer)
* job[data][primaryBroadcastingUrl] (string)
* job[data][secondaryBroadcastingUrl] (string)
* job[data][streamName] (string)
* job[data][maxResults] (integer)
* job[data][resultsFilePath] (string)
* job[data][referenceTime] (integer)
* job[data][serverUrl] (string)
* job[data][serverUsername] (string)
* job[data][serverPassword] (string)
* job[data][serverPrivateKey] (string)
* job[data][serverPublicKey] (string)
* job[data][serverPassPhrase] (string)
* job[data][ftpPassiveMode] (boolean)
* job[data][srcFileSyncId] (string)
* job[data][destFileSyncStoredPath] (string)
* job[data][categoryId] (integer) - category id
* job[data][lastUpdatedCategoryEntryCreatedAt] (integer) - Saves the last category entry creation date that was updated
* job[data][lastUpdatedCategoryCreatedAt] (integer) - Saves the last sub category creation date that was updated
* job[data][srcXslPath] (string)
* job[data][srcVersion] (integer)
* job[data][destVersion] (integer)
* job[data][destXsdPath] (string)
* job[data][metadataProfileId] (integer)
* job[data][scanResult] (integer) - Enum Type: `KalturaVirusScanJobResult`
* job[data][virusFoundAction] (integer) - Enum Type: `KalturaVirusFoundAction`
* job[data][syncMode] (integer) - Enum Type: `KalturaWidevineRepositorySyncMode`
* job[data][wvAssetIds] (string)
* job[data][modifiedAttributes] (string)
* job[data][monitorSyncCompletion] (integer)
* job[data][columns] (array)
* job[data][eventsType] (integer) - Enum Type: `KalturaScheduleEventType`
* job[data][destDirLocalPath] (string)
* job[data][destDirRemoteUrl] (string)
* job[data][destFileName] (string)
* job[data][inputXmlLocalPath] (string)
* job[data][inputXmlRemoteUrl] (string)
* job[data][commandLinesStr] (string)
* job[data][flavors] (array)
* job[data][destFileSyncLocalPath] (string)
* job[data][destFileSyncRemoteUrl] (string)
* job[data][logFileSyncLocalPath] (string)
* job[data][logFileSyncRemoteUrl] (string)
* job[data][remoteMediaId] (string)
* job[data][customData] (string)
* job[data][extraDestFileSyncs] (array)
* job[data][engineMessage] (string)
* job[data][calculateComplexity] (boolean)
* job[data][extractId3Tags] (boolean)
* job[data][detectGOP] (integer)
* job[data][createThumb] (boolean) - Indicates if a thumbnail should be created
* job[data][thumbOffset] (integer) - The position of the thumbnail in the media file
* job[data][keepDistributionItem] (boolean) - Flag signifying that the associated distribution item should not be moved to 'removed' status
* job[data][plays] (integer)
* job[data][views] (integer)
* job[data][description] (string)
* job[data][webexHostId] (string)
* job[data][server][name] (string)
* job[data][server][systemName] (string)
* job[data][server][description] (string)
* job[data][server][dc] (integer) - The dc of the server
* job[data][server][objectType] (string)
* job[data][server][host] (string)
* job[data][server][port] (integer)
* job[data][server][protocol] (string) - Enum Type: `KalturaActivitiBusinessProcessServerProtocol`
* job[data][server][username] (string)
* job[data][server][password] (string)
* job[data][to][objectType] (string)
* job[data][to][categoryUserFilter][orderBy] (string)
* job[data][to][categoryUserFilter][categoryIdEqual] (integer)
* job[data][to][categoryUserFilter][categoryIdIn] (string)
* job[data][to][categoryUserFilter][userIdEqual] (string)
* job[data][to][categoryUserFilter][userIdIn] (string)
* job[data][to][categoryUserFilter][permissionLevelEqual] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* job[data][to][categoryUserFilter][permissionLevelIn] (string)
* job[data][to][categoryUserFilter][statusEqual] (integer) - Enum Type: `KalturaCategoryUserStatus`
* job[data][to][categoryUserFilter][statusIn] (string)
* job[data][to][categoryUserFilter][createdAtGreaterThanOrEqual] (integer)
* job[data][to][categoryUserFilter][createdAtLessThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updatedAtGreaterThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updatedAtLessThanOrEqual] (integer)
* job[data][to][categoryUserFilter][updateMethodEqual] (integer) - Enum Type: `KalturaUpdateMethodType`
* job[data][to][categoryUserFilter][updateMethodIn] (string)
* job[data][to][categoryUserFilter][categoryFullIdsStartsWith] (string)
* job[data][to][categoryUserFilter][categoryFullIdsEqual] (string)
* job[data][to][categoryUserFilter][permissionNamesMatchAnd] (string)
* job[data][to][categoryUserFilter][permissionNamesMatchOr] (string)
* job[data][to][categoryUserFilter][permissionNamesNotContains] (string)
* job[data][to][categoryUserFilter][categoryDirectMembers] (boolean) - Return the list of categoryUser that are not inherited from parent category - only the direct categoryUsers.
* job[data][to][categoryUserFilter][freeText] (string) - Free text search on user id or screen name
* job[data][to][categoryUserFilter][relatedGroupsByUserId] (string) - Return a list of categoryUser that related to the userId in this field by groups
* job[data][to][emailRecipients] (array)
* job[data][to][filter][orderBy] (string)
* job[data][to][filter][partnerIdEqual] (integer)
* job[data][to][filter][typeEqual] (integer) - Enum Type: `KalturaUserType`
* job[data][to][filter][typeIn] (string)
* job[data][to][filter][screenNameLike] (string)
* job[data][to][filter][screenNameStartsWith] (string)
* job[data][to][filter][emailLike] (string)
* job[data][to][filter][emailStartsWith] (string)
* job[data][to][filter][tagsMultiLikeOr] (string)
* job[data][to][filter][tagsMultiLikeAnd] (string)
* job[data][to][filter][statusEqual] (integer) - Enum Type: `KalturaUserStatus`
* job[data][to][filter][statusIn] (string)
* job[data][to][filter][createdAtGreaterThanOrEqual] (integer)
* job[data][to][filter][createdAtLessThanOrEqual] (integer)
* job[data][to][filter][firstNameStartsWith] (string)
* job[data][to][filter][lastNameStartsWith] (string)
* job[data][to][filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][to][filter][idOrScreenNameStartsWith] (string)
* job[data][to][filter][idEqual] (string)
* job[data][to][filter][idIn] (string)
* job[data][to][filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* job[data][to][filter][roleIdEqual] (string)
* job[data][to][filter][roleIdsEqual] (string)
* job[data][to][filter][roleIdsIn] (string)
* job[data][to][filter][firstNameOrLastNameStartsWith] (string)
* job[data][to][filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* job[data][to][filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* job[data][to][filter][objectType] (string)
* job[data][url] (string) - Remote server URL
* job[data][method] (integer) - Enum Type: `KalturaHttpNotificationMethod`
* job[data][timeout] (integer) - The maximum number of seconds to allow cURL functions to execute.
* job[data][connectTimeout] (integer) - The number of seconds to wait while trying to connect.
* job[data][username] (string) - A username to use for the connection.
* job[data][password] (string) - A password to use for the connection.
* job[data][authenticationMethod] (integer) - Enum Type: `KalturaHttpNotificationAuthenticationMethod`
* job[data][sslVersion] (integer) - Enum Type: `KalturaHttpNotificationSslVersion`
* job[data][sslCertificate] (string) - SSL certificate to verify the peer with.
* job[data][sslCertificateType] (string) - Enum Type: `KalturaHttpNotificationCertificateType`
* job[data][sslCertificatePassword] (string) - The password required to use the certificate.
* job[data][sslEngine] (string) - The identifier for the crypto engine of the private SSL key specified in ssl key.
* job[data][sslEngineDefault] (string) - The identifier for the crypto engine used for asymmetric crypto operations.
* job[data][sslKeyType] (string) - Enum Type: `KalturaHttpNotificationSslKeyType`
* job[data][sslKey] (string) - Private SSL key.
* job[data][sslKeyPassword] (string) - The secret password needed to use the private SSL key specified in ssl key.
* job[data][customHeaders] (array)
* job[data][signSecret] (string) - The secret to sign the notification with
* job[data][privateKey] (string)
* job[data][publicKey] (string)
* job[data][passPhrase] (string)
* job[data][dropFolderFileId] (integer)
* job[data][wsdlUsername] (string)
* job[data][wsdlPassword] (string)
* job[data][cpcode] (string)
* job[data][emailId] (string)
* job[data][primaryContact] (string)
* job[data][secondaryContact] (string)
* job[data][streamId] (integer)
* job[data][systemUserName] (string)
* job[data][systemPassword] (string)
* job[data][domainName] (string)
* job[data][dvrEnabled] (integer) - Enum Type: `KalturaDVRStatus`
* job[data][dvrWindow] (integer)
* job[data][streamType] (string) - Enum Type: `KalturaAkamaiUniversalStreamType`
* job[data][notificationEmail] (string)
* job[data][provisioningParams] (array)
* job[data][userName] (string)
* job[data][protocol] (string) - http / https
* job[data][ksType] (integer) - Enum Type: `KalturaSessionType`
* job[data][userRoles] (array)
* job[data][cachedObjectType] (string) - Class name
* job[data][startObjectKey] (string)
* job[data][endObjectKey] (string)
* job[data][force] (boolean)
* job[data][createLink] (boolean)
* job[data][contentMoid] (string) - Unique Kontiki MOID for the content uploaded to Kontiki
* job[data][serviceToken] (string)
* job[data][filesPermissionInS3] (string) - Enum Type: `KalturaAmazonS3StorageProfileFilesPermissionLevel`
* job[data][s3Region] (string)
* job[data][sseType] (string)
* job[data][sseKmsKeyId] (string)
* job[data][signatureType] (string)
* job[data][endPoint] (string)

### batch.updatePartnerLoadTable
batch updatePartnerLoadTable action cleans the partner load table


```js
kaltura.batch.updatePartnerLoadTable({}, context)
```


### batchcontrol.configLoaded
batch configLoaded action saves the configuration as loaded by a remote scheduler


```js
kaltura.batchcontrol.configLoaded({
  "configParam": "",
  "configValue": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduler[configuredId] (integer) - The id as configured in the batch config
* scheduler[name] (string) - The scheduler name
* scheduler[host] (string) - The host name
* scheduler[statuses] (array)
* scheduler[configs] (array)
* scheduler[workers] (array)
* configParam (string) **required** - The parameter that was loaded
* configValue (string) **required** - The value that was loaded
* configParamPart (string) - The parameter part that was loaded
* workerConfigId (integer) - The id of the job that the configuration refers to, not mandatory if the configuration refers to the scheduler
* workerName (string) - The name of the job that the configuration refers to, not mandatory if the configuration refers to the scheduler

### batchcontrol.getCommand
batch getCommand action returns the command with its current status


```js
kaltura.batchcontrol.getCommand({
  "commandId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* commandId (integer) **required** - The id of the command

### batchcontrol.getFullStatus
batch getFullStatus action returns the status of all schedulers and queues


```js
kaltura.batchcontrol.getFullStatus({}, context)
```


### batchcontrol.kill
batch kill action forces stop og a batch on a remote scheduler


```js
kaltura.batchcontrol.kill({
  "workerId": 0,
  "batchIndex": 0,
  "adminId": 0,
  "cause": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* workerId (integer) **required** - The id of the job to be stopped
* batchIndex (integer) **required** - The index of the batch job process to be stopped
* adminId (integer) **required** - The id of the admin that called the stop
* cause (string) **required** - The reason it was stopped

### batchcontrol.listCommands
list batch control commands


```js
kaltura.batchcontrol.listCommands({}, context)
```


### batchcontrol.listSchedulers
list all Schedulers


```js
kaltura.batchcontrol.listSchedulers({}, context)
```


### batchcontrol.listWorkers
list all Workers


```js
kaltura.batchcontrol.listWorkers({}, context)
```


### batchcontrol.reportStatus
batch reportStatus action saves the a status attribute from a remote scheduler and returns pending commands for the scheduler


```js
kaltura.batchcontrol.reportStatus({}, context)
```


### batchcontrol.setCommandResult
batch setCommandResult action saves the results of a command as recieved from a remote scheduler


```js
kaltura.batchcontrol.setCommandResult({
  "commandId": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* commandId (integer) **required** - The id of the command
* status (integer) **required** - Enum Type: `KalturaControlPanelCommandStatus`
* errorDescription (string) - The description, important for failed commands

### batchcontrol.setSchedulerConfig
batch sets a configuration parameter to be loaded by a scheduler


```js
kaltura.batchcontrol.setSchedulerConfig({
  "schedulerId": 0,
  "adminId": 0,
  "configParam": "",
  "configValue": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* schedulerId (integer) **required** - The id of the remote scheduler location
* adminId (integer) **required** - The id of the admin that called the setConfig
* configParam (string) **required** - The parameter to be set
* configValue (string) **required** - The value to be set
* configParamPart (string) - The parameter part to be set - for additional params
* cause (string) - The reason it was changed

### batchcontrol.setWorkerConfig
batch sets a configuration parameter to be loaded by a worker


```js
kaltura.batchcontrol.setWorkerConfig({
  "workerId": 0,
  "adminId": 0,
  "configParam": "",
  "configValue": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* workerId (integer) **required** - The id of the job to be configured
* adminId (integer) **required** - The id of the admin that called the setConfig
* configParam (string) **required** - The parameter to be set
* configValue (string) **required** - The value to be set
* configParamPart (string) - The parameter part to be set - for additional params
* cause (string) - The reason it was changed

### batchcontrol.startWorker
batch start action starts a job


```js
kaltura.batchcontrol.startWorker({
  "workerId": 0,
  "adminId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* workerId (integer) **required** - The id of the job to be started
* adminId (integer) **required** - The id of the admin that called the start
* cause (string) - The reason it was started

### batchcontrol.stopScheduler
batch stop action stops a scheduler


```js
kaltura.batchcontrol.stopScheduler({
  "schedulerId": 0,
  "adminId": 0,
  "cause": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* schedulerId (integer) **required** - The id of the remote scheduler location
* adminId (integer) **required** - The id of the admin that called the stop
* cause (string) **required** - The reason it was stopped

### batchcontrol.stopWorker
batch stop action stops a worker


```js
kaltura.batchcontrol.stopWorker({
  "workerId": 0,
  "adminId": 0,
  "cause": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* workerId (integer) **required** - The id of the job to be stopped
* adminId (integer) **required** - The id of the admin that called the stop
* cause (string) **required** - The reason it was stopped

### bulkUpload.abort
Aborts the bulk upload and all its child jobs


```js
kaltura.bulkUpload.abort({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### bulkUpload.add
Add new bulk upload batch job

Conversion profile id can be specified in the API or in the CSV file, the one in the CSV file will be stronger.

If no conversion profile was specified, partner's default will be used


```js
kaltura.bulkUpload.add({
  "conversionProfileId": 0,
  "csvFileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* conversionProfileId (integer) **required** - Convertion profile id to use for converting the current bulk (-1 to use partner's default)
* csvFileData (string) **required** - bulk upload file
* bulkUploadType (string) - Enum Type: `KalturaBulkUploadType`
* uploadedBy (string)
* fileName (string) - Friendly name of the file, used to be recognized later in the logs.

### bulkUpload.get
Get bulk upload batch job by id


```js
kaltura.bulkUpload.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### bulkUpload.list
List bulk upload batch jobs


```js
kaltura.bulkUpload.list({}, context)
```


### bulkUpload.serve
serve action returan the original file.


```js
kaltura.bulkUpload.serve({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### bulkUpload.serveLog
serveLog action returan the original file.


```js
kaltura.bulkUpload.serveLog({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### bulk.abort
Aborts the bulk upload and all its child jobs


```js
kaltura.bulk.abort({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### bulk.get
Get bulk upload batch job by id


```js
kaltura.bulk.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### bulk.list
List bulk upload batch jobs


```js
kaltura.bulk.list({}, context)
```


### bulk.serve
serve action returns the original file.


```js
kaltura.bulk.serve({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### bulk.serveLog
serveLog action returns the log file for the bulk-upload job.


```js
kaltura.bulk.serveLog({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - job id

### businessProcessCase.abort
Abort business-process case


```js
kaltura.businessProcessCase.abort({
  "objectType": "",
  "objectId": "",
  "businessProcessStartNotificationTemplateId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* objectType (string) **required** - Enum Type: `KalturaEventNotificationEventObjectType`
* objectId (string) **required**
* businessProcessStartNotificationTemplateId (integer) **required**

### businessProcessCase.list
list business-process cases


```js
kaltura.businessProcessCase.list({
  "objectType": "",
  "objectId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* objectType (string) **required** - Enum Type: `KalturaEventNotificationEventObjectType`
* objectId (string) **required**

### businessProcessCase.serveDiagram
Server business-process case diagram


```js
kaltura.businessProcessCase.serveDiagram({
  "objectType": "",
  "objectId": "",
  "businessProcessStartNotificationTemplateId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* objectType (string) **required** - Enum Type: `KalturaEventNotificationEventObjectType`
* objectId (string) **required**
* businessProcessStartNotificationTemplateId (integer) **required**

### businessProcessServer.add
Allows you to add a new Business-Process server object


```js
kaltura.businessProcessServer.add({}, context)
```


### businessProcessServer.delete
Delete an Business-Process server object


```js
kaltura.businessProcessServer.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### businessProcessServer.get
Retrieve an Business-Process server object by id


```js
kaltura.businessProcessServer.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### businessProcessServer.list
list Business-Process server objects


```js
kaltura.businessProcessServer.list({}, context)
```


### businessProcessServer.update
Update an existing Business-Process server object


```js
kaltura.businessProcessServer.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* businessProcessServer[name] (string)
* businessProcessServer[systemName] (string)
* businessProcessServer[description] (string)
* businessProcessServer[dc] (integer) - The dc of the server
* businessProcessServer[objectType] (string)
* businessProcessServer[host] (string)
* businessProcessServer[port] (integer)
* businessProcessServer[protocol] (string) - Enum Type: `KalturaActivitiBusinessProcessServerProtocol`
* businessProcessServer[username] (string)
* businessProcessServer[password] (string)

### businessProcessServer.updateStatus
Update Business-Process server status by id


```js
kaltura.businessProcessServer.updateStatus({
  "id": 0,
  "status": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* status (string) **required** - Enum Type: `KalturaBusinessProcessServerStatus`

### captionAsset.add
Add caption asset


```js
kaltura.captionAsset.add({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* captionAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* captionAsset[fileExt] (string) - `insertOnly`
* captionAsset[partnerData] (string) - Partner private data
* captionAsset[partnerDescription] (string) - Partner friendly description
* captionAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* captionAsset[captionParamsId] (integer) - `insertOnly`
* captionAsset[language] (string) - Enum Type: `KalturaLanguage`
* captionAsset[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* captionAsset[label] (string) - Friendly label
* captionAsset[format] (string) - `insertOnly`
* captionAsset[parentId] (string) - `insertOnly`
* captionAsset[accuracy] (integer) - The Accuracy of the caption content

### captionAsset.delete



```js
kaltura.captionAsset.delete({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**

### captionAsset.get



```js
kaltura.captionAsset.get({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**

### captionAsset.getRemotePaths
Get remote storage existing paths for the asset


```js
kaltura.captionAsset.getRemotePaths({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### captionAsset.getUrl
Get download URL for the asset


```js
kaltura.captionAsset.getUrl({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* storageId (integer)

### captionAsset.list
List caption Assets by filter and pager


```js
kaltura.captionAsset.list({}, context)
```


### captionAsset.serve
Serves caption by its id


```js
kaltura.captionAsset.serve({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**

### captionAsset.serveByEntryId
Serves caption by entry id and thumnail params id


```js
kaltura.captionAsset.serveByEntryId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* captionParamId (integer) - if not set, default caption will be used.

### captionAsset.serveWebVTT
Serves caption by its id converting it to segmented WebVTT


```js
kaltura.captionAsset.serveWebVTT({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**
* segmentDuration (integer)
* segmentIndex (integer)
* localTimestamp (integer)

### captionAsset.setAsDefault
Markss the caption as default and removes that mark from all other caption assets of the entry.


```js
kaltura.captionAsset.setAsDefault({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**

### captionAsset.setContent
Update content of caption asset


```js
kaltura.captionAsset.setContent({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* contentResource[objectType] (string)
* contentResource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[forceAsyncDownload] (boolean) - Force Import Job
* contentResource[assetId] (string) - ID of the source asset
* contentResource[entryId] (string) - ID of the source entry
* contentResource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[objectId] (string) - The object id of the file sync object
* contentResource[version] (string) - The version of the file sync object
* contentResource[resource][objectType] (string)
* contentResource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][assetId] (string) - ID of the source asset
* contentResource[resource][entryId] (string) - ID of the source entry
* contentResource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][objectType] (string)
* contentResource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][objectType] (string)
* contentResource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][resources] (array)
* contentResource[resource][resource][resource][content] (string) - Textual content
* contentResource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resource][resources] (array)
* contentResource[resource][resource][content] (string) - Textual content
* contentResource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resources] (array)
* contentResource[resource][content] (string) - Textual content
* contentResource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][privateKey] (string) - SSH private key
* contentResource[resource][publicKey] (string) - SSH public key
* contentResource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resources] (array)
* contentResource[content] (string) - Textual content
* contentResource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[privateKey] (string) - SSH private key
* contentResource[publicKey] (string) - SSH public key
* contentResource[keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[localFilePath] (string) - Full path to the local file
* contentResource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[fileData] (string) - Represents the $_FILE
* contentResource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### captionAsset.update
Update caption asset


```js
kaltura.captionAsset.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* captionAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* captionAsset[fileExt] (string) - `insertOnly`
* captionAsset[partnerData] (string) - Partner private data
* captionAsset[partnerDescription] (string) - Partner friendly description
* captionAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* captionAsset[captionParamsId] (integer) - `insertOnly`
* captionAsset[language] (string) - Enum Type: `KalturaLanguage`
* captionAsset[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* captionAsset[label] (string) - Friendly label
* captionAsset[format] (string) - `insertOnly`
* captionAsset[parentId] (string) - `insertOnly`
* captionAsset[accuracy] (integer) - The Accuracy of the caption content

### captionParams.add
Add new Caption Params


```js
kaltura.captionParams.add({}, context)
```


### captionParams.delete
Delete Caption Params by ID


```js
kaltura.captionParams.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### captionParams.get
Get Caption Params by ID


```js
kaltura.captionParams.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### captionParams.list
List Caption Params by filter with paging support (By default - all system default params will be listed too)


```js
kaltura.captionParams.list({}, context)
```


### captionParams.update
Update Caption Params by ID


```js
kaltura.captionParams.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* captionParams[partnerId] (integer)
* captionParams[name] (string) - The name of the Flavor Params
* captionParams[systemName] (string) - System name of the Flavor Params
* captionParams[description] (string) - The description of the Flavor Params
* captionParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* captionParams[requiredPermissions] (array)
* captionParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* captionParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* captionParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* captionParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* captionParams[language] (string) - `insertOnly`
* captionParams[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* captionParams[label] (string) - Friendly label
* captionParams[format] (string) - `insertOnly`
* captionParams[sourceParamsId] (integer) - Id of the caption params or the flavor params to be used as source for the caption creation

### captionAssetItem.parse
Parse content of caption asset and index it


```js
kaltura.captionAssetItem.parse({
  "captionAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* captionAssetId (string) **required**

### captionAssetItem.search
Search caption asset items by filter, pager and free text


```js
kaltura.captionAssetItem.search({}, context)
```


### captionAssetItem.searchEntries
Search caption asset items by filter, pager and free text


```js
kaltura.captionAssetItem.searchEntries({}, context)
```


### captureSpace.clientUpdates
Returns latest version and URL


```js
kaltura.captureSpace.clientUpdates({
  "os": "",
  "version": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* os (string) **required**
* version (string) **required**
* hashAlgorithm (string) - Enum Type: `KalturaCaptureSpaceHashAlgorithm`

### captureSpace.serveInstall
Serve installation file


```js
kaltura.captureSpace.serveInstall({
  "os": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* os (string) **required**

### captureSpace.serveUpdate
Serve update file


```js
kaltura.captureSpace.serveUpdate({
  "os": "",
  "version": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* os (string) **required**
* version (string) **required**

### category.add
Add new Category


```js
kaltura.category.add({}, context)
```


### category.addFromBulkUpload



```js
kaltura.category.addFromBulkUpload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries

### category.delete
Delete a Category


```js
kaltura.category.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* moveEntriesToParentCategory (integer) - Enum Type: `KalturaNullableBoolean`

### category.get
Get Category by id


```js
kaltura.category.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### category.index
Index Category by id


```js
kaltura.category.index({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* shouldUpdate (boolean)

### category.list
List all categories


```js
kaltura.category.list({}, context)
```


### category.move
Move categories that belong to the same parent category to a target categroy - enabled only for ks with disable entitlement


```js
kaltura.category.move({
  "categoryIds": "",
  "targetCategoryParentId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryIds (string) **required**
* targetCategoryParentId (integer) **required**

### category.unlockCategories
Unlock categories


```js
kaltura.category.unlockCategories({}, context)
```


### category.update
Update Category


```js
kaltura.category.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* category[parentId] (integer)
* category[name] (string) - The name of the Category. 
* category[description] (string) - Category description
* category[tags] (string) - Category tags
* category[appearInList] (integer) - Enum Type: `KalturaAppearInListType`
* category[privacy] (integer) - Enum Type: `KalturaPrivacyType`
* category[inheritanceType] (integer) - Enum Type: `KalturaInheritanceType`
* category[defaultPermissionLevel] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* category[owner] (string) - Category Owner (User id)
* category[referenceId] (string) - Category external id, controlled and managed by the partner.
* category[contributionPolicy] (integer) - Enum Type: `KalturaContributionPolicyType`
* category[privacyContext] (string) - Set privacy context for search entries that assiged to private and public categories. the entries will be private if the search context is set with those categories.
* category[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* category[partnerData] (string) - Can be used to store various partner related data as a string
* category[defaultOrderBy] (string) - Enum Type: `KalturaCategoryOrderBy`
* category[moderation] (integer) - Enum Type: `KalturaNullableBoolean`
* category[isAggregationCategory] (integer) - Enum Type: `KalturaNullableBoolean`
* category[aggregationCategories] (string) - List of aggregation channels the category belongs to

### categoryEntry.activate
activate CategoryEntry when it is pending moderation


```js
kaltura.categoryEntry.activate({
  "entryId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* categoryId (integer) **required**

### categoryEntry.add
Add new CategoryEntry


```js
kaltura.categoryEntry.add({}, context)
```


### categoryEntry.addFromBulkUpload



```js
kaltura.categoryEntry.addFromBulkUpload({}, context)
```


### categoryEntry.delete
Delete CategoryEntry


```js
kaltura.categoryEntry.delete({
  "entryId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* categoryId (integer) **required**

### categoryEntry.index
Index CategoryEntry by Id


```js
kaltura.categoryEntry.index({
  "entryId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* categoryId (integer) **required**
* shouldUpdate (boolean)

### categoryEntry.list
List all categoryEntry


```js
kaltura.categoryEntry.list({}, context)
```


### categoryEntry.reject
activate CategoryEntry when it is pending moderation


```js
kaltura.categoryEntry.reject({
  "entryId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* categoryId (integer) **required**

### categoryEntry.syncPrivacyContext
update privacy context from the category


```js
kaltura.categoryEntry.syncPrivacyContext({
  "entryId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* categoryId (integer) **required**

### categoryUser.activate
activate CategoryUser


```js
kaltura.categoryUser.activate({
  "categoryId": 0,
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* userId (string) **required**

### categoryUser.add
Add new CategoryUser


```js
kaltura.categoryUser.add({}, context)
```


### categoryUser.addFromBulkUpload



```js
kaltura.categoryUser.addFromBulkUpload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries

### categoryUser.copyFromCategory
Copy all memeber from parent category


```js
kaltura.categoryUser.copyFromCategory({
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**

### categoryUser.deactivate
reject CategoryUser


```js
kaltura.categoryUser.deactivate({
  "categoryId": 0,
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* userId (string) **required**

### categoryUser.delete
Delete a CategoryUser


```js
kaltura.categoryUser.delete({
  "categoryId": 0,
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* userId (string) **required**

### categoryUser.get
Get CategoryUser by id


```js
kaltura.categoryUser.get({
  "categoryId": 0,
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* userId (string) **required**

### categoryUser.index
Index CategoryUser by userid and category id


```js
kaltura.categoryUser.index({
  "userId": "",
  "categoryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required**
* categoryId (integer) **required**
* shouldUpdate (boolean)

### categoryUser.list
List all categories


```js
kaltura.categoryUser.list({}, context)
```


### categoryUser.update
Update CategoryUser by id


```js
kaltura.categoryUser.update({
  "categoryId": 0,
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* userId (string) **required**
* categoryUser[categoryId] (integer) - `insertOnly`
* categoryUser[userId] (string) - `insertOnly`
* categoryUser[permissionLevel] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* categoryUser[updateMethod] (integer) - Enum Type: `KalturaUpdateMethodType`
* categoryUser[permissionNames] (string) - Set of category-related permissions for the current category user.
* override (boolean) - - to override manual changes

### comcastMrss.getFeed



```js
kaltura.comcastMrss.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### contentDistributionBatch.createRequiredJobs
creates all required jobs according to entry distribution dirty flags


```js
kaltura.contentDistributionBatch.createRequiredJobs({}, context)
```


### contentDistributionBatch.getAssetUrl
returns absolute valid url for asset file


```js
kaltura.contentDistributionBatch.getAssetUrl({
  "assetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**

### contentDistributionBatch.updateSunStatus
updates entry distribution sun status in the search engine


```js
kaltura.contentDistributionBatch.updateSunStatus({}, context)
```


### distributionProfile.add
Add new Distribution Profile


```js
kaltura.distributionProfile.add({}, context)
```


### distributionProfile.delete
Delete Distribution Profile by id


```js
kaltura.distributionProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### distributionProfile.get
Get Distribution Profile by id


```js
kaltura.distributionProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### distributionProfile.list
List all distribution providers


```js
kaltura.distributionProfile.list({}, context)
```


### distributionProfile.listByPartner



```js
kaltura.distributionProfile.listByPartner({}, context)
```


### distributionProfile.update
Update Distribution Profile by id


```js
kaltura.distributionProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* distributionProfile[providerType] (string) - `insertOnly`
* distributionProfile[name] (string)
* distributionProfile[status] (integer) - Enum Type: `KalturaDistributionProfileStatus`
* distributionProfile[submitEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* distributionProfile[updateEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* distributionProfile[deleteEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* distributionProfile[reportEnabled] (integer) - Enum Type: `KalturaDistributionProfileActionStatus`
* distributionProfile[autoCreateFlavors] (string) - Comma separated flavor params ids that should be auto converted
* distributionProfile[autoCreateThumb] (string) - Comma separated thumbnail params ids that should be auto generated
* distributionProfile[optionalFlavorParamsIds] (string) - Comma separated flavor params ids that should be submitted if ready
* distributionProfile[requiredFlavorParamsIds] (string) - Comma separated flavor params ids that required to be ready before submission
* distributionProfile[optionalThumbDimensions] (array)
* distributionProfile[requiredThumbDimensions] (array)
* distributionProfile[optionalAssetDistributionRules] (array)
* distributionProfile[requiredAssetDistributionRules] (array)
* distributionProfile[sunriseDefaultOffset] (integer) - If entry distribution sunrise not specified that will be the default since entry creation time, in seconds
* distributionProfile[sunsetDefaultOffset] (integer) - If entry distribution sunset not specified that will be the default since entry creation time, in seconds
* distributionProfile[recommendedStorageProfileForDownload] (integer) - The best external storage to be used to download the asset files from
* distributionProfile[recommendedDcForDownload] (integer) - The best Kaltura data center to be used to download the asset files to
* distributionProfile[recommendedDcForExecute] (integer) - The best Kaltura data center to be used to execute the distribution job
* distributionProfile[objectType] (string)
* distributionProfile[fieldConfigArray] (array)
* distributionProfile[itemXpathsToExtend] (array)
* distributionProfile[useCategoryEntries] (boolean) - When checking custom XSLT conditions using the fieldConfigArray - address only categories associated with the entry via the categoryEntry object
* distributionProfile[apikey] (string)
* distributionProfile[email] (string)
* distributionProfile[sftpPass] (string)
* distributionProfile[sftpLogin] (string)
* distributionProfile[accountId] (string)
* distributionProfile[metadataProfileId] (integer)
* distributionProfile[genericProviderId] (integer) - `insertOnly`
* distributionProfile[submitAction][protocol] (integer) - Enum Type: `KalturaDistributionProtocol`
* distributionProfile[submitAction][serverUrl] (string)
* distributionProfile[submitAction][serverPath] (string)
* distributionProfile[submitAction][username] (string)
* distributionProfile[submitAction][password] (string)
* distributionProfile[submitAction][ftpPassiveMode] (boolean)
* distributionProfile[submitAction][httpFieldName] (string)
* distributionProfile[submitAction][httpFileName] (string)
* distributionProfile[xsl] (string)
* distributionProfile[ftpHost] (string)
* distributionProfile[ftpUsername] (string)
* distributionProfile[ftpPassword] (string)
* distributionProfile[ftpPath] (string)
* distributionProfile[channelTitle] (string)
* distributionProfile[flavorAssetFilenameXslt] (string)
* distributionProfile[thumbnailAssetFilenameXslt] (string)
* distributionProfile[assetFilenameXslt] (string)
* distributionProfile[feedTitle] (string)
* distributionProfile[feedLink] (string)
* distributionProfile[feedDescription] (string)
* distributionProfile[feedLastBuildDate] (string)
* distributionProfile[itemLink] (string)
* distributionProfile[cPlatformTvSeries] (array)
* distributionProfile[cPlatformTvSeriesField] (string)
* distributionProfile[shouldIncludeCuePoints] (boolean)
* distributionProfile[shouldIncludeCaptions] (boolean)
* distributionProfile[shouldAddThumbExtension] (boolean)
* distributionProfile[targetServiceUrl] (string)
* distributionProfile[targetAccountId] (integer)
* distributionProfile[targetLoginId] (string)
* distributionProfile[targetLoginPassword] (string)
* distributionProfile[metadataXslt] (string)
* distributionProfile[metadataXpathsTriggerUpdate] (array)
* distributionProfile[distributeCaptions] (boolean)
* distributionProfile[distributeCuePoints] (boolean)
* distributionProfile[distributeRemoteFlavorAssetContent] (boolean)
* distributionProfile[distributeRemoteThumbAssetContent] (boolean)
* distributionProfile[distributeRemoteCaptionAssetContent] (boolean)
* distributionProfile[mapAccessControlProfileIds] (array)
* distributionProfile[mapConversionProfileIds] (array)
* distributionProfile[mapMetadataProfileIds] (array)
* distributionProfile[mapStorageProfileIds] (array)
* distributionProfile[mapFlavorParamsIds] (array)
* distributionProfile[mapThumbParamsIds] (array)
* distributionProfile[mapCaptionParamsIds] (array)
* distributionProfile[user] (string)
* distributionProfile[password] (string)
* distributionProfile[geoBlockingMapping] (integer) - Enum Type: `KalturaDailymotionGeoBlockingMapping`
* distributionProfile[channelLink] (string)
* distributionProfile[channelDescription] (string)
* distributionProfile[cuePointsProvider] (string)
* distributionProfile[itemsPerPage] (string)
* distributionProfile[ignoreSchedulingInFeed] (boolean)
* distributionProfile[apiAuthorizeUrl] (string)
* distributionProfile[pageId] (string)
* distributionProfile[pageAccessToken] (string)
* distributionProfile[userAccessToken] (string)
* distributionProfile[state] (string)
* distributionProfile[permissions] (string)
* distributionProfile[reRequestPermissions] (integer)
* distributionProfile[contentOwner] (string)
* distributionProfile[upstreamVideoId] (string)
* distributionProfile[upstreamNetworkName] (string)
* distributionProfile[upstreamNetworkId] (string)
* distributionProfile[categoryId] (string)
* distributionProfile[replaceGroup] (boolean)
* distributionProfile[replaceAirDates] (boolean)
* distributionProfile[protocol] (integer) - `insertOnly`
* distributionProfile[host] (string)
* distributionProfile[port] (integer)
* distributionProfile[basePath] (string)
* distributionProfile[username] (string)
* distributionProfile[passphrase] (string)
* distributionProfile[sftpPublicKey] (string)
* distributionProfile[sftpPrivateKey] (string)
* distributionProfile[disableMetadata] (boolean)
* distributionProfile[metadataFilenameXslt] (string)
* distributionProfile[asperaPublicKey] (string)
* distributionProfile[asperaPrivateKey] (string)
* distributionProfile[sendMetadataAfterAssets] (boolean)
* distributionProfile[sftpHost] (string)
* distributionProfile[seriesChannel] (string)
* distributionProfile[seriesPrimaryCategory] (string)
* distributionProfile[seriesAdditionalCategories] (array)
* distributionProfile[seasonNumber] (string)
* distributionProfile[seasonSynopsis] (string)
* distributionProfile[seasonTuneInInformation] (string)
* distributionProfile[videoMediaType] (string)
* distributionProfile[disableEpisodeNumberCustomValidation] (boolean)
* distributionProfile[asperaHost] (string)
* distributionProfile[asperaLogin] (string)
* distributionProfile[asperaPass] (string)
* distributionProfile[domain] (string)
* distributionProfile[ftpLogin] (string)
* distributionProfile[ftpPass] (string)
* distributionProfile[providerName] (string)
* distributionProfile[providerId] (string)
* distributionProfile[copyright] (string)
* distributionProfile[entitlements] (string)
* distributionProfile[rating] (string)
* distributionProfile[itemType] (string)
* distributionProfile[csId] (string)
* distributionProfile[source] (string)
* distributionProfile[sourceFriendlyName] (string)
* distributionProfile[pageGroup] (string)
* distributionProfile[sourceFlavorParamsId] (integer)
* distributionProfile[wmvFlavorParamsId] (integer)
* distributionProfile[flvFlavorParamsId] (integer)
* distributionProfile[slFlavorParamsId] (integer)
* distributionProfile[slHdFlavorParamsId] (integer)
* distributionProfile[msnvideoCat] (string)
* distributionProfile[msnvideoTop] (string)
* distributionProfile[msnvideoTopCat] (string)
* distributionProfile[channelLanguage] (string)
* distributionProfile[channelCopyright] (string)
* distributionProfile[channelImageTitle] (string)
* distributionProfile[channelImageUrl] (string)
* distributionProfile[channelImageLink] (string)
* distributionProfile[itemMediaRating] (string)
* distributionProfile[ips] (string)
* distributionProfile[certificateKey] (string)
* distributionProfile[bodyXslt] (string)
* distributionProfile[sftpBasePath] (string)
* distributionProfile[channelManagingEditor] (string)
* distributionProfile[channelImageWidth] (string)
* distributionProfile[channelImageHeight] (string)
* distributionProfile[channelGenerator] (string)
* distributionProfile[channelRating] (string)
* distributionProfile[feedSubtitle] (string)
* distributionProfile[feedAuthorName] (string)
* distributionProfile[feedLanguage] (string)
* distributionProfile[feedCopyright] (string)
* distributionProfile[feedImageTitle] (string)
* distributionProfile[feedImageUrl] (string)
* distributionProfile[feedImageLink] (string)
* distributionProfile[feedImageWidth] (integer)
* distributionProfile[feedImageHeight] (integer)
* distributionProfile[ingestUrl] (string)
* distributionProfile[tags] (array)
* distributionProfile[xsltFile] (string)
* distributionProfile[domainName] (string) - The name of the Domain that the Upload User should have access to, Used for authentication.
* distributionProfile[channelGuid] (string) - The Channel GUID assigned to this Publication Rule. Must be a valid Channel in the Domain that was used in authentication.
* distributionProfile[apiHostUrl] (string) - The API host URL that the Upload User should have access to, Used for HTTP content submission.
* distributionProfile[domainGuid] (string) - The GUID of the Customer Domain in the Unicorn system obtained by contacting your Unicorn representative.
* distributionProfile[adFreeApplicationGuid] (string) - The GUID for the application in which to record metrics and enforce business rules obtained through your Unicorn representative.
* distributionProfile[remoteAssetParamsId] (integer) - The flavor-params that will be used for the remote asset.
* distributionProfile[storageProfileId] (string) - The remote storage that should be used for the remote asset.
* distributionProfile[backgroundImageWide] (string)
* distributionProfile[backgroundImageStandard] (string)
* distributionProfile[entitlement] (string)
* distributionProfile[priority] (string)
* distributionProfile[allowStreaming] (string)
* distributionProfile[streamingPriceCode] (string)
* distributionProfile[allowDownload] (string)
* distributionProfile[downloadPriceCode] (string)
* distributionProfile[contactTelephone] (string)
* distributionProfile[contactEmail] (string)
* distributionProfile[processFeed] (integer) - Enum Type: `KalturaYahooDistributionProcessFeedActionStatus`
* distributionProfile[feedSpecVersion] (string) - Enum Type: `KalturaYouTubeDistributionFeedSpecVersion`
* distributionProfile[notificationEmail] (string)
* distributionProfile[sftpPort] (integer)
* distributionProfile[sftpBaseDir] (string)
* distributionProfile[ownerName] (string)
* distributionProfile[defaultCategory] (string)
* distributionProfile[allowComments] (string)
* distributionProfile[allowEmbedding] (string)
* distributionProfile[allowRatings] (string)
* distributionProfile[allowResponses] (string)
* distributionProfile[commercialPolicy] (string)
* distributionProfile[ugcPolicy] (string)
* distributionProfile[target] (string)
* distributionProfile[adServerPartnerId] (string)
* distributionProfile[enableAdServer] (boolean)
* distributionProfile[allowPreRollAds] (boolean)
* distributionProfile[allowPostRollAds] (boolean)
* distributionProfile[strict] (string)
* distributionProfile[overrideManualEdits] (string)
* distributionProfile[urgentReference] (string)
* distributionProfile[allowSyndication] (string)
* distributionProfile[hideViewCount] (string)
* distributionProfile[allowAdsenseForVideo] (string)
* distributionProfile[allowInvideo] (string)
* distributionProfile[allowMidRollAds] (boolean)
* distributionProfile[instreamStandard] (string)
* distributionProfile[instreamTrueview] (string)
* distributionProfile[claimType] (string)
* distributionProfile[blockOutsideOwnership] (string)
* distributionProfile[captionAutosync] (string)
* distributionProfile[deleteReference] (boolean)
* distributionProfile[releaseClaims] (boolean)
* distributionProfile[googleClientId] (string)
* distributionProfile[googleClientSecret] (string)
* distributionProfile[googleTokenData] (string)
* distributionProfile[assumeSuccess] (boolean)
* distributionProfile[privacyStatus] (string)

### distributionProfile.updateStatus
Update Distribution Profile status by id


```js
kaltura.distributionProfile.updateStatus({
  "id": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* status (integer) **required** - Enum Type: `KalturaDistributionProfileStatus`

### distributionProvider.list
List all distribution providers


```js
kaltura.distributionProvider.list({}, context)
```


### entryDistribution.add
Add new Entry Distribution


```js
kaltura.entryDistribution.add({}, context)
```


### entryDistribution.delete
Delete Entry Distribution by id


```js
kaltura.entryDistribution.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.get
Get Entry Distribution by id


```js
kaltura.entryDistribution.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.list
List all distribution providers


```js
kaltura.entryDistribution.list({}, context)
```


### entryDistribution.retrySubmit
Retries last submit action


```js
kaltura.entryDistribution.retrySubmit({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.serveReturnedData
Serves entry distribution returned data


```js
kaltura.entryDistribution.serveReturnedData({
  "id": 0,
  "actionType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* actionType (integer) **required** - Enum Type: `KalturaDistributionAction`

### entryDistribution.serveSentData
Serves entry distribution sent data


```js
kaltura.entryDistribution.serveSentData({
  "id": 0,
  "actionType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* actionType (integer) **required** - Enum Type: `KalturaDistributionAction`

### entryDistribution.submitAdd
Submits Entry Distribution to the remote destination


```js
kaltura.entryDistribution.submitAdd({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* submitWhenReady (boolean)

### entryDistribution.submitDelete
Deletes Entry Distribution from the remote destination


```js
kaltura.entryDistribution.submitDelete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.submitFetchReport
Submits Entry Distribution report request


```js
kaltura.entryDistribution.submitFetchReport({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.submitUpdate
Submits Entry Distribution changes to the remote destination


```js
kaltura.entryDistribution.submitUpdate({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### entryDistribution.update
Update Entry Distribution by id


```js
kaltura.entryDistribution.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* entryDistribution[entryId] (string) - `insertOnly`
* entryDistribution[distributionProfileId] (integer) - `insertOnly`
* entryDistribution[thumbAssetIds] (string) - Comma separated thumbnail asset ids
* entryDistribution[flavorAssetIds] (string) - Comma separated flavor asset ids
* entryDistribution[assetIds] (string) - Comma separated asset ids
* entryDistribution[sunrise] (integer) - Entry distribution publish time as Unix timestamp (In seconds)
* entryDistribution[sunset] (integer) - Entry distribution un-publish time as Unix timestamp (In seconds)
* entryDistribution[validationErrors] (array)

### entryDistribution.validate
Validates Entry Distribution by id for submission


```js
kaltura.entryDistribution.validate({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### genericDistributionProvider.add
Add new Generic Distribution Provider


```js
kaltura.genericDistributionProvider.add({}, context)
```


### genericDistributionProvider.delete
Delete Generic Distribution Provider by id


```js
kaltura.genericDistributionProvider.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### genericDistributionProvider.get
Get Generic Distribution Provider by id


```js
kaltura.genericDistributionProvider.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### genericDistributionProvider.list
List all distribution providers


```js
kaltura.genericDistributionProvider.list({}, context)
```


### genericDistributionProvider.update
Update Generic Distribution Provider by id


```js
kaltura.genericDistributionProvider.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* genericDistributionProvider[name] (string)
* genericDistributionProvider[scheduleUpdateEnabled] (boolean)
* genericDistributionProvider[availabilityUpdateEnabled] (boolean)
* genericDistributionProvider[deleteInsteadUpdate] (boolean)
* genericDistributionProvider[intervalBeforeSunrise] (integer)
* genericDistributionProvider[intervalBeforeSunset] (integer)
* genericDistributionProvider[updateRequiredEntryFields] (string)
* genericDistributionProvider[updateRequiredMetadataXPaths] (string)
* genericDistributionProvider[isDefault] (boolean)
* genericDistributionProvider[optionalFlavorParamsIds] (string)
* genericDistributionProvider[requiredFlavorParamsIds] (string)
* genericDistributionProvider[optionalThumbDimensions] (array)
* genericDistributionProvider[requiredThumbDimensions] (array)
* genericDistributionProvider[editableFields] (string)
* genericDistributionProvider[mandatoryFields] (string)

### genericDistributionProviderAction.add
Add new Generic Distribution Provider Action


```js
kaltura.genericDistributionProviderAction.add({}, context)
```


### genericDistributionProviderAction.addMrssTransform
Add MRSS transform file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addMrssTransform({
  "id": 0,
  "xslData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* xslData (string) **required** - XSL MRSS transformation data

### genericDistributionProviderAction.addMrssTransformFromFile
Add MRSS transform file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addMrssTransformFromFile({
  "id": 0,
  "xslFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* xslFile (string) **required** - XSL MRSS transformation file

### genericDistributionProviderAction.addMrssValidate
Add MRSS validate file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addMrssValidate({
  "id": 0,
  "xsdData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* xsdData (string) **required** - XSD MRSS validatation data

### genericDistributionProviderAction.addMrssValidateFromFile
Add MRSS validate file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addMrssValidateFromFile({
  "id": 0,
  "xsdFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* xsdFile (string) **required** - XSD MRSS validatation file

### genericDistributionProviderAction.addResultsTransform
Add results transform file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addResultsTransform({
  "id": 0,
  "transformData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* transformData (string) **required** - transformation data xsl, xPath or regex

### genericDistributionProviderAction.addResultsTransformFromFile
Add MRSS transform file to generic distribution provider action


```js
kaltura.genericDistributionProviderAction.addResultsTransformFromFile({
  "id": 0,
  "transformFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - the id of the generic distribution provider action
* transformFile (string) **required** - transformation file xsl, xPath or regex

### genericDistributionProviderAction.delete
Delete Generic Distribution Provider Action by id


```js
kaltura.genericDistributionProviderAction.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### genericDistributionProviderAction.deleteByProviderId
Delete Generic Distribution Provider Action by provider id


```js
kaltura.genericDistributionProviderAction.deleteByProviderId({
  "genericDistributionProviderId": 0,
  "actionType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* genericDistributionProviderId (integer) **required**
* actionType (integer) **required** - Enum Type: `KalturaDistributionAction`

### genericDistributionProviderAction.get
Get Generic Distribution Provider Action by id


```js
kaltura.genericDistributionProviderAction.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### genericDistributionProviderAction.getByProviderId
Get Generic Distribution Provider Action by provider id


```js
kaltura.genericDistributionProviderAction.getByProviderId({
  "genericDistributionProviderId": 0,
  "actionType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* genericDistributionProviderId (integer) **required**
* actionType (integer) **required** - Enum Type: `KalturaDistributionAction`

### genericDistributionProviderAction.list
List all distribution providers


```js
kaltura.genericDistributionProviderAction.list({}, context)
```


### genericDistributionProviderAction.update
Update Generic Distribution Provider Action by id


```js
kaltura.genericDistributionProviderAction.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* genericDistributionProviderAction[genericDistributionProviderId] (integer) - `insertOnly`
* genericDistributionProviderAction[action] (integer) - `insertOnly`
* genericDistributionProviderAction[resultsParser] (integer) - Enum Type: `KalturaGenericDistributionProviderParser`
* genericDistributionProviderAction[protocol] (integer) - Enum Type: `KalturaDistributionProtocol`
* genericDistributionProviderAction[serverAddress] (string)
* genericDistributionProviderAction[remotePath] (string)
* genericDistributionProviderAction[remoteUsername] (string)
* genericDistributionProviderAction[remotePassword] (string)
* genericDistributionProviderAction[editableFields] (string)
* genericDistributionProviderAction[mandatoryFields] (string)

### genericDistributionProviderAction.updateByProviderId
Update Generic Distribution Provider Action by provider id


```js
kaltura.genericDistributionProviderAction.updateByProviderId({
  "genericDistributionProviderId": 0,
  "actionType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* genericDistributionProviderId (integer) **required**
* actionType (integer) **required** - Enum Type: `KalturaDistributionAction`
* genericDistributionProviderAction[genericDistributionProviderId] (integer) - `insertOnly`
* genericDistributionProviderAction[action] (integer) - `insertOnly`
* genericDistributionProviderAction[resultsParser] (integer) - Enum Type: `KalturaGenericDistributionProviderParser`
* genericDistributionProviderAction[protocol] (integer) - Enum Type: `KalturaDistributionProtocol`
* genericDistributionProviderAction[serverAddress] (string)
* genericDistributionProviderAction[remotePath] (string)
* genericDistributionProviderAction[remoteUsername] (string)
* genericDistributionProviderAction[remotePassword] (string)
* genericDistributionProviderAction[editableFields] (string)
* genericDistributionProviderAction[mandatoryFields] (string)

### conversionProfile.add
Add new Conversion Profile


```js
kaltura.conversionProfile.add({}, context)
```


### conversionProfile.delete
Delete Conversion Profile by ID


```js
kaltura.conversionProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### conversionProfile.get
Get Conversion Profile by ID


```js
kaltura.conversionProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### conversionProfile.getDefault
Get the partner's default conversion profile


```js
kaltura.conversionProfile.getDefault({}, context)
```


### conversionProfile.list
List Conversion Profiles by filter with paging support


```js
kaltura.conversionProfile.list({}, context)
```


### conversionProfile.setAsDefault
Set Conversion Profile to be the partner default


```js
kaltura.conversionProfile.setAsDefault({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### conversionProfile.update
Update Conversion Profile by ID


```js
kaltura.conversionProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* conversionProfile[status] (string) - Enum Type: `KalturaConversionProfileStatus`
* conversionProfile[type] (string) - `insertOnly`
* conversionProfile[name] (string) - The name of the Conversion Profile
* conversionProfile[systemName] (string) - System name of the Conversion Profile
* conversionProfile[tags] (string) - Comma separated tags
* conversionProfile[description] (string) - The description of the Conversion Profile
* conversionProfile[defaultEntryId] (string) - ID of the default entry to be used for template data
* conversionProfile[flavorParamsIds] (string) - List of included flavor ids (comma separated)
* conversionProfile[isDefault] (integer) - Enum Type: `KalturaNullableBoolean`
* conversionProfile[cropDimensions][left] (integer) - Crop left point
* conversionProfile[cropDimensions][top] (integer) - Crop top point
* conversionProfile[cropDimensions][width] (integer) - Crop width
* conversionProfile[cropDimensions][height] (integer) - Crop height

### conversionProfileAssetParams.list
Lists asset parmas of conversion profile by ID


```js
kaltura.conversionProfileAssetParams.list({}, context)
```


### conversionProfileAssetParams.update
Update asset parmas of conversion profile by ID


```js
kaltura.conversionProfileAssetParams.update({
  "conversionProfileId": 0,
  "assetParamsId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* conversionProfileId (integer) **required**
* assetParamsId (integer) **required**
* conversionProfileAssetParams[readyBehavior] (integer) - Enum Type: `KalturaFlavorReadyBehaviorType`
* conversionProfileAssetParams[origin] (integer) - Enum Type: `KalturaAssetParamsOrigin`
* conversionProfileAssetParams[systemName] (string) - Asset params system name
* conversionProfileAssetParams[forceNoneComplied] (integer) - Enum Type: `KalturaNullableBoolean`
* conversionProfileAssetParams[deletePolicy] (integer) - Enum Type: `KalturaAssetParamsDeletePolicy`
* conversionProfileAssetParams[isEncrypted] (integer) - Enum Type: `KalturaNullableBoolean`
* conversionProfileAssetParams[contentAwareness] (number)
* conversionProfileAssetParams[twoPass] (integer) - Enum Type: `KalturaNullableBoolean`
* conversionProfileAssetParams[tags] (string)

### cuePoint.add
Allows you to add an cue point object associated with an entry


```js
kaltura.cuePoint.add({}, context)
```


### cuePoint.addFromBulk
Allows you to add multiple cue points objects by uploading XML that contains multiple cue point definitions


```js
kaltura.cuePoint.addFromBulk({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**

### cuePoint.clone
Clone cuePoint with id to given entry


```js
kaltura.cuePoint.clone({
  "id": "",
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* entryId (string) **required**

### cuePoint.count
count cue point objects by filter


```js
kaltura.cuePoint.count({}, context)
```


### cuePoint.delete
delete cue point by id, and delete all children cue points


```js
kaltura.cuePoint.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### cuePoint.get
Retrieve an CuePoint object by id


```js
kaltura.cuePoint.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### cuePoint.list
List cue point objects by filter and pager


```js
kaltura.cuePoint.list({}, context)
```


### cuePoint.serveBulk
Download multiple cue points objects as XML definitions


```js
kaltura.cuePoint.serveBulk({}, context)
```


### cuePoint.update
Update cue point by id


```js
kaltura.cuePoint.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* cuePoint[entryId] (string) - `insertOnly`
* cuePoint[triggeredAt] (integer)
* cuePoint[tags] (string)
* cuePoint[startTime] (integer) - Start time in milliseconds
* cuePoint[partnerData] (string)
* cuePoint[partnerSortValue] (integer)
* cuePoint[forceStop] (integer) - Enum Type: `KalturaNullableBoolean`
* cuePoint[thumbOffset] (integer)
* cuePoint[systemName] (string)
* cuePoint[objectType] (string)
* cuePoint[parentId] (string) - `insertOnly`
* cuePoint[text] (string)
* cuePoint[endTime] (integer) - End time in milliseconds
* cuePoint[isPublic] (integer) - Enum Type: `KalturaNullableBoolean`
* cuePoint[searchableOnEntry] (integer) - Enum Type: `KalturaNullableBoolean`
* cuePoint[protocolType] (string) - `insertOnly`
* cuePoint[sourceUrl] (string)
* cuePoint[adType] (string) - Enum Type: `KalturaAdType`
* cuePoint[title] (string)
* cuePoint[duration] (integer) - Duration in milliseconds
* cuePoint[quizUserEntryId] (string) - `insertOnly`
* cuePoint[answerKey] (string)
* cuePoint[correctAnswerKeys] (array)
* cuePoint[code] (string)
* cuePoint[description] (string)
* cuePoint[eventType] (string) - Enum Type: `KalturaEventType`
* cuePoint[optionalAnswers] (array)
* cuePoint[hint] (string)
* cuePoint[question] (string)
* cuePoint[explanation] (string)
* cuePoint[assetId] (string)
* cuePoint[subType] (integer) - Enum Type: `KalturaThumbCuePointSubType`

### cuePoint.updateStatus
Update cuePoint status by id


```js
kaltura.cuePoint.updateStatus({
  "id": "",
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* status (integer) **required** - Enum Type: `KalturaCuePointStatus`

### data.add
Adds a new data entry


```js
kaltura.data.add({}, context)
```


### data.delete
Delete a data entry.


```js
kaltura.data.delete({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Data entry id to delete

### data.get
Get data entry by ID.


```js
kaltura.data.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Data entry id
* version (integer) - Desired version of the data

### data.list
List data entries by filter with paging support.


```js
kaltura.data.list({}, context)
```


### data.serve
serve action returan the file from dataContent field.


```js
kaltura.data.serve({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Data entry id
* version (integer) - Desired version of the data
* forceProxy (boolean) - force to get the content without redirect

### data.update
Update data entry. Only the properties that were set will be updated.


```js
kaltura.data.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Data entry id to update
* documentEntry[name] (string) - Entry name (Min 1 chars)
* documentEntry[description] (string) - Entry description
* documentEntry[userId] (string) - The ID of the user who is the owner of this entry
* documentEntry[creatorId] (string) - `insertOnly`
* documentEntry[tags] (string) - Entry tags
* documentEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* documentEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[type] (string) - Enum Type: `KalturaEntryType`
* documentEntry[groupId] (integer)
* documentEntry[partnerData] (string) - Can be used to store various partner related data as a string
* documentEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* documentEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* documentEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* documentEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* documentEntry[referenceId] (string) - Entry external reference id
* documentEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* documentEntry[conversionProfileId] (integer) - Override the default ingestion profile
* documentEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* documentEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* documentEntry[operationAttributes] (array)
* documentEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[templateEntryId] (string) - `insertOnly`
* documentEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* documentEntry[dataContent] (string) - The data of the entry
* documentEntry[retrieveDataContentByGet] (boolean) - `insertOnly`

### deliveryProfile.add
Add new delivery.


```js
kaltura.deliveryProfile.add({}, context)
```


### deliveryProfile.clone
Add delivery based on existing delivery.

Must provide valid sourceDeliveryId


```js
kaltura.deliveryProfile.clone({
  "deliveryId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* deliveryId (integer) **required**

### deliveryProfile.get
Get delivery by id


```js
kaltura.deliveryProfile.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### deliveryProfile.list
Retrieve a list of available delivery depends on the filter given


```js
kaltura.deliveryProfile.list({}, context)
```


### deliveryProfile.update
Update exisiting delivery


```js
kaltura.deliveryProfile.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* delivery[name] (string) - The name of the Delivery
* delivery[type] (string) - Enum Type: `KalturaDeliveryProfileType`
* delivery[systemName] (string) - System name of the delivery
* delivery[description] (string) - The description of the Delivery
* delivery[streamerType] (string) - Enum Type: `KalturaPlaybackProtocol`
* delivery[url] (string)
* delivery[status] (integer) - Enum Type: `KalturaDeliveryStatus`
* delivery[recognizer][hosts] (string) - The hosts that are recognized
* delivery[recognizer][uriPrefix] (string) - The URI prefix we use for security
* delivery[recognizer][objectType] (string)
* delivery[recognizer][headerData] (string) - headerData
* delivery[recognizer][headerSign] (string) - headerSign
* delivery[recognizer][timeout] (integer) - timeout
* delivery[recognizer][salt] (string) - salt

### documents.addFromEntry
Copy entry into new entry


```js
kaltura.documents.addFromEntry({
  "sourceEntryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* sourceEntryId (string) **required** - Document entry id to copy from
* documentEntry[name] (string) - Entry name (Min 1 chars)
* documentEntry[description] (string) - Entry description
* documentEntry[userId] (string) - The ID of the user who is the owner of this entry
* documentEntry[creatorId] (string) - `insertOnly`
* documentEntry[tags] (string) - Entry tags
* documentEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* documentEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[type] (string) - Enum Type: `KalturaEntryType`
* documentEntry[groupId] (integer)
* documentEntry[partnerData] (string) - Can be used to store various partner related data as a string
* documentEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* documentEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* documentEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* documentEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* documentEntry[referenceId] (string) - Entry external reference id
* documentEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* documentEntry[conversionProfileId] (integer) - Override the default ingestion profile
* documentEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* documentEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* documentEntry[operationAttributes] (array)
* documentEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[templateEntryId] (string) - `insertOnly`
* documentEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* documentEntry[documentType] (integer) - `insertOnly`
* sourceFlavorParamsId (integer) - The flavor to be used as the new entry source, source flavor will be used if not specified

### documents.addFromFlavorAsset
Copy flavor asset into new entry


```js
kaltura.documents.addFromFlavorAsset({
  "sourceFlavorAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* sourceFlavorAssetId (string) **required** - Flavor asset id to be used as the new entry source
* documentEntry[name] (string) - Entry name (Min 1 chars)
* documentEntry[description] (string) - Entry description
* documentEntry[userId] (string) - The ID of the user who is the owner of this entry
* documentEntry[creatorId] (string) - `insertOnly`
* documentEntry[tags] (string) - Entry tags
* documentEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* documentEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[type] (string) - Enum Type: `KalturaEntryType`
* documentEntry[groupId] (integer)
* documentEntry[partnerData] (string) - Can be used to store various partner related data as a string
* documentEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* documentEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* documentEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* documentEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* documentEntry[referenceId] (string) - Entry external reference id
* documentEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* documentEntry[conversionProfileId] (integer) - Override the default ingestion profile
* documentEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* documentEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* documentEntry[operationAttributes] (array)
* documentEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[templateEntryId] (string) - `insertOnly`
* documentEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* documentEntry[documentType] (integer) - `insertOnly`

### documents.addFromUploadedFile
Add new document entry after the specific document file was uploaded and the upload token id exists


```js
kaltura.documents.addFromUploadedFile({
  "uploadTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* documentEntry[name] (string) - Entry name (Min 1 chars)
* documentEntry[description] (string) - Entry description
* documentEntry[userId] (string) - The ID of the user who is the owner of this entry
* documentEntry[creatorId] (string) - `insertOnly`
* documentEntry[tags] (string) - Entry tags
* documentEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* documentEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[type] (string) - Enum Type: `KalturaEntryType`
* documentEntry[groupId] (integer)
* documentEntry[partnerData] (string) - Can be used to store various partner related data as a string
* documentEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* documentEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* documentEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* documentEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* documentEntry[referenceId] (string) - Entry external reference id
* documentEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* documentEntry[conversionProfileId] (integer) - Override the default ingestion profile
* documentEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* documentEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* documentEntry[operationAttributes] (array)
* documentEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[templateEntryId] (string) - `insertOnly`
* documentEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* documentEntry[documentType] (integer) - `insertOnly`
* uploadTokenId (string) **required** - Upload token id

### documents.approveReplace
Approves document replacement


```js
kaltura.documents.approveReplace({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - document entry id to replace

### documents.cancelReplace
Cancels document replacement


```js
kaltura.documents.cancelReplace({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id to cancel

### documents.convert
Convert entry


```js
kaltura.documents.convert({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id
* conversionProfileId (integer)

### documents.convertPptToSwf
This will queue a batch job for converting the document file to swf

Returns the URL where the new swf will be available


```js
kaltura.documents.convertPptToSwf({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### documents.delete
Delete a document entry.


```js
kaltura.documents.delete({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id to delete

### documents.get
Get document entry by ID.


```js
kaltura.documents.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id
* version (integer) - Desired version of the data

### documents.list
List document entries by filter with paging support.


```js
kaltura.documents.list({}, context)
```


### documents.serve
Serves the file content


```js
kaltura.documents.serve({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id
* flavorAssetId (string) - Flavor asset id
* forceProxy (boolean) - force to get the content without redirect

### documents.serveByFlavorParamsId
Serves the file content


```js
kaltura.documents.serveByFlavorParamsId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id
* flavorParamsId (string) - Flavor params id
* forceProxy (boolean) - force to get the content without redirect

### documents.update
Update document entry. Only the properties that were set will be updated.


```js
kaltura.documents.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Document entry id to update
* documentEntry[name] (string) - Entry name (Min 1 chars)
* documentEntry[description] (string) - Entry description
* documentEntry[userId] (string) - The ID of the user who is the owner of this entry
* documentEntry[creatorId] (string) - `insertOnly`
* documentEntry[tags] (string) - Entry tags
* documentEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* documentEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* documentEntry[type] (string) - Enum Type: `KalturaEntryType`
* documentEntry[groupId] (integer)
* documentEntry[partnerData] (string) - Can be used to store various partner related data as a string
* documentEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* documentEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* documentEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* documentEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* documentEntry[referenceId] (string) - Entry external reference id
* documentEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* documentEntry[conversionProfileId] (integer) - Override the default ingestion profile
* documentEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* documentEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* documentEntry[operationAttributes] (array)
* documentEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* documentEntry[templateEntryId] (string) - `insertOnly`
* documentEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* documentEntry[documentType] (integer) - `insertOnly`

### documents.updateContent
Replace content associated with the given document entry.


```js
kaltura.documents.updateContent({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - document entry id to update
* resource[objectType] (string)
* resource[resource][objectType] (string)
* resource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][assetId] (string) - ID of the source asset
* resource[resource][entryId] (string) - ID of the source entry
* resource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][objectId] (string) - The object id of the file sync object
* resource[resource][version] (string) - The version of the file sync object
* resource[resource][resource][objectType] (string)
* resource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][objectType] (string)
* resource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][resources] (array)
* resource[resource][resource][resource][content] (string) - Textual content
* resource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resource][resources] (array)
* resource[resource][resource][content] (string) - Textual content
* resource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resources] (array)
* resource[resource][content] (string) - Textual content
* resource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][privateKey] (string) - SSH private key
* resource[resource][publicKey] (string) - SSH public key
* resource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][localFilePath] (string) - Full path to the local file
* resource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][fileData] (string) - Represents the $_FILE
* resource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resources] (array)
* resource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[forceAsyncDownload] (boolean) - Force Import Job
* resource[assetId] (string) - ID of the source asset
* resource[entryId] (string) - ID of the source entry
* resource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[fileSyncObjectType] (integer) - The object type of the file sync object
* resource[objectSubType] (integer) - The object sub-type of the file sync object
* resource[objectId] (string) - The object id of the file sync object
* resource[version] (string) - The version of the file sync object
* resource[content] (string) - Textual content
* resource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[privateKey] (string) - SSH private key
* resource[publicKey] (string) - SSH public key
* resource[keyPassphrase] (string) - Passphrase for SSH keys
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* conversionProfileId (integer) - The conversion profile id to be used on the entry

### documents.upload
Upload a document file to Kaltura, then the file can be used to create a document entry.


```js
kaltura.documents.upload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required** - The file data

### doubleClick.getFeed



```js
kaltura.doubleClick.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**
* page (integer)
* period (integer)
* state (string)
* ignoreScheduling (boolean)

### doubleClick.getFeedByEntryId



```js
kaltura.doubleClick.getFeedByEntryId({
  "distributionProfileId": 0,
  "hash": "",
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**
* entryId (string) **required**

### drmLicenseAccess.getAccess
getAccessAction
     input: flavor ids, drmProvider
     Get Access Action


```js
kaltura.drmLicenseAccess.getAccess({
  "entryId": "",
  "flavorIds": "",
  "referrer": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* flavorIds (string) **required**
* referrer (string) **required**

### drmPolicy.add
Allows you to add a new DrmPolicy object


```js
kaltura.drmPolicy.add({}, context)
```


### drmPolicy.delete
Mark the KalturaDrmPolicy object as deleted


```js
kaltura.drmPolicy.delete({
  "drmPolicyId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmPolicyId (integer) **required**

### drmPolicy.get
Retrieve a KalturaDrmPolicy object by ID


```js
kaltura.drmPolicy.get({
  "drmPolicyId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmPolicyId (integer) **required**

### drmPolicy.list
List KalturaDrmPolicy objects


```js
kaltura.drmPolicy.list({}, context)
```


### drmPolicy.update
Update an existing KalturaDrmPolicy object


```js
kaltura.drmPolicy.update({
  "drmPolicyId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmPolicyId (integer) **required**
* drmPolicy[partnerId] (integer) - `insertOnly`
* drmPolicy[name] (string)
* drmPolicy[systemName] (string)
* drmPolicy[description] (string)
* drmPolicy[provider] (string) - Enum Type: `KalturaDrmProviderType`
* drmPolicy[status] (integer) - Enum Type: `KalturaDrmPolicyStatus`
* drmPolicy[scenario] (string) - Enum Type: `KalturaDrmLicenseScenario`
* drmPolicy[licenseType] (string) - Enum Type: `KalturaDrmLicenseType`
* drmPolicy[licenseExpirationPolicy] (integer) - Enum Type: `KalturaDrmLicenseExpirationPolicy`
* drmPolicy[duration] (integer) - Duration in days the license is effective
* drmPolicy[licenseParams] (array)
* drmPolicy[objectType] (string)
* drmPolicy[gracePeriod] (integer)
* drmPolicy[licenseRemovalPolicy] (integer) - Enum Type: `KalturaPlayReadyLicenseRemovalPolicy`
* drmPolicy[licenseRemovalDuration] (integer)
* drmPolicy[minSecurityLevel] (integer) - Enum Type: `KalturaPlayReadyMinimumLicenseSecurityLevel`
* drmPolicy[rights] (array)

### drmProfile.add
Allows you to add a new DrmProfile object


```js
kaltura.drmProfile.add({}, context)
```


### drmProfile.delete
Mark the KalturaDrmProfile object as deleted


```js
kaltura.drmProfile.delete({
  "drmProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmProfileId (integer) **required**

### drmProfile.get
Retrieve a KalturaDrmProfile object by ID


```js
kaltura.drmProfile.get({
  "drmProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmProfileId (integer) **required**

### drmProfile.getByProvider
Retrieve a KalturaDrmProfile object by provider, if no specific profile defined return default profile


```js
kaltura.drmProfile.getByProvider({
  "provider": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* provider (string) **required** - Enum Type: `KalturaDrmProviderType`

### drmProfile.list
List KalturaDrmProfile objects


```js
kaltura.drmProfile.list({}, context)
```


### drmProfile.update
Update an existing KalturaDrmProfile object


```js
kaltura.drmProfile.update({
  "drmProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* drmProfileId (integer) **required**
* drmProfile[partnerId] (integer) - `insertOnly`
* drmProfile[name] (string)
* drmProfile[description] (string)
* drmProfile[provider] (string) - Enum Type: `KalturaDrmProviderType`
* drmProfile[status] (integer) - Enum Type: `KalturaDrmProfileStatus`
* drmProfile[licenseServerUrl] (string)
* drmProfile[defaultPolicy] (string)
* drmProfile[signingKey] (string)
* drmProfile[objectType] (string)
* drmProfile[publicCertificate] (string)
* drmProfile[keySeed] (string)
* drmProfile[key] (string)
* drmProfile[iv] (string)
* drmProfile[owner] (string)
* drmProfile[portal] (string)
* drmProfile[maxGop] (integer)
* drmProfile[regServerHost] (string)

### dropFolder.add
Allows you to add a new KalturaDropFolder object


```js
kaltura.dropFolder.add({}, context)
```


### dropFolder.delete
Mark the KalturaDropFolder object as deleted


```js
kaltura.dropFolder.delete({
  "dropFolderId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderId (integer) **required**

### dropFolder.freeExclusiveDropFolder
freeExclusive KalturaDropFolder object


```js
kaltura.dropFolder.freeExclusiveDropFolder({
  "dropFolderId": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderId (integer) **required**
* status (integer) **required**
* errorCode (string)
* errorDescription (string)

### dropFolder.get
Retrieve a KalturaDropFolder object by ID


```js
kaltura.dropFolder.get({
  "dropFolderId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderId (integer) **required**

### dropFolder.getExclusiveDropFolder
getExclusive KalturaDropFolder object


```js
kaltura.dropFolder.getExclusiveDropFolder({
  "tag": "",
  "maxTime": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* tag (string) **required**
* maxTime (integer) **required**

### dropFolder.list
List KalturaDropFolder objects


```js
kaltura.dropFolder.list({}, context)
```


### dropFolder.update
Update an existing KalturaDropFolder object


```js
kaltura.dropFolder.update({
  "dropFolderId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderId (integer) **required**
* dropFolder[partnerId] (integer) - `insertOnly`
* dropFolder[name] (string)
* dropFolder[description] (string)
* dropFolder[type] (string) - Enum Type: `KalturaDropFolderType`
* dropFolder[status] (integer) - Enum Type: `KalturaDropFolderStatus`
* dropFolder[conversionProfileId] (integer)
* dropFolder[dc] (integer)
* dropFolder[path] (string)
* dropFolder[fileSizeCheckInterval] (integer) - The ammount of time, in seconds, that should pass so that a file with no change in size we'll be treated as "finished uploading to folder"
* dropFolder[fileDeletePolicy] (integer) - Enum Type: `KalturaDropFolderFileDeletePolicy`
* dropFolder[autoFileDeleteDays] (integer)
* dropFolder[fileHandlerType] (string) - Enum Type: `KalturaDropFolderFileHandlerType`
* dropFolder[fileNamePatterns] (string)
* dropFolder[fileHandlerConfig][objectType] (string)
* dropFolder[fileHandlerConfig][contentMatchPolicy] (integer) - Enum Type: `KalturaDropFolderContentFileHandlerMatchPolicy`
* dropFolder[fileHandlerConfig][slugRegex] (string) - Regular expression that defines valid file names to be handled.
* dropFolder[fileHandlerConfig][eventsType] (integer) - Enum Type: `KalturaScheduleEventType`

### dropFolderFile.add
Allows you to add a new KalturaDropFolderFile object


```js
kaltura.dropFolderFile.add({}, context)
```


### dropFolderFile.delete
Mark the KalturaDropFolderFile object as deleted


```js
kaltura.dropFolderFile.delete({
  "dropFolderFileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderFileId (integer) **required**

### dropFolderFile.get
Retrieve a KalturaDropFolderFile object by ID


```js
kaltura.dropFolderFile.get({
  "dropFolderFileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderFileId (integer) **required**

### dropFolderFile.ignore
Set the KalturaDropFolderFile status to ignore (KalturaDropFolderFileStatus::IGNORE)


```js
kaltura.dropFolderFile.ignore({
  "dropFolderFileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderFileId (integer) **required**

### dropFolderFile.list
List KalturaDropFolderFile objects


```js
kaltura.dropFolderFile.list({}, context)
```


### dropFolderFile.update
Update an existing KalturaDropFolderFile object


```js
kaltura.dropFolderFile.update({
  "dropFolderFileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderFileId (integer) **required**
* dropFolderFile[dropFolderId] (integer) - `insertOnly`
* dropFolderFile[fileName] (string) - `insertOnly`
* dropFolderFile[fileSize] (number)
* dropFolderFile[parsedSlug] (string)
* dropFolderFile[parsedFlavor] (string)
* dropFolderFile[parsedUserId] (string)
* dropFolderFile[leadDropFolderFileId] (integer)
* dropFolderFile[deletedDropFolderFileId] (integer)
* dropFolderFile[entryId] (string)
* dropFolderFile[errorCode] (string) - Enum Type: `KalturaDropFolderFileErrorCode`
* dropFolderFile[errorDescription] (string)
* dropFolderFile[lastModificationTime] (string)
* dropFolderFile[uploadStartDetectedAt] (integer)
* dropFolderFile[uploadEndDetectedAt] (integer)
* dropFolderFile[importStartedAt] (integer)
* dropFolderFile[importEndedAt] (integer)
* dropFolderFile[objectType] (string)
* dropFolderFile[hash] (string) - MD5 or Sha1 encrypted string
* dropFolderFile[feedXmlPath] (string) - Path of the original Feed content XML
* dropFolderFile[recordingId] (integer)
* dropFolderFile[webexHostId] (string)
* dropFolderFile[description] (string)
* dropFolderFile[confId] (string)
* dropFolderFile[contentUrl] (string)

### dropFolderFile.updateStatus
Update status of KalturaDropFolderFile


```js
kaltura.dropFolderFile.updateStatus({
  "dropFolderFileId": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* dropFolderFileId (integer) **required**
* status (integer) **required** - Enum Type: `KalturaDropFolderFileStatus`

### EmailIngestionProfile.add
EmailIngestionProfile Add action allows you to add a EmailIngestionProfile to Kaltura DB


```js
kaltura.EmailIngestionProfile.add({}, context)
```


### EmailIngestionProfile.addMediaEntry
add KalturaMediaEntry from email ingestion


```js
kaltura.EmailIngestionProfile.addMediaEntry({
  "uploadTokenId": "",
  "emailProfId": 0,
  "fromAddress": "",
  "emailMsgId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* uploadTokenId (string) **required** - Upload token id
* emailProfId (integer) **required**
* fromAddress (string) **required**
* emailMsgId (string) **required**

### EmailIngestionProfile.delete
Delete an existing EmailIngestionProfile


```js
kaltura.EmailIngestionProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### EmailIngestionProfile.get
Retrieve a EmailIngestionProfile by id


```js
kaltura.EmailIngestionProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### EmailIngestionProfile.getByEmailAddress
Retrieve a EmailIngestionProfile by email address


```js
kaltura.EmailIngestionProfile.getByEmailAddress({
  "emailAddress": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* emailAddress (string) **required**

### EmailIngestionProfile.update
Update an existing EmailIngestionProfile


```js
kaltura.EmailIngestionProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* EmailIP[name] (string)
* EmailIP[description] (string)
* EmailIP[emailAddress] (string)
* EmailIP[mailboxId] (string)
* EmailIP[conversionProfile2Id] (integer)
* EmailIP[moderationStatus] (integer) - Enum Type: `KalturaEntryModerationStatus`
* EmailIP[defaultCategory] (string)
* EmailIP[defaultUserId] (string)
* EmailIP[defaultTags] (string)
* EmailIP[defaultAdminTags] (string)
* EmailIP[maxAttachmentSizeKbytes] (integer)
* EmailIP[maxAttachmentsPerMail] (integer)

### entryServerNode.get



```js
kaltura.entryServerNode.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### entryServerNode.list



```js
kaltura.entryServerNode.list({}, context)
```


### entryServerNode.update



```js
kaltura.entryServerNode.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* entryServerNode[objectType] (string)
* entryServerNode[streams] (array)

### entryServerNode.validateRegisteredEntryServerNode
Validates server node still registered on entry


```js
kaltura.entryServerNode.validateRegisteredEntryServerNode({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - entry server node id

### eventNotificationTemplate.add
This action allows for the creation of new backend event types in the system. This action requires access to the Kaltura server Admin Console. If you're looking to register to existing event types, please use the clone action instead.


```js
kaltura.eventNotificationTemplate.add({}, context)
```


### eventNotificationTemplate.clone
This action allows registering to various backend event. Use this action to create notifications that will react to events such as new video was uploaded or metadata field was updated. To see the list of available event types, call the listTemplates action.


```js
kaltura.eventNotificationTemplate.clone({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - source template to clone
* eventNotificationTemplate[name] (string)
* eventNotificationTemplate[systemName] (string)
* eventNotificationTemplate[description] (string)
* eventNotificationTemplate[type] (string) - `insertOnly`
* eventNotificationTemplate[manualDispatchEnabled] (boolean) - Define that the template could be dispatched manually from the API
* eventNotificationTemplate[automaticDispatchEnabled] (boolean) - Define that the template could be dispatched automatically by the system
* eventNotificationTemplate[eventType] (string) - Enum Type: `KalturaEventNotificationEventType`
* eventNotificationTemplate[eventObjectType] (string) - Enum Type: `KalturaEventNotificationEventObjectType`
* eventNotificationTemplate[eventConditions] (array)
* eventNotificationTemplate[contentParameters] (array)
* eventNotificationTemplate[userParameters] (array)
* eventNotificationTemplate[objectType] (string)
* eventNotificationTemplate[serverId] (integer) - Define the integrated BPM server id
* eventNotificationTemplate[processId] (string) - Define the integrated BPM process id
* eventNotificationTemplate[mainObjectCode] (string) - Code to load the main triggering object
* eventNotificationTemplate[format] (string) - Enum Type: `KalturaEmailNotificationFormat`
* eventNotificationTemplate[subject] (string) - Define the email subject
* eventNotificationTemplate[body] (string) - Define the email body content
* eventNotificationTemplate[fromEmail] (string) - Define the email sender email
* eventNotificationTemplate[fromName] (string) - Define the email sender name
* eventNotificationTemplate[to][objectType] (string)
* eventNotificationTemplate[to][categoryId][description] (string)
* eventNotificationTemplate[to][categoryId][value] (string)
* eventNotificationTemplate[to][categoryId][objectType] (string)
* eventNotificationTemplate[to][categoryId][geoCoderType] (string) - Enum Type: `KalturaGeoCoderType`
* eventNotificationTemplate[to][categoryId][code] (string) - PHP code
* eventNotificationTemplate[to][categoryId][xPath] (string) - May contain the full xpath to the field in three formats
* eventNotificationTemplate[to][categoryId][profileId] (integer) - Metadata profile id
* eventNotificationTemplate[to][categoryId][profileSystemName] (string) - Metadata profile system name
* eventNotificationTemplate[to][emailRecipients] (array)
* eventNotificationTemplate[to][filter][orderBy] (string)
* eventNotificationTemplate[to][filter][advancedSearch][objectType] (string)
* eventNotificationTemplate[to][filter][advancedSearch][value] (string)
* eventNotificationTemplate[to][filter][advancedSearch][categoriesMatchOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][categoryEntryStatusIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* eventNotificationTemplate[to][filter][advancedSearch][categoryIdEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][memberIdEq] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberIdIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberPermissionsMatchOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberPermissionsMatchAnd] (string)
* eventNotificationTemplate[to][filter][advancedSearch][noDistributionProfiles] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][distributionProfileId] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* eventNotificationTemplate[to][filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* eventNotificationTemplate[to][filter][advancedSearch][contentLike] (string)
* eventNotificationTemplate[to][filter][advancedSearch][contentMultiLikeOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][contentMultiLikeAnd] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointsFreeText] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointTypeIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointSubTypeEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][watermarkId] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][indexIdGreaterThan] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][depthGreaterThanEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][advancedSearch][field] (string)
* eventNotificationTemplate[to][filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* eventNotificationTemplate[to][filter][advancedSearch][items] (array)
* eventNotificationTemplate[to][filter][advancedSearch][idEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][idIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][userIdEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][userIdIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* eventNotificationTemplate[to][filter][advancedSearch][extendedStatusIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* eventNotificationTemplate[to][filter][advancedSearch][not] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* eventNotificationTemplate[to][filter][advancedSearch][metadataProfileId] (integer)
* eventNotificationTemplate[to][filter][partnerIdEqual] (integer)
* eventNotificationTemplate[to][filter][typeEqual] (integer) - Enum Type: `KalturaUserType`
* eventNotificationTemplate[to][filter][typeIn] (string)
* eventNotificationTemplate[to][filter][screenNameLike] (string)
* eventNotificationTemplate[to][filter][screenNameStartsWith] (string)
* eventNotificationTemplate[to][filter][emailLike] (string)
* eventNotificationTemplate[to][filter][emailStartsWith] (string)
* eventNotificationTemplate[to][filter][tagsMultiLikeOr] (string)
* eventNotificationTemplate[to][filter][tagsMultiLikeAnd] (string)
* eventNotificationTemplate[to][filter][statusEqual] (integer) - Enum Type: `KalturaUserStatus`
* eventNotificationTemplate[to][filter][statusIn] (string)
* eventNotificationTemplate[to][filter][createdAtGreaterThanOrEqual] (integer)
* eventNotificationTemplate[to][filter][createdAtLessThanOrEqual] (integer)
* eventNotificationTemplate[to][filter][firstNameStartsWith] (string)
* eventNotificationTemplate[to][filter][lastNameStartsWith] (string)
* eventNotificationTemplate[to][filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][idOrScreenNameStartsWith] (string)
* eventNotificationTemplate[to][filter][idEqual] (string)
* eventNotificationTemplate[to][filter][idIn] (string)
* eventNotificationTemplate[to][filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][roleIdEqual] (string)
* eventNotificationTemplate[to][filter][roleIdsEqual] (string)
* eventNotificationTemplate[to][filter][roleIdsIn] (string)
* eventNotificationTemplate[to][filter][firstNameOrLastNameStartsWith] (string)
* eventNotificationTemplate[to][filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* eventNotificationTemplate[to][filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* eventNotificationTemplate[to][filter][objectType] (string)
* eventNotificationTemplate[url] (string) - Remote server URL
* eventNotificationTemplate[method] (integer) - Enum Type: `KalturaHttpNotificationMethod`
* eventNotificationTemplate[data][objectType] (string)
* eventNotificationTemplate[data][content][description] (string)
* eventNotificationTemplate[data][content][value] (string)
* eventNotificationTemplate[data][content][objectType] (string)
* eventNotificationTemplate[data][content][geoCoderType] (string) - Enum Type: `KalturaGeoCoderType`
* eventNotificationTemplate[data][content][code] (string) - PHP code
* eventNotificationTemplate[data][content][xPath] (string) - May contain the full xpath to the field in three formats
* eventNotificationTemplate[data][content][profileId] (integer) - Metadata profile id
* eventNotificationTemplate[data][content][profileSystemName] (string) - Metadata profile system name
* eventNotificationTemplate[data][apiObjectType] (string) - Kaltura API object type
* eventNotificationTemplate[data][format] (integer) - Enum Type: `KalturaResponseType`
* eventNotificationTemplate[data][ignoreNull] (boolean) - Ignore null attributes during serialization
* eventNotificationTemplate[data][code] (string) - PHP code
* eventNotificationTemplate[queueNameParameters] (array)
* eventNotificationTemplate[queueKeyParameters] (array)
* eventNotificationTemplate[apiObjectType] (string) - Kaltura API object type
* eventNotificationTemplate[objectFormat] (integer) - Enum Type: `KalturaResponseType`
* eventNotificationTemplate[responseProfileId] (integer) - Kaltura response-profile id
* eventNotificationTemplate[message] (string) - Define the message to be sent
* eventNotificationTemplate[eventId] (string) - Define the event that waiting to the signal
* eventNotificationTemplate[abortOnDeletion] (boolean) - Abort the process automatically if the triggering object deleted

### eventNotificationTemplate.delete
Delete an event notification template object


```js
kaltura.eventNotificationTemplate.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### eventNotificationTemplate.dispatch
Dispatch event notification object by id


```js
kaltura.eventNotificationTemplate.dispatch({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* scope[objectId] (string)
* scope[scopeObjectType] (string) - Enum Type: `KalturaEventNotificationEventObjectType`

### eventNotificationTemplate.get
Retrieve an event notification template object by id


```js
kaltura.eventNotificationTemplate.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### eventNotificationTemplate.list
list event notification template objects


```js
kaltura.eventNotificationTemplate.list({}, context)
```


### eventNotificationTemplate.listByPartner



```js
kaltura.eventNotificationTemplate.listByPartner({}, context)
```


### eventNotificationTemplate.listTemplates
Action lists the template partner event notification templates.


```js
kaltura.eventNotificationTemplate.listTemplates({}, context)
```


### eventNotificationTemplate.register
Register to a queue from which event messages will be provided according to given template. Queue will be created if not already exists


```js
kaltura.eventNotificationTemplate.register({
  "notificationTemplateSystemName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* notificationTemplateSystemName (string) **required** - Existing push notification template system name
* pushNotificationParams[userParams] (array)

### eventNotificationTemplate.sendCommand
Clear queue messages


```js
kaltura.eventNotificationTemplate.sendCommand({
  "notificationTemplateSystemName": "",
  "command": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* notificationTemplateSystemName (string) **required** - Existing push notification template system name
* pushNotificationParams[userParams] (array)
* command (string) **required** - Enum Type: `KalturaPushNotificationCommandType`

### eventNotificationTemplate.update
Update an existing event notification template object


```js
kaltura.eventNotificationTemplate.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* eventNotificationTemplate[name] (string)
* eventNotificationTemplate[systemName] (string)
* eventNotificationTemplate[description] (string)
* eventNotificationTemplate[type] (string) - `insertOnly`
* eventNotificationTemplate[manualDispatchEnabled] (boolean) - Define that the template could be dispatched manually from the API
* eventNotificationTemplate[automaticDispatchEnabled] (boolean) - Define that the template could be dispatched automatically by the system
* eventNotificationTemplate[eventType] (string) - Enum Type: `KalturaEventNotificationEventType`
* eventNotificationTemplate[eventObjectType] (string) - Enum Type: `KalturaEventNotificationEventObjectType`
* eventNotificationTemplate[eventConditions] (array)
* eventNotificationTemplate[contentParameters] (array)
* eventNotificationTemplate[userParameters] (array)
* eventNotificationTemplate[objectType] (string)
* eventNotificationTemplate[serverId] (integer) - Define the integrated BPM server id
* eventNotificationTemplate[processId] (string) - Define the integrated BPM process id
* eventNotificationTemplate[mainObjectCode] (string) - Code to load the main triggering object
* eventNotificationTemplate[format] (string) - Enum Type: `KalturaEmailNotificationFormat`
* eventNotificationTemplate[subject] (string) - Define the email subject
* eventNotificationTemplate[body] (string) - Define the email body content
* eventNotificationTemplate[fromEmail] (string) - Define the email sender email
* eventNotificationTemplate[fromName] (string) - Define the email sender name
* eventNotificationTemplate[to][objectType] (string)
* eventNotificationTemplate[to][categoryId][description] (string)
* eventNotificationTemplate[to][categoryId][value] (string)
* eventNotificationTemplate[to][categoryId][objectType] (string)
* eventNotificationTemplate[to][categoryId][geoCoderType] (string) - Enum Type: `KalturaGeoCoderType`
* eventNotificationTemplate[to][categoryId][code] (string) - PHP code
* eventNotificationTemplate[to][categoryId][xPath] (string) - May contain the full xpath to the field in three formats
* eventNotificationTemplate[to][categoryId][profileId] (integer) - Metadata profile id
* eventNotificationTemplate[to][categoryId][profileSystemName] (string) - Metadata profile system name
* eventNotificationTemplate[to][emailRecipients] (array)
* eventNotificationTemplate[to][filter][orderBy] (string)
* eventNotificationTemplate[to][filter][advancedSearch][objectType] (string)
* eventNotificationTemplate[to][filter][advancedSearch][value] (string)
* eventNotificationTemplate[to][filter][advancedSearch][categoriesMatchOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][categoryEntryStatusIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* eventNotificationTemplate[to][filter][advancedSearch][categoryIdEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][memberIdEq] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberIdIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberPermissionsMatchOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][memberPermissionsMatchAnd] (string)
* eventNotificationTemplate[to][filter][advancedSearch][noDistributionProfiles] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][distributionProfileId] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* eventNotificationTemplate[to][filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* eventNotificationTemplate[to][filter][advancedSearch][contentLike] (string)
* eventNotificationTemplate[to][filter][advancedSearch][contentMultiLikeOr] (string)
* eventNotificationTemplate[to][filter][advancedSearch][contentMultiLikeAnd] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointsFreeText] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointTypeIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][cuePointSubTypeEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][watermarkId] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][indexIdGreaterThan] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][depthGreaterThanEqual] (integer)
* eventNotificationTemplate[to][filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][advancedSearch][field] (string)
* eventNotificationTemplate[to][filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* eventNotificationTemplate[to][filter][advancedSearch][items] (array)
* eventNotificationTemplate[to][filter][advancedSearch][idEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][idIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][userIdEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][userIdIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* eventNotificationTemplate[to][filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* eventNotificationTemplate[to][filter][advancedSearch][extendedStatusIn] (string)
* eventNotificationTemplate[to][filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* eventNotificationTemplate[to][filter][advancedSearch][not] (boolean)
* eventNotificationTemplate[to][filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* eventNotificationTemplate[to][filter][advancedSearch][metadataProfileId] (integer)
* eventNotificationTemplate[to][filter][partnerIdEqual] (integer)
* eventNotificationTemplate[to][filter][typeEqual] (integer) - Enum Type: `KalturaUserType`
* eventNotificationTemplate[to][filter][typeIn] (string)
* eventNotificationTemplate[to][filter][screenNameLike] (string)
* eventNotificationTemplate[to][filter][screenNameStartsWith] (string)
* eventNotificationTemplate[to][filter][emailLike] (string)
* eventNotificationTemplate[to][filter][emailStartsWith] (string)
* eventNotificationTemplate[to][filter][tagsMultiLikeOr] (string)
* eventNotificationTemplate[to][filter][tagsMultiLikeAnd] (string)
* eventNotificationTemplate[to][filter][statusEqual] (integer) - Enum Type: `KalturaUserStatus`
* eventNotificationTemplate[to][filter][statusIn] (string)
* eventNotificationTemplate[to][filter][createdAtGreaterThanOrEqual] (integer)
* eventNotificationTemplate[to][filter][createdAtLessThanOrEqual] (integer)
* eventNotificationTemplate[to][filter][firstNameStartsWith] (string)
* eventNotificationTemplate[to][filter][lastNameStartsWith] (string)
* eventNotificationTemplate[to][filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][idOrScreenNameStartsWith] (string)
* eventNotificationTemplate[to][filter][idEqual] (string)
* eventNotificationTemplate[to][filter][idIn] (string)
* eventNotificationTemplate[to][filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* eventNotificationTemplate[to][filter][roleIdEqual] (string)
* eventNotificationTemplate[to][filter][roleIdsEqual] (string)
* eventNotificationTemplate[to][filter][roleIdsIn] (string)
* eventNotificationTemplate[to][filter][firstNameOrLastNameStartsWith] (string)
* eventNotificationTemplate[to][filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* eventNotificationTemplate[to][filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* eventNotificationTemplate[to][filter][objectType] (string)
* eventNotificationTemplate[url] (string) - Remote server URL
* eventNotificationTemplate[method] (integer) - Enum Type: `KalturaHttpNotificationMethod`
* eventNotificationTemplate[data][objectType] (string)
* eventNotificationTemplate[data][content][description] (string)
* eventNotificationTemplate[data][content][value] (string)
* eventNotificationTemplate[data][content][objectType] (string)
* eventNotificationTemplate[data][content][geoCoderType] (string) - Enum Type: `KalturaGeoCoderType`
* eventNotificationTemplate[data][content][code] (string) - PHP code
* eventNotificationTemplate[data][content][xPath] (string) - May contain the full xpath to the field in three formats
* eventNotificationTemplate[data][content][profileId] (integer) - Metadata profile id
* eventNotificationTemplate[data][content][profileSystemName] (string) - Metadata profile system name
* eventNotificationTemplate[data][apiObjectType] (string) - Kaltura API object type
* eventNotificationTemplate[data][format] (integer) - Enum Type: `KalturaResponseType`
* eventNotificationTemplate[data][ignoreNull] (boolean) - Ignore null attributes during serialization
* eventNotificationTemplate[data][code] (string) - PHP code
* eventNotificationTemplate[queueNameParameters] (array)
* eventNotificationTemplate[queueKeyParameters] (array)
* eventNotificationTemplate[apiObjectType] (string) - Kaltura API object type
* eventNotificationTemplate[objectFormat] (integer) - Enum Type: `KalturaResponseType`
* eventNotificationTemplate[responseProfileId] (integer) - Kaltura response-profile id
* eventNotificationTemplate[message] (string) - Define the message to be sent
* eventNotificationTemplate[eventId] (string) - Define the event that waiting to the signal
* eventNotificationTemplate[abortOnDeletion] (boolean) - Abort the process automatically if the triggering object deleted

### eventNotificationTemplate.updateStatus
Update event notification template status by id


```js
kaltura.eventNotificationTemplate.updateStatus({
  "id": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* status (integer) **required** - Enum Type: `KalturaEventNotificationTemplateStatus`

### externalMedia.add
Add external media entry


```js
kaltura.externalMedia.add({}, context)
```


### externalMedia.count
Count media entries by filter.


```js
kaltura.externalMedia.count({}, context)
```


### externalMedia.delete
Delete a external media entry.


```js
kaltura.externalMedia.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - External media entry id to delete

### externalMedia.get
Get external media entry by ID.


```js
kaltura.externalMedia.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - External media entry id

### externalMedia.list
List media entries by filter with paging support.


```js
kaltura.externalMedia.list({}, context)
```


### externalMedia.update
Update external media entry. Only the properties that were set will be updated.


```js
kaltura.externalMedia.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - External media entry id to update
* entry[name] (string) - Entry name (Min 1 chars)
* entry[description] (string) - Entry description
* entry[userId] (string) - The ID of the user who is the owner of this entry
* entry[creatorId] (string) - `insertOnly`
* entry[tags] (string) - Entry tags
* entry[adminTags] (string) - Entry admin tags can be updated only by administrators
* entry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* entry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* entry[type] (string) - Enum Type: `KalturaEntryType`
* entry[groupId] (integer)
* entry[partnerData] (string) - Can be used to store various partner related data as a string
* entry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* entry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* entry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* entry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* entry[referenceId] (string) - Entry external reference id
* entry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* entry[conversionProfileId] (integer) - Override the default ingestion profile
* entry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* entry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* entry[operationAttributes] (array)
* entry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* entry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* entry[templateEntryId] (string) - `insertOnly`
* entry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* entry[msDuration] (integer) - The duration in miliseconds
* entry[mediaType] (integer) - `insertOnly`
* entry[conversionQuality] (string) - `insertOnly`
* entry[sourceType] (string) - `insertOnly`
* entry[searchProviderType] (integer) - `insertOnly`
* entry[searchProviderId] (string) - `insertOnly`
* entry[creditUserName] (string) - The user name used for credits
* entry[creditUrl] (string) - The URL for credits
* entry[streams] (array)
* entry[externalSourceType] (string) - `insertOnly`

### fileAsset.add
Add new file asset


```js
kaltura.fileAsset.add({}, context)
```


### fileAsset.delete
Delete file asset by id


```js
kaltura.fileAsset.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### fileAsset.get
Get file asset by id


```js
kaltura.fileAsset.get({
  "id": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* id (integer) **required**

### fileAsset.list
List file assets by filter and pager


```js
kaltura.fileAsset.list({}, context)
```


### fileAsset.serve
Serve file asset by id


```js
kaltura.fileAsset.serve({
  "id": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* id (integer) **required**

### fileAsset.setContent
Set content of file asset


```js
kaltura.fileAsset.setContent({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* contentResource[objectType] (string)
* contentResource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[forceAsyncDownload] (boolean) - Force Import Job
* contentResource[assetId] (string) - ID of the source asset
* contentResource[entryId] (string) - ID of the source entry
* contentResource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[objectId] (string) - The object id of the file sync object
* contentResource[version] (string) - The version of the file sync object
* contentResource[resource][objectType] (string)
* contentResource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][assetId] (string) - ID of the source asset
* contentResource[resource][entryId] (string) - ID of the source entry
* contentResource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][objectType] (string)
* contentResource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][objectType] (string)
* contentResource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][resources] (array)
* contentResource[resource][resource][resource][content] (string) - Textual content
* contentResource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resource][resources] (array)
* contentResource[resource][resource][content] (string) - Textual content
* contentResource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resources] (array)
* contentResource[resource][content] (string) - Textual content
* contentResource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][privateKey] (string) - SSH private key
* contentResource[resource][publicKey] (string) - SSH public key
* contentResource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resources] (array)
* contentResource[content] (string) - Textual content
* contentResource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[privateKey] (string) - SSH private key
* contentResource[publicKey] (string) - SSH public key
* contentResource[keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[localFilePath] (string) - Full path to the local file
* contentResource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[fileData] (string) - Represents the $_FILE
* contentResource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### fileAsset.update
Update file asset by id


```js
kaltura.fileAsset.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* fileAsset[fileAssetObjectType] (string) - `insertOnly`
* fileAsset[objectId] (string) - `insertOnly`
* fileAsset[name] (string)
* fileAsset[systemName] (string)
* fileAsset[fileExt] (string)

### fileSync.list
List file syce objects by filter and pager


```js
kaltura.fileSync.list({}, context)
```


### fileSync.update
Update file sync by id


```js
kaltura.fileSync.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* fileSync[status] (integer) - Enum Type: `KalturaFileSyncStatus`
* fileSync[fileRoot] (string)
* fileSync[filePath] (string)

### flavorAsset.add
Add flavor asset


```js
kaltura.flavorAsset.add({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* flavorAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* flavorAsset[fileExt] (string) - `insertOnly`
* flavorAsset[partnerData] (string) - Partner private data
* flavorAsset[partnerDescription] (string) - Partner friendly description
* flavorAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* flavorAsset[flavorParamsId] (integer) - `insertOnly`
* flavorAsset[language] (string) - Enum Type: `KalturaLanguage`
* flavorAsset[label] (string) - The label of the flavor asset
* flavorAsset[objectType] (string)
* flavorAsset[multicastIP] (string)
* flavorAsset[multicastPort] (integer)
* flavorAsset[widevineDistributionStartDate] (integer) - License distribution window start date
* flavorAsset[widevineDistributionEndDate] (integer) - License distribution window end date
* flavorAsset[widevineAssetId] (integer) - Widevine unique asset id

### flavorAsset.convert
Add and convert new Flavor Asset for Entry with specific Flavor Params


```js
kaltura.flavorAsset.convert({
  "entryId": "",
  "flavorParamsId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* flavorParamsId (integer) **required**
* priority (integer)

### flavorAsset.delete
Delete Flavor Asset by ID


```js
kaltura.flavorAsset.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### flavorAsset.deleteLocalContent
delete all local file syncs for this asset


```js
kaltura.flavorAsset.deleteLocalContent({
  "assetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**

### flavorAsset.export
manually export an asset


```js
kaltura.flavorAsset.export({
  "assetId": "",
  "storageProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**
* storageProfileId (integer) **required**

### flavorAsset.get
Get Flavor Asset by ID


```js
kaltura.flavorAsset.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### flavorAsset.getByEntryId
Get Flavor Assets for Entry


```js
kaltura.flavorAsset.getByEntryId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### flavorAsset.getDownloadUrl
Get download URL for the Flavor Asset


```js
kaltura.flavorAsset.getDownloadUrl({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* useCdn (boolean)

### flavorAsset.getFlavorAssetsWithParams
Get Flavor Asset with the relevant Flavor Params (Flavor Params can exist without Flavor Asset & vice versa)


```js
kaltura.flavorAsset.getFlavorAssetsWithParams({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### flavorAsset.getRemotePaths
Get remote storage existing paths for the asset


```js
kaltura.flavorAsset.getRemotePaths({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### flavorAsset.getUrl
Get download URL for the asset


```js
kaltura.flavorAsset.getUrl({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* storageId (integer)
* forceProxy (boolean)
* options[fileName] (string) - The name of the downloaded file
* options[referrer] (string)

### flavorAsset.getWebPlayableByEntryId
Get web playable Flavor Assets for Entry


```js
kaltura.flavorAsset.getWebPlayableByEntryId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### flavorAsset.list
List Flavor Assets by filter and pager


```js
kaltura.flavorAsset.list({}, context)
```


### flavorAsset.reconvert
Reconvert Flavor Asset by ID


```js
kaltura.flavorAsset.reconvert({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - Flavor Asset ID

### flavorAsset.serveAdStitchCmd
serve cmd line to transcode the ad


```js
kaltura.flavorAsset.serveAdStitchCmd({
  "assetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**
* ffprobeJson (string)
* duration (string)

### flavorAsset.setAsSource
Set a given flavor as the original flavor


```js
kaltura.flavorAsset.setAsSource({
  "assetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**

### flavorAsset.setContent
Update content of flavor asset


```js
kaltura.flavorAsset.setContent({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* contentResource[objectType] (string)
* contentResource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[forceAsyncDownload] (boolean) - Force Import Job
* contentResource[assetId] (string) - ID of the source asset
* contentResource[entryId] (string) - ID of the source entry
* contentResource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[objectId] (string) - The object id of the file sync object
* contentResource[version] (string) - The version of the file sync object
* contentResource[resource][objectType] (string)
* contentResource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][assetId] (string) - ID of the source asset
* contentResource[resource][entryId] (string) - ID of the source entry
* contentResource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][objectType] (string)
* contentResource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][objectType] (string)
* contentResource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][resources] (array)
* contentResource[resource][resource][resource][content] (string) - Textual content
* contentResource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resource][resources] (array)
* contentResource[resource][resource][content] (string) - Textual content
* contentResource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resources] (array)
* contentResource[resource][content] (string) - Textual content
* contentResource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][privateKey] (string) - SSH private key
* contentResource[resource][publicKey] (string) - SSH public key
* contentResource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resources] (array)
* contentResource[content] (string) - Textual content
* contentResource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[privateKey] (string) - SSH private key
* contentResource[publicKey] (string) - SSH public key
* contentResource[keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[localFilePath] (string) - Full path to the local file
* contentResource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[fileData] (string) - Represents the $_FILE
* contentResource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### flavorAsset.update
Update flavor asset


```js
kaltura.flavorAsset.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* flavorAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* flavorAsset[fileExt] (string) - `insertOnly`
* flavorAsset[partnerData] (string) - Partner private data
* flavorAsset[partnerDescription] (string) - Partner friendly description
* flavorAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* flavorAsset[flavorParamsId] (integer) - `insertOnly`
* flavorAsset[language] (string) - Enum Type: `KalturaLanguage`
* flavorAsset[label] (string) - The label of the flavor asset
* flavorAsset[objectType] (string)
* flavorAsset[multicastIP] (string)
* flavorAsset[multicastPort] (integer)
* flavorAsset[widevineDistributionStartDate] (integer) - License distribution window start date
* flavorAsset[widevineDistributionEndDate] (integer) - License distribution window end date
* flavorAsset[widevineAssetId] (integer) - Widevine unique asset id

### flavorParams.add
Add new Flavor Params


```js
kaltura.flavorParams.add({}, context)
```


### flavorParams.delete
Delete Flavor Params by ID


```js
kaltura.flavorParams.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### flavorParams.get
Get Flavor Params by ID


```js
kaltura.flavorParams.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### flavorParams.getByConversionProfileId
Get Flavor Params by Conversion Profile ID


```js
kaltura.flavorParams.getByConversionProfileId({
  "conversionProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* conversionProfileId (integer) **required**

### flavorParams.list
List Flavor Params by filter with paging support (By default - all system default params will be listed too)


```js
kaltura.flavorParams.list({}, context)
```


### flavorParams.update
Update Flavor Params by ID


```js
kaltura.flavorParams.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* flavorParams[partnerId] (integer)
* flavorParams[name] (string) - The name of the Flavor Params
* flavorParams[systemName] (string) - System name of the Flavor Params
* flavorParams[description] (string) - The description of the Flavor Params
* flavorParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* flavorParams[requiredPermissions] (array)
* flavorParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* flavorParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* flavorParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* flavorParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* flavorParams[videoCodec] (string) - Enum Type: `KalturaVideoCodec`
* flavorParams[videoBitrate] (integer) - The video bitrate (in KBits) of the Flavor Params
* flavorParams[audioCodec] (string) - Enum Type: `KalturaAudioCodec`
* flavorParams[audioBitrate] (integer) - The audio bitrate (in KBits) of the Flavor Params
* flavorParams[audioChannels] (integer) - The number of audio channels for "downmixing"
* flavorParams[audioSampleRate] (integer) - The audio sample rate of the Flavor Params
* flavorParams[width] (integer) - The desired width of the Flavor Params
* flavorParams[height] (integer) - The desired height of the Flavor Params
* flavorParams[frameRate] (number) - The frame rate of the Flavor Params
* flavorParams[gopSize] (integer) - The gop size of the Flavor Params
* flavorParams[conversionEngines] (string) - The list of conversion engines (comma separated)
* flavorParams[conversionEnginesExtraParams] (string) - The list of conversion engines extra params (separated with "|")
* flavorParams[twoPass] (boolean)
* flavorParams[deinterlice] (integer)
* flavorParams[rotate] (integer)
* flavorParams[operators] (string)
* flavorParams[engineVersion] (integer)
* flavorParams[format] (string) - Enum Type: `KalturaContainerFormat`
* flavorParams[aspectRatioProcessingMode] (integer)
* flavorParams[forceFrameToMultiplication16] (integer)
* flavorParams[isGopInSec] (integer)
* flavorParams[isAvoidVideoShrinkFramesizeToSource] (integer)
* flavorParams[isAvoidVideoShrinkBitrateToSource] (integer)
* flavorParams[isVideoFrameRateForLowBrAppleHls] (integer)
* flavorParams[multiStream] (string)
* flavorParams[anamorphicPixels] (number)
* flavorParams[isAvoidForcedKeyFrames] (integer)
* flavorParams[forcedKeyFramesMode] (integer)
* flavorParams[isCropIMX] (integer)
* flavorParams[optimizationPolicy] (integer)
* flavorParams[maxFrameRate] (integer)
* flavorParams[videoConstantBitrate] (integer)
* flavorParams[videoBitrateTolerance] (integer)
* flavorParams[watermarkData] (string)
* flavorParams[subtitlesData] (string)
* flavorParams[isEncrypted] (integer)
* flavorParams[contentAwareness] (number)
* flavorParams[clipOffset] (integer)
* flavorParams[clipDuration] (integer)
* flavorParams[objectType] (string)
* flavorParams[flavorParamsId] (integer)
* flavorParams[commandLinesStr] (string)
* flavorParams[flavorParamsVersion] (string)
* flavorParams[flavorAssetId] (string)
* flavorParams[flavorAssetVersion] (string)
* flavorParams[readyBehavior] (integer)
* flavorParams[densityWidth] (integer)
* flavorParams[densityHeight] (integer)
* flavorParams[sizeWidth] (integer)
* flavorParams[sizeHeight] (integer)
* flavorParams[depth] (integer)
* flavorParams[streamSuffix] (string) - Suffix to be added to the stream name after the entry id {entry_id}_{stream_suffix}, e.g. for entry id 0_kjdu5jr6 and suffix 1, the stream name will be 0_kjdu5jr6_1
* flavorParams[readonly] (boolean)
* flavorParams[flashVersion] (integer)
* flavorParams[poly2Bitmap] (boolean)
* flavorParams[widevineDistributionStartDate] (integer) - License distribution window start date
* flavorParams[widevineDistributionEndDate] (integer) - License distribution window end date

### flavorParamsOutput.get
Get flavor params output object by ID


```js
kaltura.flavorParamsOutput.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### flavorParamsOutput.list
List flavor params output objects by filter and pager


```js
kaltura.flavorParamsOutput.list({}, context)
```


### groupUser.add
Add new GroupUser


```js
kaltura.groupUser.add({}, context)
```


### groupUser.delete
delete by userId and groupId


```js
kaltura.groupUser.delete({
  "userId": "",
  "groupId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required**
* groupId (string) **required**

### groupUser.list
List all GroupUsers


```js
kaltura.groupUser.list({}, context)
```


### integration.dispatch
Dispatch integration task


```js
kaltura.integration.dispatch({
  "objectType": "",
  "objectId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* data[providerType] (string) - Enum Type: `KalturaIntegrationProviderType`
* data[providerData][objectType] (string)
* data[providerData][entryId] (string) - Entry ID
* data[providerData][flavorAssetId] (string) - Flavor ID
* data[providerData][captionAssetFormats] (string) - Caption formats
* data[providerData][priority] (string) - Enum Type: `KalturaCielo24Priority`
* data[providerData][fidelity] (string) - Enum Type: `KalturaCielo24Fidelity`
* data[providerData][spokenLanguage] (string) - Enum Type: `KalturaLanguage`
* data[providerData][replaceMediaContent] (boolean) - should replace remote media content
* data[providerData][additionalParameters] (string) - additional parameters to send to Cielo24
* data[providerData][metadataProfileId] (integer) - ID of the metadata profile for the extracted term metadata
* data[providerData][transcriptAssetId] (string) - ID of the transcript asset
* data[providerData][voicebaseApiKey] (string) - Voicebase API key to fetch transcript tokens
* data[providerData][voicebaseApiPassword] (string) - Voicebase API password to fetch transcript tokens
* data[providerData][exampleUrl] (string) - Just an example
* data[providerData][transcriptId] (string) - input Transcript-asset ID
* objectType (string) **required** - Enum Type: `KalturaBatchJobObjectType`
* objectId (string) **required**

### integration.notify



```js
kaltura.integration.notify({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - integration job id

### jobs.abortBulkUpload
batch abortBulkUploadAction aborts and returns the status of bulk upload task


```js
kaltura.jobs.abortBulkUpload({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortCaptureThumb
batch abortCaptureThumbAction aborts and returns the status of capture thumbnail task


```js
kaltura.jobs.abortCaptureThumb({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortConvert
batch abortConvertAction aborts and returns the status of convert task


```js
kaltura.jobs.abortConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortConvertCollection
batch abortConvertCollectionAction aborts and returns the status of convert profile task


```js
kaltura.jobs.abortConvertCollection({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortConvertProfile
batch abortConvertProfileAction aborts and returns the status of convert profile task


```js
kaltura.jobs.abortConvertProfile({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortExtractMedia
batch abortExtractMediaAction aborts and returns the status of extract media task


```js
kaltura.jobs.abortExtractMedia({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortImport
batch abortImportAction aborts and returns the status of import task


```js
kaltura.jobs.abortImport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortJob
batch abortJobAction aborts and returns the status of task


```js
kaltura.jobs.abortJob({
  "jobId": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the job
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`

### jobs.abortMail
batch abortMailAction aborts and returns the status of mail task


```js
kaltura.jobs.abortMail({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortNotification
batch abortNotificationAction aborts and returns the status of notification task


```js
kaltura.jobs.abortNotification({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortPostConvert
batch abortPostConvertAction aborts and returns the status of post convert task


```js
kaltura.jobs.abortPostConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortProvisionDelete
batch abortProvisionDeleteAction aborts and returns the status of ProvisionDelete task


```js
kaltura.jobs.abortProvisionDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortProvisionProvide
batch abortProvisionProvideAction aborts and returns the status of ProvisionProvide task


```js
kaltura.jobs.abortProvisionProvide({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortStorageDelete
batch abortStorageDeleteAction aborts and returns the status of export task


```js
kaltura.jobs.abortStorageDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.abortStorageExport
batch abortStorageExportAction aborts and returns the status of export task


```js
kaltura.jobs.abortStorageExport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.addBatchJob
batch addBatchJob action allows to add a generic BatchJob


```js
kaltura.jobs.addBatchJob({}, context)
```


### jobs.addConvertProfileJob
batch addConvertProfileJobAction creates a new convert profile job


```js
kaltura.jobs.addConvertProfileJob({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - the id of the entry to be reconverted

### jobs.addMailJob
Adds new mail job


```js
kaltura.jobs.addMailJob({}, context)
```


### jobs.boostEntryJobs
batch boostEntryJobsAction boosts all the jobs associated with the entry


```js
kaltura.jobs.boostEntryJobs({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - the id of the entry to be boosted

### jobs.deleteBulkUpload
batch deleteBulkUploadAction deletes and returns the status of bulk upload task


```js
kaltura.jobs.deleteBulkUpload({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteCaptureThumb
batch deleteCaptureThumbAction deletes and returns the status of capture thumbnail task


```js
kaltura.jobs.deleteCaptureThumb({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteConvert
batch deleteConvertAction deletes and returns the status of convert task


```js
kaltura.jobs.deleteConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteConvertCollection
batch deleteConvertCollectionAction deletes and returns the status of convert profile task


```js
kaltura.jobs.deleteConvertCollection({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteConvertProfile
batch deleteConvertProfileAction deletes and returns the status of convert profile task


```js
kaltura.jobs.deleteConvertProfile({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteExtractMedia
batch deleteExtractMediaAction deletes and returns the status of extract media task


```js
kaltura.jobs.deleteExtractMedia({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteImport
batch deleteImportAction deletes and returns the status of import task


```js
kaltura.jobs.deleteImport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteJob
batch deleteJobAction deletes and returns the status of task


```js
kaltura.jobs.deleteJob({
  "jobId": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the job
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`

### jobs.deleteMail
batch deleteMailAction deletes and returns the status of mail task


```js
kaltura.jobs.deleteMail({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteNotification
batch deleteNotificationAction deletes and returns the status of notification task


```js
kaltura.jobs.deleteNotification({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deletePostConvert
batch deletePostConvertAction deletes and returns the status of post convert task


```js
kaltura.jobs.deletePostConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteProvisionDelete
batch deleteProvisionDeleteAction deletes and returns the status of ProvisionDelete task


```js
kaltura.jobs.deleteProvisionDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteProvisionProvide
batch deleteProvisionProvideAction deletes and returns the status of ProvisionProvide task


```js
kaltura.jobs.deleteProvisionProvide({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteStorageDelete
batch deleteStorageDeleteAction deletes and returns the status of export task


```js
kaltura.jobs.deleteStorageDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.deleteStorageExport
batch deleteStorageExportAction deletes and returns the status of export task


```js
kaltura.jobs.deleteStorageExport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.getBulkUploadStatus
// --------------------------------- ProvisionDeleteJob functions 	--------------------------------- //

// --------------------------------- BulkUploadJob functions 	--------------------------------- //

/batch getBulkUploadStatusAction returns the status of bulk upload task


```js
kaltura.jobs.getBulkUploadStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.getCaptureThumbStatus
batch getCaptureThumbStatusAction returns the status of capture thumbnail task


```js
kaltura.jobs.getCaptureThumbStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the capture thumbnail job

### jobs.getConvertCollectionStatus
batch getConvertCollectionStatusAction returns the status of convert task


```js
kaltura.jobs.getConvertCollectionStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the convert profile job

### jobs.getConvertProfileStatus
batch getConvertProfileStatusAction returns the status of convert task


```js
kaltura.jobs.getConvertProfileStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the convert profile job

### jobs.getConvertStatus
batch getConvertStatusAction returns the status of convert task


```js
kaltura.jobs.getConvertStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the convert job

### jobs.getExtractMediaStatus
batch getExtractMediaStatusAction returns the status of extract media task


```js
kaltura.jobs.getExtractMediaStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the extract media job

### jobs.getImportStatus
batch getImportStatusAction returns the status of import task


```js
kaltura.jobs.getImportStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the import job

### jobs.getMailStatus
batch getMailStatusAction returns the status of mail task


```js
kaltura.jobs.getMailStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the mail job

### jobs.getNotificationStatus
batch getNotificationStatusAction returns the status of Notification task


```js
kaltura.jobs.getNotificationStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the Notification job

### jobs.getPostConvertStatus
batch getPostConvertStatusAction returns the status of post convert task


```js
kaltura.jobs.getPostConvertStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the post convert job

### jobs.getProvisionDeleteStatus
// --------------------------------- ProvisionProvideJob functions 	--------------------------------- //

// --------------------------------- ProvisionDeleteJob functions 	--------------------------------- //

/batch getProvisionDeleteStatusAction returns the status of ProvisionDelete task


```js
kaltura.jobs.getProvisionDeleteStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the ProvisionDelete job

### jobs.getProvisionProvideStatus
// --------------------------------- ImportJob functions 	--------------------------------- //

// --------------------------------- ProvisionProvideJob functions 	--------------------------------- //

/batch getProvisionProvideStatusAction returns the status of ProvisionProvide task


```js
kaltura.jobs.getProvisionProvideStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the ProvisionProvide job

### jobs.getStatus
batch getStatusAction returns the status of task


```js
kaltura.jobs.getStatus({
  "jobId": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the job
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### jobs.getStorageDeleteStatus
batch getStorageDeleteStatusAction returns the status of export task


```js
kaltura.jobs.getStorageDeleteStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the export job

### jobs.getStorageExportStatus
batch getStorageExportStatusAction returns the status of export task


```js
kaltura.jobs.getStorageExportStatus({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the export job

### jobs.listBatchJobs
list Batch Jobs


```js
kaltura.jobs.listBatchJobs({}, context)
```


### jobs.retryBulkUpload
batch retryBulkUploadAction retrys and returns the status of bulk upload task


```js
kaltura.jobs.retryBulkUpload({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryCaptureThumb
batch retryCaptureThumbAction retrys and returns the status of capture thumbnail task


```js
kaltura.jobs.retryCaptureThumb({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryConvert
batch retryConvertAction retrys and returns the status of convert task


```js
kaltura.jobs.retryConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryConvertCollection
batch retryConvertCollectionAction retrys and returns the status of convert profile task


```js
kaltura.jobs.retryConvertCollection({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryConvertProfile
batch retryConvertProfileAction retrys and returns the status of convert profile task


```js
kaltura.jobs.retryConvertProfile({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryExtractMedia
batch retryExtractMediaAction retrys and returns the status of extract media task


```js
kaltura.jobs.retryExtractMedia({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryImport
batch retryImportAction retrys and returns the status of import task


```js
kaltura.jobs.retryImport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryJob
batch retryJobAction aborts and returns the status of task


```js
kaltura.jobs.retryJob({
  "jobId": 0,
  "jobType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the job
* jobType (string) **required** - Enum Type: `KalturaBatchJobType`
* force (boolean) - should we force the restart.

### jobs.retryMail
batch retryMailAction retrys and returns the status of mail task


```js
kaltura.jobs.retryMail({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryNotification
batch retryNotificationAction retrys and returns the status of notification task


```js
kaltura.jobs.retryNotification({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryPostConvert
batch retryPostConvertAction retrys and returns the status of post convert task


```js
kaltura.jobs.retryPostConvert({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryProvisionDelete
batch retryProvisionDeleteAction retrys and returns the status of ProvisionDelete task


```js
kaltura.jobs.retryProvisionDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryProvisionProvide
batch retryProvisionProvideAction retrys and returns the status of ProvisionProvide task


```js
kaltura.jobs.retryProvisionProvide({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryStorageDelete
batch retryStorageDeleteAction retrys and returns the status of export task


```js
kaltura.jobs.retryStorageDelete({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### jobs.retryStorageExport
batch retryStorageExportAction retrys and returns the status of export task


```js
kaltura.jobs.retryStorageExport({
  "jobId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* jobId (integer) **required** - the id of the bulk upload job

### sharepointExtension.isVersionSupported
Is this Kaltura-Sharepoint-Server-Plugin supports minimum version of $major.$minor.$build (which is required by the extension)


```js
kaltura.sharepointExtension.isVersionSupported({
  "serverMajor": 0,
  "serverMinor": 0,
  "serverBuild": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* serverMajor (integer) **required**
* serverMinor (integer) **required**
* serverBuild (integer) **required**

### sharepointExtension.listUiconfs
list uiconfs for sharepoint extension


```js
kaltura.sharepointExtension.listUiconfs({}, context)
```


### like.checkLikeExists



```js
kaltura.like.checkLikeExists({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* userId (string)

### like.like



```js
kaltura.like.like({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### like.list



```js
kaltura.like.list({}, context)
```


### like.unlike



```js
kaltura.like.unlike({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### liveReports.exportToCsv



```js
kaltura.liveReports.exportToCsv({
  "reportType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (integer) **required** - Enum Type: `KalturaLiveReportExportType`
* params[entryIds] (string)
* params[recpientEmail] (string)
* params[timeZoneOffset] (integer) - Time zone offset in minutes (between client to UTC)
* params[applicationUrlTemplate] (string) - Optional argument that allows controlling the prefix of the exported csv url

### liveReports.getEvents



```js
kaltura.liveReports.getEvents({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaLiveReportType`
* filter[entryIds] (string)
* filter[fromTime] (integer)
* filter[toTime] (integer)
* filter[live] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[orderBy] (string) - Enum Type: `KalturaLiveReportOrderBy`
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### liveReports.getReport



```js
kaltura.liveReports.getReport({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaLiveReportType`
* filter[entryIds] (string)
* filter[fromTime] (integer)
* filter[toTime] (integer)
* filter[live] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[orderBy] (string) - Enum Type: `KalturaLiveReportOrderBy`
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### liveReports.serveReport
Will serve a requested report


```js
kaltura.liveReports.serveReport({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - - the requested id

### liveStats.collect
Will write to the event log a single line representing the event

KalturaStatsEvent $event


```js
kaltura.liveStats.collect({}, context)
```


### liveStream.add
Adds new live stream entry.

The entry will be queued for provision.


```js
kaltura.liveStream.add({}, context)
```


### liveStream.addLiveStreamPushPublishConfiguration
Add new pushPublish configuration to entry


```js
kaltura.liveStream.addLiveStreamPushPublishConfiguration({
  "entryId": "",
  "protocol": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* protocol (string) **required** - Enum Type: `KalturaPlaybackProtocol`
* url (string)
* liveStreamConfiguration[protocol] (string) - Enum Type: `KalturaPlaybackProtocol`
* liveStreamConfiguration[url] (string)
* liveStreamConfiguration[publishUrl] (string)
* liveStreamConfiguration[backupUrl] (string)
* liveStreamConfiguration[streamName] (string)

### liveStream.appendRecording
Append recorded video to live entry


```js
kaltura.liveStream.appendRecording({
  "entryId": "",
  "assetId": "",
  "mediaServerIndex": "",
  "duration": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live entry id
* assetId (string) **required** - Live asset id
* mediaServerIndex (string) **required** - Enum Type: `KalturaEntryServerNodeType`
* resource[objectType] (string)
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* duration (number) **required** - in seconds
* isLastChunk (boolean) - Is this the last recorded chunk in the current session (i.e. following a stream stop event)

### liveStream.authenticate
Authenticate live-stream entry against stream token and partner limitations


```js
kaltura.liveStream.authenticate({
  "entryId": "",
  "token": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live stream entry id
* token (string) **required** - Live stream broadcasting token
* hostname (string) - Media server host name
* mediaServerIndex (string) - Enum Type: `KalturaEntryServerNodeType`
* applicationName (string) - the application to which entry is being broadcast

### liveStream.createPeriodicSyncPoints
Creates perioding metadata sync-point events on a live stream


```js
kaltura.liveStream.createPeriodicSyncPoints({
  "entryId": "",
  "interval": 0,
  "duration": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Kaltura live-stream entry id
* interval (integer) **required** - Events interval in seconds
* duration (integer) **required** - Duration in seconds

### liveStream.delete
Delete a live stream entry.


```js
kaltura.liveStream.delete({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live stream entry id to delete

### liveStream.get
Get live stream entry by ID.


```js
kaltura.liveStream.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live stream entry id
* version (integer) - Desired version of the data

### liveStream.isLive
Delivering the status of a live stream (on-air/offline) if it is possible


```js
kaltura.liveStream.isLive({
  "id": "",
  "protocol": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - ID of the live stream
* protocol (string) **required** - Enum Type: `KalturaPlaybackProtocol`

### liveStream.list
List live stream entries by filter with paging support.


```js
kaltura.liveStream.list({}, context)
```


### liveStream.regenerateStreamToken
Regenerate new secure token for liveStream


```js
kaltura.liveStream.regenerateStreamToken({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live stream entry id to regenerate secure token for

### liveStream.registerMediaServer
Register media server to live entry


```js
kaltura.liveStream.registerMediaServer({
  "entryId": "",
  "hostname": "",
  "mediaServerIndex": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live entry id
* hostname (string) **required** - Media server host name
* mediaServerIndex (string) **required** - Enum Type: `KalturaEntryServerNodeType`
* applicationName (string) - the application to which entry is being broadcast
* liveEntryStatus (integer) - Enum Type: `KalturaEntryServerNodeStatus`

### liveStream.removeLiveStreamPushPublishConfiguration
Remove push publish configuration from entry


```js
kaltura.liveStream.removeLiveStreamPushPublishConfiguration({
  "entryId": "",
  "protocol": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* protocol (string) **required** - Enum Type: `KalturaPlaybackProtocol`

### liveStream.setRecordedContent
Sey recorded video to live entry


```js
kaltura.liveStream.setRecordedContent({
  "entryId": "",
  "mediaServerIndex": "",
  "duration": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live entry id
* mediaServerIndex (string) **required** - Enum Type: `KalturaEntryServerNodeType`
* resource[objectType] (string)
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* duration (number) **required** - in seconds
* recordedEntryId (string) - Recorded entry Id
* flavorParamsId (integer) - Recorded entry Id

### liveStream.unregisterMediaServer
Unregister media server from live entry


```js
kaltura.liveStream.unregisterMediaServer({
  "entryId": "",
  "hostname": "",
  "mediaServerIndex": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live entry id
* hostname (string) **required** - Media server host name
* mediaServerIndex (string) **required** - Enum Type: `KalturaEntryServerNodeType`

### liveStream.update
Update live stream entry. Only the properties that were set will be updated.


```js
kaltura.liveStream.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live stream entry id to update
* liveStreamEntry[name] (string) - Entry name (Min 1 chars)
* liveStreamEntry[description] (string) - Entry description
* liveStreamEntry[userId] (string) - The ID of the user who is the owner of this entry
* liveStreamEntry[creatorId] (string) - `insertOnly`
* liveStreamEntry[tags] (string) - Entry tags
* liveStreamEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* liveStreamEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* liveStreamEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* liveStreamEntry[type] (string) - Enum Type: `KalturaEntryType`
* liveStreamEntry[groupId] (integer)
* liveStreamEntry[partnerData] (string) - Can be used to store various partner related data as a string
* liveStreamEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* liveStreamEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* liveStreamEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* liveStreamEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* liveStreamEntry[referenceId] (string) - Entry external reference id
* liveStreamEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* liveStreamEntry[conversionProfileId] (integer) - Override the default ingestion profile
* liveStreamEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* liveStreamEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* liveStreamEntry[operationAttributes] (array)
* liveStreamEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* liveStreamEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* liveStreamEntry[templateEntryId] (string) - `insertOnly`
* liveStreamEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* liveStreamEntry[msDuration] (integer) - The duration in miliseconds
* liveStreamEntry[mediaType] (integer) - `insertOnly`
* liveStreamEntry[conversionQuality] (string) - `insertOnly`
* liveStreamEntry[sourceType] (string) - `insertOnly`
* liveStreamEntry[searchProviderType] (integer) - `insertOnly`
* liveStreamEntry[searchProviderId] (string) - `insertOnly`
* liveStreamEntry[creditUserName] (string) - The user name used for credits
* liveStreamEntry[creditUrl] (string) - The URL for credits
* liveStreamEntry[streams] (array)
* liveStreamEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* liveStreamEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* liveStreamEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* liveStreamEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* liveStreamEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* liveStreamEntry[liveStreamConfigurations] (array)
* liveStreamEntry[recordedEntryId] (string) - Recorded entry id
* liveStreamEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* liveStreamEntry[publishConfigurations] (array)
* liveStreamEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* liveStreamEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* liveStreamEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* liveStreamEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* liveStreamEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* liveStreamEntry[bitrates] (array)
* liveStreamEntry[primaryBroadcastingUrl] (string)
* liveStreamEntry[secondaryBroadcastingUrl] (string)
* liveStreamEntry[primaryRtspBroadcastingUrl] (string)
* liveStreamEntry[secondaryRtspBroadcastingUrl] (string)
* liveStreamEntry[streamName] (string)
* liveStreamEntry[streamUrl] (string) - The stream url
* liveStreamEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* liveStreamEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* liveStreamEntry[encodingIP1] (string) - The broadcast primary ip
* liveStreamEntry[encodingIP2] (string) - The broadcast secondary ip
* liveStreamEntry[streamPassword] (string) - The broadcast password
* liveStreamEntry[objectType] (string)

### liveStream.updateOfflineThumbnailFromUrl
Update entry thumbnail using url


```js
kaltura.liveStream.updateOfflineThumbnailFromUrl({
  "entryId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - live stream entry id
* url (string) **required** - file url

### liveStream.updateOfflineThumbnailJpeg
Update live stream entry thumbnail using a raw jpeg file


```js
kaltura.liveStream.updateOfflineThumbnailJpeg({
  "entryId": "",
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - live stream entry id
* fileData (string) **required** - Jpeg file data

### liveStream.validateRegisteredMediaServers
Validates all registered media servers


```js
kaltura.liveStream.validateRegisteredMediaServers({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Live entry id

### media.add
Add entry


```js
kaltura.media.add({}, context)
```


### media.addContent
Add content to media entry which is not yet associated with content (therefore is in status NO_CONTENT).
     If the requirement is to replace the entry's associated content, use action updateContent.


```js
kaltura.media.addContent({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* resource[objectType] (string)
* resource[resource][objectType] (string)
* resource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][assetId] (string) - ID of the source asset
* resource[resource][entryId] (string) - ID of the source entry
* resource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][objectId] (string) - The object id of the file sync object
* resource[resource][version] (string) - The version of the file sync object
* resource[resource][resource][objectType] (string)
* resource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][objectType] (string)
* resource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][resources] (array)
* resource[resource][resource][resource][content] (string) - Textual content
* resource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resource][resources] (array)
* resource[resource][resource][content] (string) - Textual content
* resource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resources] (array)
* resource[resource][content] (string) - Textual content
* resource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][privateKey] (string) - SSH private key
* resource[resource][publicKey] (string) - SSH public key
* resource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][localFilePath] (string) - Full path to the local file
* resource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][fileData] (string) - Represents the $_FILE
* resource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resources] (array)
* resource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[forceAsyncDownload] (boolean) - Force Import Job
* resource[assetId] (string) - ID of the source asset
* resource[entryId] (string) - ID of the source entry
* resource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[fileSyncObjectType] (integer) - The object type of the file sync object
* resource[objectSubType] (integer) - The object sub-type of the file sync object
* resource[objectId] (string) - The object id of the file sync object
* resource[version] (string) - The version of the file sync object
* resource[content] (string) - Textual content
* resource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[privateKey] (string) - SSH private key
* resource[publicKey] (string) - SSH public key
* resource[keyPassphrase] (string) - Passphrase for SSH keys
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### media.addFromBulk
Adds new media entry by importing an HTTP or FTP URL.

The entry will be queued for import and then for conversion.

This action should be exposed only to the batches


```js
kaltura.media.addFromBulk({
  "url": "",
  "bulkUploadId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* url (string) **required** - An HTTP or FTP URL
* bulkUploadId (integer) **required** - The id of the bulk upload job

### media.addFromEntry
Copy entry into new entry


```js
kaltura.media.addFromEntry({
  "sourceEntryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* sourceEntryId (string) **required** - Media entry id to copy from
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* sourceFlavorParamsId (integer) - The flavor to be used as the new entry source, source flavor will be used if not specified

### media.addFromFlavorAsset
Copy flavor asset into new entry


```js
kaltura.media.addFromFlavorAsset({
  "sourceFlavorAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* sourceFlavorAssetId (string) **required** - Flavor asset id to be used as the new entry source
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password

### media.addFromRecordedWebcam
Add new entry after the file was recored on the server and the token id exists


```js
kaltura.media.addFromRecordedWebcam({
  "webcamTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* webcamTokenId (string) **required** - Token id for the recored webcam file

### media.addFromSearchResult
Adds new media entry by importing the media file from a search provider.

This action should be used with the search service result.


```js
kaltura.media.addFromSearchResult({}, context)
```


### media.addFromUploadedFile
Add new entry after the specific media file was uploaded and the upload token id exists


```js
kaltura.media.addFromUploadedFile({
  "uploadTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* uploadTokenId (string) **required** - Upload token id

### media.addFromUrl
Adds new media entry by importing an HTTP or FTP URL.

The entry will be queued for import and then for conversion.


```js
kaltura.media.addFromUrl({
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password
* url (string) **required** - An HTTP or FTP URL

### media.anonymousRank
Anonymously rank a media entry, no validation is done on duplicate rankings


```js
kaltura.media.anonymousRank({
  "entryId": "",
  "rank": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* rank (integer) **required**

### media.approve
Approve the media entry and mark the pending flags (if any) as moderated (this will make the entry playable)


```js
kaltura.media.approve({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### media.approveReplace
Approves media replacement


```js
kaltura.media.approveReplace({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id to replace

### media.bulkUploadAdd
Add new bulk upload batch job

Conversion profile id can be specified in the API or in the CSV file, the one in the CSV file will be stronger.

If no conversion profile was specified, partner's default will be used


```js
kaltura.media.bulkUploadAdd({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries
* bulkUploadEntryData[conversionProfileId] (integer) - Selected profile id for all bulk entries

### media.cancelReplace
Cancels media replacement


```js
kaltura.media.cancelReplace({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id to cancel

### media.convert
Convert entry


```js
kaltura.media.convert({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* conversionProfileId (integer)

### media.count
Count media entries by filter.


```js
kaltura.media.count({}, context)
```


### media.delete
Delete a media entry.


```js
kaltura.media.delete({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id to delete

### media.flag
Flag inappropriate media entry for moderation


```js
kaltura.media.flag({}, context)
```


### media.get
Get media entry by ID.


```js
kaltura.media.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* version (integer) - Desired version of the data

### media.getMrss
Get MRSS by entry id
     XML will return as an escaped string


```js
kaltura.media.getMrss({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Entry id
* features (string)

### media.list
List media entries by filter with paging support.


```js
kaltura.media.list({}, context)
```


### media.listFlags
List all pending flags for the media entry


```js
kaltura.media.listFlags({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### media.reject
Reject the media entry and mark the pending flags (if any) as moderated (this will make the entry non playable)


```js
kaltura.media.reject({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### media.requestConversion
Request a new conversion job, this can be used to convert the media entry to a different format


```js
kaltura.media.requestConversion({
  "entryId": "",
  "fileFormat": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* fileFormat (string) **required** - Format to convert

### media.update
Update media entry. Only the properties that were set will be updated.


```js
kaltura.media.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id to update
* mediaEntry[name] (string) - Entry name (Min 1 chars)
* mediaEntry[description] (string) - Entry description
* mediaEntry[userId] (string) - The ID of the user who is the owner of this entry
* mediaEntry[creatorId] (string) - `insertOnly`
* mediaEntry[tags] (string) - Entry tags
* mediaEntry[adminTags] (string) - Entry admin tags can be updated only by administrators
* mediaEntry[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* mediaEntry[type] (string) - Enum Type: `KalturaEntryType`
* mediaEntry[groupId] (integer)
* mediaEntry[partnerData] (string) - Can be used to store various partner related data as a string
* mediaEntry[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* mediaEntry[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* mediaEntry[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* mediaEntry[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* mediaEntry[referenceId] (string) - Entry external reference id
* mediaEntry[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* mediaEntry[conversionProfileId] (integer) - Override the default ingestion profile
* mediaEntry[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* mediaEntry[parentEntryId] (string) - ID of source root entry, used for defining entires association
* mediaEntry[operationAttributes] (array)
* mediaEntry[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* mediaEntry[templateEntryId] (string) - `insertOnly`
* mediaEntry[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* mediaEntry[msDuration] (integer) - The duration in miliseconds
* mediaEntry[mediaType] (integer) - `insertOnly`
* mediaEntry[conversionQuality] (string) - `insertOnly`
* mediaEntry[sourceType] (string) - `insertOnly`
* mediaEntry[searchProviderType] (integer) - `insertOnly`
* mediaEntry[searchProviderId] (string) - `insertOnly`
* mediaEntry[creditUserName] (string) - The user name used for credits
* mediaEntry[creditUrl] (string) - The URL for credits
* mediaEntry[streams] (array)
* mediaEntry[objectType] (string)
* mediaEntry[externalSourceType] (string) - `insertOnly`
* mediaEntry[offlineMessage] (string) - The message to be presented when the stream is offline
* mediaEntry[recordStatus] (integer) - Enum Type: `KalturaRecordStatus`
* mediaEntry[dvrStatus] (integer) - Enum Type: `KalturaDVRStatus`
* mediaEntry[dvrWindow] (integer) - Window of time which the DVR allows for backwards scrubbing (in minutes)
* mediaEntry[lastElapsedRecordingTime] (integer) - Elapsed recording time (in msec) up to the point where the live stream was last stopped (unpublished).
* mediaEntry[liveStreamConfigurations] (array)
* mediaEntry[recordedEntryId] (string) - Recorded entry id
* mediaEntry[pushPublishEnabled] (integer) - Enum Type: `KalturaLivePublishStatus`
* mediaEntry[publishConfigurations] (array)
* mediaEntry[currentBroadcastStartTime] (number) - The time (unix timestamp in milliseconds) in which the entry broadcast started or 0 when the entry is off the air
* mediaEntry[recordingOptions][shouldCopyEntitlement] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyScheduling] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldCopyThumbnail] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[recordingOptions][shouldMakeHidden] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[playlistId] (string) - Playlist id to be played
* mediaEntry[repeat] (integer) - Enum Type: `KalturaNullableBoolean`
* mediaEntry[bitrates] (array)
* mediaEntry[primaryBroadcastingUrl] (string)
* mediaEntry[secondaryBroadcastingUrl] (string)
* mediaEntry[primaryRtspBroadcastingUrl] (string)
* mediaEntry[secondaryRtspBroadcastingUrl] (string)
* mediaEntry[streamName] (string)
* mediaEntry[streamUrl] (string) - The stream url
* mediaEntry[hlsStreamUrl] (string) - HLS URL - URL for live stream playback on mobile device
* mediaEntry[urlManager] (string) - URL Manager to handle the live stream URL (for instance, add token)
* mediaEntry[encodingIP1] (string) - The broadcast primary ip
* mediaEntry[encodingIP2] (string) - The broadcast secondary ip
* mediaEntry[streamPassword] (string) - The broadcast password

### media.updateContent
Replace content associated with the media entry.


```js
kaltura.media.updateContent({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id to update
* resource[objectType] (string)
* resource[resource][objectType] (string)
* resource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][assetId] (string) - ID of the source asset
* resource[resource][entryId] (string) - ID of the source entry
* resource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][objectId] (string) - The object id of the file sync object
* resource[resource][version] (string) - The version of the file sync object
* resource[resource][resource][objectType] (string)
* resource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][objectType] (string)
* resource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* resource[resource][resource][resource][assetId] (string) - ID of the source asset
* resource[resource][resource][resource][entryId] (string) - ID of the source entry
* resource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* resource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* resource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* resource[resource][resource][resource][version] (string) - The version of the file sync object
* resource[resource][resource][resource][resources] (array)
* resource[resource][resource][resource][content] (string) - Textual content
* resource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resource][resources] (array)
* resource[resource][resource][content] (string) - Textual content
* resource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][resource][privateKey] (string) - SSH private key
* resource[resource][resource][publicKey] (string) - SSH public key
* resource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][resource][localFilePath] (string) - Full path to the local file
* resource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][resource][fileData] (string) - Represents the $_FILE
* resource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resource][resources] (array)
* resource[resource][content] (string) - Textual content
* resource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[resource][privateKey] (string) - SSH private key
* resource[resource][publicKey] (string) - SSH public key
* resource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* resource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* resource[resource][localFilePath] (string) - Full path to the local file
* resource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[resource][fileData] (string) - Represents the $_FILE
* resource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* resource[resources] (array)
* resource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* resource[forceAsyncDownload] (boolean) - Force Import Job
* resource[assetId] (string) - ID of the source asset
* resource[entryId] (string) - ID of the source entry
* resource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* resource[fileSyncObjectType] (integer) - The object type of the file sync object
* resource[objectSubType] (integer) - The object sub-type of the file sync object
* resource[objectId] (string) - The object id of the file sync object
* resource[version] (string) - The version of the file sync object
* resource[content] (string) - Textual content
* resource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* resource[privateKey] (string) - SSH private key
* resource[publicKey] (string) - SSH public key
* resource[keyPassphrase] (string) - Passphrase for SSH keys
* resource[dropFolderFileId] (integer) - Id of the drop folder file object
* resource[localFilePath] (string) - Full path to the local file
* resource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* resource[fileData] (string) - Represents the $_FILE
* resource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* conversionProfileId (integer) - The conversion profile id to be used on the entry
* advancedOptions[keepManualThumbnails] (integer) - If true manually created thumbnails will not be deleted on entry replacement
* advancedOptions[pluginOptionItems] (array)

### media.updateThumbnail
Update media entry thumbnail by a specified time offset (In seconds)

If flavor params id not specified, source flavor will be used by default


```js
kaltura.media.updateThumbnail({
  "entryId": "",
  "timeOffset": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* timeOffset (integer) **required** - Time offset (in seconds)
* flavorParamsId (integer) - The flavor params id to be used

### media.updateThumbnailFromSourceEntry
Update media entry thumbnail from a different entry by a specified time offset (In seconds)

If flavor params id not specified, source flavor will be used by default


```js
kaltura.media.updateThumbnailFromSourceEntry({
  "entryId": "",
  "sourceEntryId": "",
  "timeOffset": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* sourceEntryId (string) **required** - Media entry id
* timeOffset (integer) **required** - Time offset (in seconds)
* flavorParamsId (integer) - The flavor params id to be used

### media.updateThumbnailFromUrl
Update entry thumbnail using url


```js
kaltura.media.updateThumbnailFromUrl({
  "entryId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* url (string) **required** - file url

### media.updateThumbnailJpeg
Update media entry thumbnail using a raw jpeg file


```js
kaltura.media.updateThumbnailJpeg({
  "entryId": "",
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required** - Media entry id
* fileData (string) **required** - Jpeg file data

### media.upload
Upload a media file to Kaltura, then the file can be used to create a media entry.


```js
kaltura.media.upload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required** - The file data

### mediaInfo.list
List media info objects by filter and pager


```js
kaltura.mediaInfo.list({}, context)
```


### metadata.add
Allows you to add a metadata object and metadata content associated with Kaltura object


```js
kaltura.metadata.add({
  "metadataProfileId": 0,
  "objectType": "",
  "objectId": "",
  "xmlData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required**
* objectType (string) **required** - Enum Type: `KalturaMetadataObjectType`
* objectId (string) **required**
* xmlData (string) **required** - XML metadata

### metadata.addFromBulk
Allows you to add a metadata xml data from remote URL.

Enables different permissions than addFromUrl action.


```js
kaltura.metadata.addFromBulk({
  "metadataProfileId": 0,
  "objectType": "",
  "objectId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required**
* objectType (string) **required** - Enum Type: `KalturaMetadataObjectType`
* objectId (string) **required**
* url (string) **required** - XML metadata remote url

### metadata.addFromFile
Allows you to add a metadata object and metadata file associated with Kaltura object


```js
kaltura.metadata.addFromFile({
  "metadataProfileId": 0,
  "objectType": "",
  "objectId": "",
  "xmlFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required**
* objectType (string) **required** - Enum Type: `KalturaMetadataObjectType`
* objectId (string) **required**
* xmlFile (string) **required** - XML metadata

### metadata.addFromUrl
Allows you to add a metadata xml data from remote URL


```js
kaltura.metadata.addFromUrl({
  "metadataProfileId": 0,
  "objectType": "",
  "objectId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required**
* objectType (string) **required** - Enum Type: `KalturaMetadataObjectType`
* objectId (string) **required**
* url (string) **required** - XML metadata remote url

### metadata.delete
Delete an existing metadata


```js
kaltura.metadata.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadata.get
Retrieve a metadata object by id


```js
kaltura.metadata.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadata.index
Index metadata by id, will also index the related object


```js
kaltura.metadata.index({
  "id": "",
  "shouldUpdate": true
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* shouldUpdate (boolean) **required**

### metadata.invalidate
Mark existing metadata as invalid

Used by batch metadata transform


```js
kaltura.metadata.invalidate({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* version (integer) - Enable update only if the metadata object version did not change by other process

### metadata.list
List metadata objects by filter and pager


```js
kaltura.metadata.list({}, context)
```


### metadata.serve
Serves metadata XML file


```js
kaltura.metadata.serve({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadata.update
Update an existing metadata object with new XML content


```js
kaltura.metadata.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* xmlData (string) - XML metadata
* version (integer) - Enable update only if the metadata object version did not change by other process

### metadata.updateFromFile
Update an existing metadata object with new XML file


```js
kaltura.metadata.updateFromFile({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* xmlFile (string) - XML metadata

### metadata.updateFromXSL
Action transforms current metadata object XML using a provided XSL.


```js
kaltura.metadata.updateFromXSL({
  "id": 0,
  "xslFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* xslFile (string) **required**

### metadataBatch.getExclusiveTransformMetadataJobs
batch getExclusiveTransformMetadataJob action allows to get a BatchJob of type METADATA_TRANSFORM


```js
kaltura.metadataBatch.getExclusiveTransformMetadataJobs({
  "maxExecutionTime": 0,
  "numberOfJobs": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* lockKey[schedulerId] (integer)
* lockKey[workerId] (integer)
* lockKey[batchIndex] (integer)
* maxExecutionTime (integer) **required** - The maximum time in seconds the job reguarly take. Is used for the locking mechanism when determining an unexpected termination of a batch-process.
* numberOfJobs (integer) **required** - The maximum number of jobs to return.
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[idEqual] (integer)
* filter[idGreaterThanOrEqual] (integer)
* filter[partnerIdEqual] (integer)
* filter[partnerIdIn] (string)
* filter[partnerIdNotIn] (string)
* filter[createdAtGreaterThanOrEqual] (integer)
* filter[createdAtLessThanOrEqual] (integer)
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[executionAttemptsGreaterThanOrEqual] (integer)
* filter[executionAttemptsLessThanOrEqual] (integer)
* filter[lockVersionGreaterThanOrEqual] (integer)
* filter[lockVersionLessThanOrEqual] (integer)
* filter[entryIdEqual] (string)
* filter[jobTypeEqual] (string) - Enum Type: `KalturaBatchJobType`
* filter[jobTypeIn] (string)
* filter[jobTypeNotIn] (string)
* filter[jobSubTypeEqual] (integer)
* filter[jobSubTypeIn] (string)
* filter[jobSubTypeNotIn] (string)
* filter[statusEqual] (integer) - Enum Type: `KalturaBatchJobStatus`
* filter[statusIn] (string)
* filter[statusNotIn] (string)
* filter[priorityGreaterThanOrEqual] (integer)
* filter[priorityLessThanOrEqual] (integer)
* filter[priorityEqual] (integer)
* filter[priorityIn] (string)
* filter[priorityNotIn] (string)
* filter[batchVersionGreaterThanOrEqual] (integer)
* filter[batchVersionLessThanOrEqual] (integer)
* filter[batchVersionEqual] (integer)
* filter[queueTimeGreaterThanOrEqual] (integer)
* filter[queueTimeLessThanOrEqual] (integer)
* filter[finishTimeGreaterThanOrEqual] (integer)
* filter[finishTimeLessThanOrEqual] (integer)
* filter[errTypeEqual] (integer) - Enum Type: `KalturaBatchJobErrorTypes`
* filter[errTypeIn] (string)
* filter[errTypeNotIn] (string)
* filter[errNumberEqual] (integer)
* filter[errNumberIn] (string)
* filter[errNumberNotIn] (string)
* filter[estimatedEffortLessThan] (integer)
* filter[estimatedEffortGreaterThan] (integer)
* filter[urgencyLessThanOrEqual] (integer)
* filter[urgencyGreaterThanOrEqual] (integer)
* filter[objectType] (string)
* filter[jobTypeAndSubTypeIn] (string)
* maxJobToPull (integer) - The maximum job we will pull from the DB into the cache

### metadataBatch.getTransformMetadataObjects
batch getTransformMetadataObjects action retrieve all metadata objects that requires upgrade and the total count


```js
kaltura.metadataBatch.getTransformMetadataObjects({
  "metadataProfileId": 0,
  "srcVersion": 0,
  "destVersion": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required** - The id of the metadata profile
* srcVersion (integer) **required** - The old metadata profile version
* destVersion (integer) **required** - The new metadata profile version
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### metadataProfile.add
Allows you to add a metadata profile object and metadata profile content associated with Kaltura object type


```js
kaltura.metadataProfile.add({
  "xsdData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfile[metadataObjectType] (string) - Enum Type: `KalturaMetadataObjectType`
* metadataProfile[name] (string)
* metadataProfile[systemName] (string)
* metadataProfile[description] (string)
* metadataProfile[createMode] (integer) - Enum Type: `KalturaMetadataProfileCreateMode`
* metadataProfile[disableReIndexing] (boolean)
* xsdData (string) **required** - XSD metadata definition
* viewsData (string) - UI views definition

### metadataProfile.addFromFile
Allows you to add a metadata profile object and metadata profile file associated with Kaltura object type


```js
kaltura.metadataProfile.addFromFile({
  "xsdFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfile[metadataObjectType] (string) - Enum Type: `KalturaMetadataObjectType`
* metadataProfile[name] (string)
* metadataProfile[systemName] (string)
* metadataProfile[description] (string)
* metadataProfile[createMode] (integer) - Enum Type: `KalturaMetadataProfileCreateMode`
* metadataProfile[disableReIndexing] (boolean)
* xsdFile (string) **required** - XSD metadata definition
* viewsFile (string) - UI views definition

### metadataProfile.delete
Delete an existing metadata profile


```js
kaltura.metadataProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadataProfile.get
Retrieve a metadata profile object by id


```js
kaltura.metadataProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadataProfile.list
List metadata profile objects by filter and pager


```js
kaltura.metadataProfile.list({}, context)
```


### metadataProfile.listFields
List metadata profile fields by metadata profile id


```js
kaltura.metadataProfile.listFields({
  "metadataProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* metadataProfileId (integer) **required**

### metadataProfile.revert
Update an existing metadata object definition file


```js
kaltura.metadataProfile.revert({
  "id": 0,
  "toVersion": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* toVersion (integer) **required**

### metadataProfile.serve
Serves metadata profile XSD file


```js
kaltura.metadataProfile.serve({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadataProfile.serveView
Serves metadata profile view file


```js
kaltura.metadataProfile.serveView({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### metadataProfile.update
Update an existing metadata object


```js
kaltura.metadataProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* metadataProfile[metadataObjectType] (string) - Enum Type: `KalturaMetadataObjectType`
* metadataProfile[name] (string)
* metadataProfile[systemName] (string)
* metadataProfile[description] (string)
* metadataProfile[createMode] (integer) - Enum Type: `KalturaMetadataProfileCreateMode`
* metadataProfile[disableReIndexing] (boolean)
* xsdData (string) - XSD metadata definition
* viewsData (string) - UI views definition

### metadataProfile.updateDefinitionFromFile
Update an existing metadata object definition file


```js
kaltura.metadataProfile.updateDefinitionFromFile({
  "id": 0,
  "xsdFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* xsdFile (string) **required** - XSD metadata definition

### metadataProfile.updateTransformationFromFile
Update an existing metadata object xslt file


```js
kaltura.metadataProfile.updateTransformationFromFile({
  "id": 0,
  "xsltFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* xsltFile (string) **required** - XSLT file, will be executed on every metadata add/update

### metadataProfile.updateViewsFromFile
Update an existing metadata object views file


```js
kaltura.metadataProfile.updateViewsFromFile({
  "id": 0,
  "viewsFile": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* viewsFile (string) **required** - UI views file

### filesyncImportBatch.extendFileSyncLock
batch extendFileSyncLock action extends the expiration of a file sync lock


```js
kaltura.filesyncImportBatch.extendFileSyncLock({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required** - The id of the file sync

### filesyncImportBatch.lockPendingFileSyncs
batch lockPendingFileSyncs action locks file syncs for import by the file sync periodic worker


```js
kaltura.filesyncImportBatch.lockPendingFileSyncs({
  "workerId": 0,
  "sourceDc": 0,
  "maxCount": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[partnerIdEqual] (integer)
* filter[fileObjectTypeEqual] (string) - Enum Type: `KalturaFileSyncObjectType`
* filter[fileObjectTypeIn] (string)
* filter[objectIdEqual] (string)
* filter[objectIdIn] (string)
* filter[versionEqual] (string)
* filter[versionIn] (string)
* filter[objectSubTypeEqual] (integer)
* filter[objectSubTypeIn] (string)
* filter[dcEqual] (string)
* filter[dcIn] (string)
* filter[originalEqual] (integer)
* filter[createdAtGreaterThanOrEqual] (integer)
* filter[createdAtLessThanOrEqual] (integer)
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[readyAtGreaterThanOrEqual] (integer)
* filter[readyAtLessThanOrEqual] (integer)
* filter[syncTimeGreaterThanOrEqual] (integer)
* filter[syncTimeLessThanOrEqual] (integer)
* filter[statusEqual] (integer) - Enum Type: `KalturaFileSyncStatus`
* filter[statusIn] (string)
* filter[fileTypeEqual] (integer) - Enum Type: `KalturaFileSyncType`
* filter[fileTypeIn] (string)
* filter[linkedIdEqual] (integer)
* filter[linkCountGreaterThanOrEqual] (integer)
* filter[linkCountLessThanOrEqual] (integer)
* filter[fileSizeGreaterThanOrEqual] (number)
* filter[fileSizeLessThanOrEqual] (number)
* filter[currentDc] (integer) - Enum Type: `KalturaNullableBoolean`
* workerId (integer) **required** - The id of the file sync import worker
* sourceDc (integer) **required** - The id of the DC from which the file syncs should be pulled
* maxCount (integer) **required** - The maximum number of file syncs that should be returned
* maxSize (integer) - The maximum total size of file syncs that should be returned, this limit may be exceeded by one file sync

### ndn.getFeed



```js
kaltura.ndn.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### notification.getClientNotification
Return the notifications for a specific entry id and type


```js
kaltura.notification.getClientNotification({
  "entryId": "",
  "type": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* type (integer) **required** - Enum Type: `KalturaNotificationType`

### partner.count
Count partner's existing sub-publishers (count includes the partner itself).


```js
kaltura.partner.count({}, context)
```


### partner.get
Retrieve partner object by Id


```js
kaltura.partner.get({}, context)
```


### partner.getInfo
Retrieve all info attributed to the partner

This action expects no parameters. It returns information for the current KS partnerId.


```js
kaltura.partner.getInfo({}, context)
```


### partner.getSecrets
Retrieve partner secret and admin secret


```js
kaltura.partner.getSecrets({
  "partnerId": 0,
  "adminEmail": "",
  "cmsPassword": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* partnerId (integer) **required**
* adminEmail (string) **required**
* cmsPassword (string) **required**

### partner.getStatistics
Get usage statistics for a partner

Calculation is done according to partner's package


```js
kaltura.partner.getStatistics({}, context)
```


### partner.getUsage
Get usage statistics for a partner

Calculation is done according to partner's package

Additional data returned is a graph points of streaming usage in a timeframe

The resolution can be "days" or "months"


```js
kaltura.partner.getUsage({}, context)
```


### partner.list
List partners by filter with paging support

Current implementation will only list the sub partners of the partner initiating the api call (using the current KS).

This action is only partially implemented to support listing sub partners of a VAR partner.


```js
kaltura.partner.list({}, context)
```


### partner.listFeatureStatus
List partner's current processes' statuses


```js
kaltura.partner.listFeatureStatus({}, context)
```


### partner.listPartnersForUser
Retrieve a list of partner objects which the current user is allowed to access.


```js
kaltura.partner.listPartnersForUser({}, context)
```


### partner.register
Create a new Partner object


```js
kaltura.partner.register({}, context)
```


### partner.update
Update details and settings of an existing partner


```js
kaltura.partner.update({}, context)
```


### permission.add
Adds a new permission object to the account.


```js
kaltura.permission.add({}, context)
```


### permission.delete
Deletes an existing permission object.


```js
kaltura.permission.delete({
  "permissionName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionName (string) **required** - The name assigned to the permission

### permission.get
Retrieves a permission object using its ID.


```js
kaltura.permission.get({
  "permissionName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionName (string) **required** - The name assigned to the permission

### permission.getCurrentPermissions
Retrieves a list of permissions that apply to the current KS.


```js
kaltura.permission.getCurrentPermissions({}, context)
```


### permission.list
Lists permission objects that are associated with an account.

Blocked permissions are listed unless you use a filter to exclude them.

Blocked permissions are listed unless you use a filter to exclude them.


```js
kaltura.permission.list({}, context)
```


### permission.update
Updates an existing permission object.


```js
kaltura.permission.update({
  "permissionName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionName (string) **required** - The name assigned to the permission
* permission[name] (string)
* permission[friendlyName] (string)
* permission[description] (string)
* permission[status] (integer) - Enum Type: `KalturaPermissionStatus`
* permission[dependsOnPermissionNames] (string)
* permission[tags] (string)
* permission[permissionItemsIds] (string)
* permission[partnerGroup] (string)

### permissionItem.add
Adds a new permission item object to the account.

This action is available only to Kaltura system administrators.


```js
kaltura.permissionItem.add({}, context)
```


### permissionItem.delete
Deletes an existing permission item object.

This action is available only to Kaltura system administrators.


```js
kaltura.permissionItem.delete({
  "permissionItemId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionItemId (integer) **required** - The permission item's unique identifier

### permissionItem.get
Retrieves a permission item object using its ID.


```js
kaltura.permissionItem.get({
  "permissionItemId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionItemId (integer) **required** - The permission item's unique identifier

### permissionItem.list
Lists permission item objects that are associated with an account.


```js
kaltura.permissionItem.list({}, context)
```


### permissionItem.update
Updates an existing permission item object.

This action is available only to Kaltura system administrators.


```js
kaltura.permissionItem.update({
  "permissionItemId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* permissionItemId (integer) **required** - The permission item's unique identifier
* permissionItem[tags] (string)
* permissionItem[objectType] (string)
* permissionItem[service] (string)
* permissionItem[action] (string)
* permissionItem[object] (string)
* permissionItem[parameter] (string)

### playlist.add
Add new playlist

Note that all entries used in a playlist will become public and may appear in KalturaNetwork


```js
kaltura.playlist.add({}, context)
```


### playlist.clone
Clone an existing playlist


```js
kaltura.playlist.clone({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - Id of the playlist to clone
* newPlaylist[name] (string) - Entry name (Min 1 chars)
* newPlaylist[description] (string) - Entry description
* newPlaylist[userId] (string) - The ID of the user who is the owner of this entry
* newPlaylist[creatorId] (string) - `insertOnly`
* newPlaylist[tags] (string) - Entry tags
* newPlaylist[adminTags] (string) - Entry admin tags can be updated only by administrators
* newPlaylist[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* newPlaylist[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* newPlaylist[type] (string) - Enum Type: `KalturaEntryType`
* newPlaylist[groupId] (integer)
* newPlaylist[partnerData] (string) - Can be used to store various partner related data as a string
* newPlaylist[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* newPlaylist[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* newPlaylist[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* newPlaylist[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* newPlaylist[referenceId] (string) - Entry external reference id
* newPlaylist[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* newPlaylist[conversionProfileId] (integer) - Override the default ingestion profile
* newPlaylist[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* newPlaylist[parentEntryId] (string) - ID of source root entry, used for defining entires association
* newPlaylist[operationAttributes] (array)
* newPlaylist[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* newPlaylist[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* newPlaylist[templateEntryId] (string) - `insertOnly`
* newPlaylist[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* newPlaylist[playlistContent] (string) - Content of the playlist - 
* newPlaylist[filters] (array)
* newPlaylist[totalResults] (integer) - Maximum count of results to be returned in playlist execution
* newPlaylist[playlistType] (integer) - Enum Type: `KalturaPlaylistType`

### playlist.delete
Delete existing playlist


```js
kaltura.playlist.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### playlist.execute
Retrieve playlist for playing purpose


```js
kaltura.playlist.execute({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* detailed (string)
* playlistContext[objectType] (string)
* playlistContext[entryId] (string) - The entry ID in the context of which the playlist should be built
* playlistContext[followEntryRedirect] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[orderBy] (string)
* filter[advancedSearch][objectType] (string)
* filter[advancedSearch][value] (string)
* filter[advancedSearch][categoriesMatchOr] (string)
* filter[advancedSearch][categoryEntryStatusIn] (string)
* filter[advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* filter[advancedSearch][categoryIdEqual] (integer)
* filter[advancedSearch][memberIdEq] (string)
* filter[advancedSearch][memberIdIn] (string)
* filter[advancedSearch][memberPermissionsMatchOr] (string)
* filter[advancedSearch][memberPermissionsMatchAnd] (string)
* filter[advancedSearch][noDistributionProfiles] (boolean)
* filter[advancedSearch][distributionProfileId] (integer)
* filter[advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* filter[advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* filter[advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* filter[advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* filter[advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* filter[advancedSearch][contentLike] (string)
* filter[advancedSearch][contentMultiLikeOr] (string)
* filter[advancedSearch][contentMultiLikeAnd] (string)
* filter[advancedSearch][cuePointsFreeText] (string)
* filter[advancedSearch][cuePointTypeIn] (string)
* filter[advancedSearch][cuePointSubTypeEqual] (integer)
* filter[advancedSearch][watermarkId] (integer)
* filter[advancedSearch][indexIdGreaterThan] (integer)
* filter[advancedSearch][depthGreaterThanEqual] (integer)
* filter[advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[advancedSearch][field] (string)
* filter[advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* filter[advancedSearch][items] (array)
* filter[advancedSearch][idEqual] (string)
* filter[advancedSearch][idIn] (string)
* filter[advancedSearch][userIdEqual] (string)
* filter[advancedSearch][userIdIn] (string)
* filter[advancedSearch][updatedAtGreaterThanOrEqual] (string)
* filter[advancedSearch][updatedAtLessThanOrEqual] (string)
* filter[advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* filter[advancedSearch][extendedStatusIn] (string)
* filter[advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* filter[advancedSearch][not] (boolean)
* filter[advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* filter[advancedSearch][metadataProfileId] (integer)
* filter[idEqual] (string) - This filter should be in use for retrieving only a specific entry (identified by its entryId).
* filter[idIn] (string) - This filter should be in use for retrieving few specific entries (string should include comma separated list of entryId strings).
* filter[idNotIn] (string)
* filter[nameLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry names (no wildcards, spaces are treated as part of the string).
* filter[nameMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* filter[nameMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* filter[nameEqual] (string) - This filter should be in use for retrieving entries with a specific name.
* filter[partnerIdEqual] (integer) - This filter should be in use for retrieving only entries which were uploaded by/assigned to users of a specific Kaltura Partner (identified by Partner ID).
* filter[partnerIdIn] (string) - This filter should be in use for retrieving only entries within Kaltura network which were uploaded by/assigned to users of few Kaltura Partners  (string should include comma separated list of PartnerIDs)
* filter[userIdEqual] (string) - This filter parameter should be in use for retrieving only entries, uploaded by/assigned to a specific user (identified by user Id).
* filter[userIdIn] (string)
* filter[userIdNotIn] (string)
* filter[creatorIdEqual] (string)
* filter[tagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags (no wildcards, spaces are treated as part of the string).
* filter[tagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* filter[tagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* filter[adminTagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags set by an ADMIN user (no wildcards, spaces are treated as part of the string).
* filter[adminTagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* filter[adminTagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* filter[categoriesMatchAnd] (string)
* filter[categoriesMatchOr] (string) - All entries within these categories or their child categories.
* filter[categoriesNotContains] (string)
* filter[categoriesIdsMatchAnd] (string)
* filter[categoriesIdsMatchOr] (string) - All entries of the categories, excluding their child categories.
* filter[categoriesIdsNotContains] (string)
* filter[categoriesIdsEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[statusEqual] (string) - Enum Type: `KalturaEntryStatus`
* filter[statusNotEqual] (string) - Enum Type: `KalturaEntryStatus`
* filter[statusIn] (string) - This filter should be in use for retrieving only entries, at few specific {
* filter[statusNotIn] (string) - This filter should be in use for retrieving only entries, not at few specific {
* filter[moderationStatusEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* filter[moderationStatusNotEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* filter[moderationStatusIn] (string)
* filter[moderationStatusNotIn] (string)
* filter[typeEqual] (string) - Enum Type: `KalturaEntryType`
* filter[typeIn] (string) - This filter should be in use for retrieving entries of few {
* filter[createdAtGreaterThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system after a specific time/date (standard timestamp format).
* filter[createdAtLessThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system before a specific time/date (standard timestamp format).
* filter[updatedAtGreaterThanOrEqual] (integer)
* filter[updatedAtLessThanOrEqual] (integer)
* filter[totalRankLessThanOrEqual] (integer)
* filter[totalRankGreaterThanOrEqual] (integer)
* filter[groupIdEqual] (integer)
* filter[searchTextMatchAnd] (string) - This filter should be in use for retrieving specific entries while search match the input string within all of the following metadata attributes: name, description, tags, adminTags.
* filter[searchTextMatchOr] (string) - This filter should be in use for retrieving specific entries while search match the input string within at least one of the following metadata attributes: name, description, tags, adminTags.
* filter[accessControlIdEqual] (integer)
* filter[accessControlIdIn] (string)
* filter[startDateGreaterThanOrEqual] (integer)
* filter[startDateLessThanOrEqual] (integer)
* filter[startDateGreaterThanOrEqualOrNull] (integer)
* filter[startDateLessThanOrEqualOrNull] (integer)
* filter[endDateGreaterThanOrEqual] (integer)
* filter[endDateLessThanOrEqual] (integer)
* filter[endDateGreaterThanOrEqualOrNull] (integer)
* filter[endDateLessThanOrEqualOrNull] (integer)
* filter[referenceIdEqual] (string)
* filter[referenceIdIn] (string)
* filter[replacingEntryIdEqual] (string)
* filter[replacingEntryIdIn] (string)
* filter[replacedEntryIdEqual] (string)
* filter[replacedEntryIdIn] (string)
* filter[replacementStatusEqual] (string) - Enum Type: `KalturaEntryReplacementStatus`
* filter[replacementStatusIn] (string)
* filter[partnerSortValueGreaterThanOrEqual] (integer)
* filter[partnerSortValueLessThanOrEqual] (integer)
* filter[rootEntryIdEqual] (string)
* filter[rootEntryIdIn] (string)
* filter[parentEntryIdEqual] (string)
* filter[entitledUsersEditMatchAnd] (string)
* filter[entitledUsersEditMatchOr] (string)
* filter[entitledUsersPublishMatchAnd] (string)
* filter[entitledUsersPublishMatchOr] (string)
* filter[tagsNameMultiLikeOr] (string)
* filter[tagsAdminTagsMultiLikeOr] (string)
* filter[tagsAdminTagsNameMultiLikeOr] (string)
* filter[tagsNameMultiLikeAnd] (string)
* filter[tagsAdminTagsMultiLikeAnd] (string)
* filter[tagsAdminTagsNameMultiLikeAnd] (string)
* filter[freeText] (string)
* filter[isRoot] (integer) - Enum Type: `KalturaNullableBoolean`
* filter[categoriesFullNameIn] (string)
* filter[categoryAncestorIdIn] (string) - All entries within this categoy or in child categories
* filter[redirectFromEntryId] (string) - The id of the original entry
* filter[lastPlayedAtGreaterThanOrEqual] (integer)
* filter[lastPlayedAtLessThanOrEqual] (integer)
* filter[durationLessThan] (integer)
* filter[durationGreaterThan] (integer)
* filter[durationLessThanOrEqual] (integer)
* filter[durationGreaterThanOrEqual] (integer)
* filter[durationTypeMatchOr] (string)
* filter[mediaTypeEqual] (integer) - Enum Type: `KalturaMediaType`
* filter[mediaTypeIn] (string)
* filter[sourceTypeEqual] (string) - Enum Type: `KalturaSourceType`
* filter[sourceTypeNotEqual] (string) - Enum Type: `KalturaSourceType`
* filter[sourceTypeIn] (string)
* filter[sourceTypeNotIn] (string)
* filter[mediaDateGreaterThanOrEqual] (integer)
* filter[mediaDateLessThanOrEqual] (integer)
* filter[flavorParamsIdsMatchOr] (string)
* filter[flavorParamsIdsMatchAnd] (string)
* filter[limit] (integer)
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### playlist.executeFromContent
Retrieve playlist for playing purpose, based on content


```js
kaltura.playlist.executeFromContent({
  "playlistType": 0,
  "playlistContent": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* playlistType (integer) **required** - Enum Type: `KalturaPlaylistType`
* playlistContent (string) **required**
* detailed (string)
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### playlist.executeFromFilters
Revrieve playlist for playing purpose, based on media entry filters


```js
kaltura.playlist.executeFromFilters({
  "totalResults": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* totalResults (integer) **required**
* detailed (string)
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).

### playlist.get
Retrieve a playlist


```js
kaltura.playlist.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* version (integer) - Desired version of the data

### playlist.getStatsFromContent
Retrieve playlist statistics


```js
kaltura.playlist.getStatsFromContent({
  "playlistType": 0,
  "playlistContent": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* playlistType (integer) **required** - Enum Type: `KalturaPlaylistType`
* playlistContent (string) **required**

### playlist.list
List available playlists


```js
kaltura.playlist.list({}, context)
```


### playlist.update
Update existing playlist

Note - you cannot change playlist type. updated playlist must be of the same type.


```js
kaltura.playlist.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* playlist[name] (string) - Entry name (Min 1 chars)
* playlist[description] (string) - Entry description
* playlist[userId] (string) - The ID of the user who is the owner of this entry
* playlist[creatorId] (string) - `insertOnly`
* playlist[tags] (string) - Entry tags
* playlist[adminTags] (string) - Entry admin tags can be updated only by administrators
* playlist[categories] (string) - Comma separated list of full names of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* playlist[categoriesIds] (string) - Comma separated list of ids of categories to which this entry belongs. Only categories that don't have entitlement (privacy context) are listed, to retrieve the full list of categories, use the categoryEntry.list action.
* playlist[type] (string) - Enum Type: `KalturaEntryType`
* playlist[groupId] (integer)
* playlist[partnerData] (string) - Can be used to store various partner related data as a string
* playlist[licenseType] (integer) - Enum Type: `KalturaLicenseType`
* playlist[accessControlId] (integer) - The Access Control ID assigned to this entry (null when not set, send -1 to remove)
* playlist[startDate] (integer) - Entry scheduling start date (null when not set, send -1 to remove)
* playlist[endDate] (integer) - Entry scheduling end date (null when not set, send -1 to remove)
* playlist[referenceId] (string) - Entry external reference id
* playlist[partnerSortValue] (integer) - Can be used to store various partner related data as a numeric value
* playlist[conversionProfileId] (integer) - Override the default ingestion profile
* playlist[redirectEntryId] (string) - IF not empty, points to an entry ID the should replace this current entry's id.
* playlist[parentEntryId] (string) - ID of source root entry, used for defining entires association
* playlist[operationAttributes] (array)
* playlist[entitledUsersEdit] (string) - list of user ids that are entitled to edit the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* playlist[entitledUsersPublish] (string) - list of user ids that are entitled to publish the entry (no server enforcement) The difference between entitledUsersEdit and entitledUsersPublish is applicative only
* playlist[templateEntryId] (string) - `insertOnly`
* playlist[displayInSearch] (integer) - Enum Type: `KalturaEntryDisplayInSearchType`
* playlist[playlistContent] (string) - Content of the playlist - 
* playlist[filters] (array)
* playlist[totalResults] (integer) - Maximum count of results to be returned in playlist execution
* playlist[playlistType] (integer) - Enum Type: `KalturaPlaylistType`
* updateStats (boolean)

### playReadyDrm.generateKey
Generate key id and content key for PlayReady encryption


```js
kaltura.playReadyDrm.generateKey({}, context)
```


### playReadyDrm.getContentKeys
Get content keys for input key ids


```js
kaltura.playReadyDrm.getContentKeys({
  "keyIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* keyIds (string) **required** - - comma separated key id's

### playReadyDrm.getEntryContentKey
Get content key and key id for the given entry


```js
kaltura.playReadyDrm.getEntryContentKey({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* createIfMissing (boolean)

### playReadyDrm.getLicenseDetails
Get Play Ready policy and dates for license creation


```js
kaltura.playReadyDrm.getLicenseDetails({
  "keyId": "",
  "deviceId": "",
  "deviceType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* keyId (string) **required**
* deviceId (string) **required**
* deviceType (integer) **required**
* entryId (string)
* referrer (string) - 64base encoded

### poll.add
Add Action


```js
kaltura.poll.add({}, context)
```


### poll.getVote
Vote Action


```js
kaltura.poll.getVote({
  "pollId": "",
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* pollId (string) **required**
* userId (string) **required**

### poll.getVotes
Get Votes Action


```js
kaltura.poll.getVotes({
  "pollId": "",
  "answerIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* pollId (string) **required**
* answerIds (string) **required**

### poll.resetVotes
Get resetVotes Action


```js
kaltura.poll.resetVotes({
  "pollId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* pollId (string) **required**

### poll.vote
Vote Action


```js
kaltura.poll.vote({
  "pollId": "",
  "userId": "",
  "answerIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* pollId (string) **required**
* userId (string) **required**
* answerIds (string) **required**

### quiz.add
Allows to add a quiz to an entry


```js
kaltura.quiz.add({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* quiz[uiAttributes] (array)
* quiz[showResultOnAnswer] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showCorrectKeyOnAnswer] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[allowAnswerUpdate] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showCorrectAfterSubmission] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[allowDownload] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showGradeAfterSubmission] (integer) - Enum Type: `KalturaNullableBoolean`

### quiz.get
Allows to get a quiz


```js
kaltura.quiz.get({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### quiz.getUrl
sends a with an api request for pdf from quiz object


```js
kaltura.quiz.getUrl({
  "entryId": "",
  "quizOutputType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* quizOutputType (integer) **required** - Enum Type: `KalturaQuizOutputType`

### quiz.list
List quiz objects by filter and pager


```js
kaltura.quiz.list({}, context)
```


### quiz.serve
creates a pdf from quiz object

The Output type defines the file format in which the quiz will be generated

Currently only PDF files are supported


```js
kaltura.quiz.serve({
  "entryId": "",
  "quizOutputType": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* quizOutputType (integer) **required** - Enum Type: `KalturaQuizOutputType`

### quiz.update
Allows to update a quiz


```js
kaltura.quiz.update({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* quiz[uiAttributes] (array)
* quiz[showResultOnAnswer] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showCorrectKeyOnAnswer] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[allowAnswerUpdate] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showCorrectAfterSubmission] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[allowDownload] (integer) - Enum Type: `KalturaNullableBoolean`
* quiz[showGradeAfterSubmission] (integer) - Enum Type: `KalturaNullableBoolean`

### report.execute



```js
kaltura.report.execute({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### report.getBaseTotal
report getBaseTotal action allows to get a the total base for storage reports


```js
kaltura.report.getBaseTotal({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaReportType`
* reportInputFilter[fromDate] (integer) - Start date as Unix timestamp (In seconds)
* reportInputFilter[toDate] (integer) - End date as Unix timestamp (In seconds)
* reportInputFilter[fromDay] (string) - Start day as string (YYYYMMDD)
* reportInputFilter[toDay] (string) - End date as string (YYYYMMDD)
* reportInputFilter[keywords] (string) - Search keywords to filter objects
* reportInputFilter[searchInTags] (boolean) - Search keywords in onjects tags
* reportInputFilter[searchInAdminTags] (boolean) - Search keywords in onjects admin tags
* reportInputFilter[categories] (string) - Search onjects in specified categories
* reportInputFilter[timeZoneOffset] (integer) - Time zone offset in minutes
* reportInputFilter[interval] (string) - Enum Type: `KalturaReportInterval`
* reportInputFilter[objectType] (string)
* reportInputFilter[application] (string)
* reportInputFilter[userIds] (string)
* reportInputFilter[playbackContext] (string)
* reportInputFilter[ancestorPlaybackContext] (string)
* objectIds (string) - - one ID or more (separated by ',') of specific objects to query

### report.getCsv



```js
kaltura.report.getCsv({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### report.getCsvFromStringParams
Returns report CSV file executed by string params with the following convention: param1=value1;param2=value2


```js
kaltura.report.getCsvFromStringParams({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* params (string)

### report.getGraphs
report getGraphs action allows to get a graph data for a specific report.


```js
kaltura.report.getGraphs({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaReportType`
* reportInputFilter[fromDate] (integer) - Start date as Unix timestamp (In seconds)
* reportInputFilter[toDate] (integer) - End date as Unix timestamp (In seconds)
* reportInputFilter[fromDay] (string) - Start day as string (YYYYMMDD)
* reportInputFilter[toDay] (string) - End date as string (YYYYMMDD)
* reportInputFilter[keywords] (string) - Search keywords to filter objects
* reportInputFilter[searchInTags] (boolean) - Search keywords in onjects tags
* reportInputFilter[searchInAdminTags] (boolean) - Search keywords in onjects admin tags
* reportInputFilter[categories] (string) - Search onjects in specified categories
* reportInputFilter[timeZoneOffset] (integer) - Time zone offset in minutes
* reportInputFilter[interval] (string) - Enum Type: `KalturaReportInterval`
* reportInputFilter[objectType] (string)
* reportInputFilter[application] (string)
* reportInputFilter[userIds] (string)
* reportInputFilter[playbackContext] (string)
* reportInputFilter[ancestorPlaybackContext] (string)
* dimension (string)
* objectIds (string) - - one ID or more (separated by ',') of specific objects to query

### report.getTable
report getTable action allows to get a graph data for a specific report.


```js
kaltura.report.getTable({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaReportType`
* reportInputFilter[fromDate] (integer) - Start date as Unix timestamp (In seconds)
* reportInputFilter[toDate] (integer) - End date as Unix timestamp (In seconds)
* reportInputFilter[fromDay] (string) - Start day as string (YYYYMMDD)
* reportInputFilter[toDay] (string) - End date as string (YYYYMMDD)
* reportInputFilter[keywords] (string) - Search keywords to filter objects
* reportInputFilter[searchInTags] (boolean) - Search keywords in onjects tags
* reportInputFilter[searchInAdminTags] (boolean) - Search keywords in onjects admin tags
* reportInputFilter[categories] (string) - Search onjects in specified categories
* reportInputFilter[timeZoneOffset] (integer) - Time zone offset in minutes
* reportInputFilter[interval] (string) - Enum Type: `KalturaReportInterval`
* reportInputFilter[objectType] (string)
* reportInputFilter[application] (string)
* reportInputFilter[userIds] (string)
* reportInputFilter[playbackContext] (string)
* reportInputFilter[ancestorPlaybackContext] (string)
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).
* order (string)
* objectIds (string) - - one ID or more (separated by ',') of specific objects to query

### report.getTotal
report getTotal action allows to get a graph data for a specific report.


```js
kaltura.report.getTotal({
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportType (string) **required** - Enum Type: `KalturaReportType`
* reportInputFilter[fromDate] (integer) - Start date as Unix timestamp (In seconds)
* reportInputFilter[toDate] (integer) - End date as Unix timestamp (In seconds)
* reportInputFilter[fromDay] (string) - Start day as string (YYYYMMDD)
* reportInputFilter[toDay] (string) - End date as string (YYYYMMDD)
* reportInputFilter[keywords] (string) - Search keywords to filter objects
* reportInputFilter[searchInTags] (boolean) - Search keywords in onjects tags
* reportInputFilter[searchInAdminTags] (boolean) - Search keywords in onjects admin tags
* reportInputFilter[categories] (string) - Search onjects in specified categories
* reportInputFilter[timeZoneOffset] (integer) - Time zone offset in minutes
* reportInputFilter[interval] (string) - Enum Type: `KalturaReportInterval`
* reportInputFilter[objectType] (string)
* reportInputFilter[application] (string)
* reportInputFilter[userIds] (string)
* reportInputFilter[playbackContext] (string)
* reportInputFilter[ancestorPlaybackContext] (string)
* objectIds (string) - - one ID or more (separated by ',') of specific objects to query

### report.getUrlForReportAsCsv
will create a Csv file for the given report and return the URL to access it


```js
kaltura.report.getUrlForReportAsCsv({
  "reportTitle": "",
  "reportText": "",
  "headers": "",
  "reportType": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* reportTitle (string) **required** - The title of the report to display at top of CSV
* reportText (string) **required** - The text of the filter of the report
* headers (string) **required** - The headers of the columns - a map between the enumerations on the server side and the their display text
* reportType (string) **required** - Enum Type: `KalturaReportType`
* reportInputFilter[fromDate] (integer) - Start date as Unix timestamp (In seconds)
* reportInputFilter[toDate] (integer) - End date as Unix timestamp (In seconds)
* reportInputFilter[fromDay] (string) - Start day as string (YYYYMMDD)
* reportInputFilter[toDay] (string) - End date as string (YYYYMMDD)
* reportInputFilter[keywords] (string) - Search keywords to filter objects
* reportInputFilter[searchInTags] (boolean) - Search keywords in onjects tags
* reportInputFilter[searchInAdminTags] (boolean) - Search keywords in onjects admin tags
* reportInputFilter[categories] (string) - Search onjects in specified categories
* reportInputFilter[timeZoneOffset] (integer) - Time zone offset in minutes
* reportInputFilter[interval] (string) - Enum Type: `KalturaReportInterval`
* reportInputFilter[objectType] (string)
* reportInputFilter[application] (string)
* reportInputFilter[userIds] (string)
* reportInputFilter[playbackContext] (string)
* reportInputFilter[ancestorPlaybackContext] (string)
* dimension (string)
* pager[pageSize] (integer) - The number of objects to retrieve. (Default is 30, maximum page size is 500).
* pager[pageIndex] (integer) - The page number for which {pageSize} of objects should be retrieved (Default is 1).
* order (string)
* objectIds (string) - - one ID or more (separated by ',') of specific objects to query

### report.serve
Will serve a requested report


```js
kaltura.report.serve({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required** - - the requested id

### responseProfile.add
Add new response profile


```js
kaltura.responseProfile.add({}, context)
```


### responseProfile.clone
Clone an existing response profile


```js
kaltura.responseProfile.clone({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* profile[name] (string) - Friendly name
* profile[type] (integer) - Enum Type: `KalturaResponseProfileType`
* profile[fields] (string) - Comma separated fields list to be included or excluded
* profile[filter][orderBy] (string)
* profile[filter][advancedSearch][objectType] (string)
* profile[filter][advancedSearch][value] (string)
* profile[filter][advancedSearch][categoriesMatchOr] (string)
* profile[filter][advancedSearch][categoryEntryStatusIn] (string)
* profile[filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* profile[filter][advancedSearch][categoryIdEqual] (integer)
* profile[filter][advancedSearch][memberIdEq] (string)
* profile[filter][advancedSearch][memberIdIn] (string)
* profile[filter][advancedSearch][memberPermissionsMatchOr] (string)
* profile[filter][advancedSearch][memberPermissionsMatchAnd] (string)
* profile[filter][advancedSearch][noDistributionProfiles] (boolean)
* profile[filter][advancedSearch][distributionProfileId] (integer)
* profile[filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* profile[filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* profile[filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* profile[filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* profile[filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* profile[filter][advancedSearch][contentLike] (string)
* profile[filter][advancedSearch][contentMultiLikeOr] (string)
* profile[filter][advancedSearch][contentMultiLikeAnd] (string)
* profile[filter][advancedSearch][cuePointsFreeText] (string)
* profile[filter][advancedSearch][cuePointTypeIn] (string)
* profile[filter][advancedSearch][cuePointSubTypeEqual] (integer)
* profile[filter][advancedSearch][watermarkId] (integer)
* profile[filter][advancedSearch][indexIdGreaterThan] (integer)
* profile[filter][advancedSearch][depthGreaterThanEqual] (integer)
* profile[filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][advancedSearch][field] (string)
* profile[filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* profile[filter][advancedSearch][items] (array)
* profile[filter][advancedSearch][idEqual] (string)
* profile[filter][advancedSearch][idIn] (string)
* profile[filter][advancedSearch][userIdEqual] (string)
* profile[filter][advancedSearch][userIdIn] (string)
* profile[filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* profile[filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* profile[filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* profile[filter][advancedSearch][extendedStatusIn] (string)
* profile[filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* profile[filter][advancedSearch][not] (boolean)
* profile[filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* profile[filter][advancedSearch][metadataProfileId] (integer)
* profile[filter][objectType] (string)
* profile[filter][idEqual] (string)
* profile[filter][idIn] (string)
* profile[filter][entryIdEqual] (string)
* profile[filter][entryIdIn] (string)
* profile[filter][partnerIdEqual] (integer)
* profile[filter][partnerIdIn] (string)
* profile[filter][sizeGreaterThanOrEqual] (integer)
* profile[filter][sizeLessThanOrEqual] (integer)
* profile[filter][tagsLike] (string)
* profile[filter][tagsMultiLikeOr] (string)
* profile[filter][tagsMultiLikeAnd] (string)
* profile[filter][createdAtGreaterThanOrEqual] (integer)
* profile[filter][createdAtLessThanOrEqual] (integer)
* profile[filter][updatedAtGreaterThanOrEqual] (integer)
* profile[filter][updatedAtLessThanOrEqual] (integer)
* profile[filter][deletedAtGreaterThanOrEqual] (integer)
* profile[filter][deletedAtLessThanOrEqual] (integer)
* profile[filter][idNotIn] (string)
* profile[filter][nameLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry names (no wildcards, spaces are treated as part of the string).
* profile[filter][nameMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* profile[filter][nameMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* profile[filter][nameEqual] (string) - This filter should be in use for retrieving entries with a specific name.
* profile[filter][userIdEqual] (string) - This filter parameter should be in use for retrieving only entries, uploaded by/assigned to a specific user (identified by user Id).
* profile[filter][userIdIn] (string)
* profile[filter][userIdNotIn] (string)
* profile[filter][creatorIdEqual] (string)
* profile[filter][adminTagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags set by an ADMIN user (no wildcards, spaces are treated as part of the string).
* profile[filter][adminTagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* profile[filter][adminTagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* profile[filter][categoriesMatchAnd] (string)
* profile[filter][categoriesMatchOr] (string) - All entries within these categories or their child categories.
* profile[filter][categoriesNotContains] (string)
* profile[filter][categoriesIdsMatchAnd] (string)
* profile[filter][categoriesIdsMatchOr] (string) - All entries of the categories, excluding their child categories.
* profile[filter][categoriesIdsNotContains] (string)
* profile[filter][categoriesIdsEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][statusEqual] (string) - Enum Type: `KalturaEntryStatus`
* profile[filter][statusNotEqual] (string) - Enum Type: `KalturaEntryStatus`
* profile[filter][statusIn] (string) - This filter should be in use for retrieving only entries, at few specific {
* profile[filter][statusNotIn] (string) - This filter should be in use for retrieving only entries, not at few specific {
* profile[filter][moderationStatusEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* profile[filter][moderationStatusNotEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* profile[filter][moderationStatusIn] (string)
* profile[filter][moderationStatusNotIn] (string)
* profile[filter][typeEqual] (string) - Enum Type: `KalturaEntryType`
* profile[filter][typeIn] (string) - This filter should be in use for retrieving entries of few {
* profile[filter][totalRankLessThanOrEqual] (integer)
* profile[filter][totalRankGreaterThanOrEqual] (integer)
* profile[filter][groupIdEqual] (integer)
* profile[filter][searchTextMatchAnd] (string) - This filter should be in use for retrieving specific entries while search match the input string within all of the following metadata attributes: name, description, tags, adminTags.
* profile[filter][searchTextMatchOr] (string) - This filter should be in use for retrieving specific entries while search match the input string within at least one of the following metadata attributes: name, description, tags, adminTags.
* profile[filter][accessControlIdEqual] (integer)
* profile[filter][accessControlIdIn] (string)
* profile[filter][startDateGreaterThanOrEqual] (integer)
* profile[filter][startDateLessThanOrEqual] (integer)
* profile[filter][startDateGreaterThanOrEqualOrNull] (integer)
* profile[filter][startDateLessThanOrEqualOrNull] (integer)
* profile[filter][endDateGreaterThanOrEqual] (integer)
* profile[filter][endDateLessThanOrEqual] (integer)
* profile[filter][endDateGreaterThanOrEqualOrNull] (integer)
* profile[filter][endDateLessThanOrEqualOrNull] (integer)
* profile[filter][referenceIdEqual] (string)
* profile[filter][referenceIdIn] (string)
* profile[filter][replacingEntryIdEqual] (string)
* profile[filter][replacingEntryIdIn] (string)
* profile[filter][replacedEntryIdEqual] (string)
* profile[filter][replacedEntryIdIn] (string)
* profile[filter][replacementStatusEqual] (string) - Enum Type: `KalturaEntryReplacementStatus`
* profile[filter][replacementStatusIn] (string)
* profile[filter][partnerSortValueGreaterThanOrEqual] (integer)
* profile[filter][partnerSortValueLessThanOrEqual] (integer)
* profile[filter][rootEntryIdEqual] (string)
* profile[filter][rootEntryIdIn] (string)
* profile[filter][parentEntryIdEqual] (string)
* profile[filter][entitledUsersEditMatchAnd] (string)
* profile[filter][entitledUsersEditMatchOr] (string)
* profile[filter][entitledUsersPublishMatchAnd] (string)
* profile[filter][entitledUsersPublishMatchOr] (string)
* profile[filter][tagsNameMultiLikeOr] (string)
* profile[filter][tagsAdminTagsMultiLikeOr] (string)
* profile[filter][tagsAdminTagsNameMultiLikeOr] (string)
* profile[filter][tagsNameMultiLikeAnd] (string)
* profile[filter][tagsAdminTagsMultiLikeAnd] (string)
* profile[filter][tagsAdminTagsNameMultiLikeAnd] (string)
* profile[filter][categoryIdEqual] (integer)
* profile[filter][categoryIdIn] (string)
* profile[filter][permissionLevelEqual] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* profile[filter][permissionLevelIn] (string)
* profile[filter][updateMethodEqual] (integer) - Enum Type: `KalturaUpdateMethodType`
* profile[filter][updateMethodIn] (string)
* profile[filter][categoryFullIdsStartsWith] (string)
* profile[filter][categoryFullIdsEqual] (string)
* profile[filter][permissionNamesMatchAnd] (string)
* profile[filter][permissionNamesMatchOr] (string)
* profile[filter][permissionNamesNotContains] (string)
* profile[filter][screenNameLike] (string)
* profile[filter][screenNameStartsWith] (string)
* profile[filter][emailLike] (string)
* profile[filter][emailStartsWith] (string)
* profile[filter][firstNameStartsWith] (string)
* profile[filter][lastNameStartsWith] (string)
* profile[filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][systemNameEqual] (string)
* profile[filter][systemNameIn] (string)
* profile[filter][isSystemDefaultEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][tagsEqual] (string)
* profile[filter][parsedAtGreaterThanOrEqual] (integer)
* profile[filter][parsedAtLessThanOrEqual] (integer)
* profile[filter][auditObjectTypeEqual] (string) - Enum Type: `KalturaAuditTrailObjectType`
* profile[filter][auditObjectTypeIn] (string)
* profile[filter][objectIdEqual] (string)
* profile[filter][objectIdIn] (string)
* profile[filter][relatedObjectIdEqual] (string)
* profile[filter][relatedObjectIdIn] (string)
* profile[filter][relatedObjectTypeEqual] (string) - Enum Type: `KalturaAuditTrailObjectType`
* profile[filter][relatedObjectTypeIn] (string)
* profile[filter][masterPartnerIdEqual] (integer)
* profile[filter][masterPartnerIdIn] (string)
* profile[filter][requestIdEqual] (string)
* profile[filter][requestIdIn] (string)
* profile[filter][actionEqual] (string) - Enum Type: `KalturaAuditTrailAction`
* profile[filter][actionIn] (string)
* profile[filter][ksEqual] (string)
* profile[filter][contextEqual] (integer) - Enum Type: `KalturaAuditTrailContext`
* profile[filter][contextIn] (string)
* profile[filter][entryPointEqual] (string)
* profile[filter][entryPointIn] (string)
* profile[filter][serverNameEqual] (string)
* profile[filter][serverNameIn] (string)
* profile[filter][ipAddressEqual] (string)
* profile[filter][ipAddressIn] (string)
* profile[filter][clientTagEqual] (string)
* profile[filter][parentIdEqual] (integer)
* profile[filter][parentIdIn] (string)
* profile[filter][depthEqual] (integer)
* profile[filter][fullNameEqual] (string)
* profile[filter][fullNameStartsWith] (string)
* profile[filter][fullNameIn] (string)
* profile[filter][fullIdsEqual] (string)
* profile[filter][fullIdsStartsWith] (string)
* profile[filter][fullIdsMatchOr] (string)
* profile[filter][appearInListEqual] (integer) - Enum Type: `KalturaAppearInListType`
* profile[filter][privacyEqual] (integer) - Enum Type: `KalturaPrivacyType`
* profile[filter][privacyIn] (string)
* profile[filter][inheritanceTypeEqual] (integer) - Enum Type: `KalturaInheritanceType`
* profile[filter][inheritanceTypeIn] (string)
* profile[filter][referenceIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][contributionPolicyEqual] (integer) - Enum Type: `KalturaContributionPolicyType`
* profile[filter][membersCountGreaterThanOrEqual] (integer)
* profile[filter][membersCountLessThanOrEqual] (integer)
* profile[filter][pendingMembersCountGreaterThanOrEqual] (integer)
* profile[filter][pendingMembersCountLessThanOrEqual] (integer)
* profile[filter][privacyContextEqual] (string)
* profile[filter][inheritedParentIdEqual] (integer)
* profile[filter][inheritedParentIdIn] (string)
* profile[filter][aggregationCategoriesMultiLikeOr] (string)
* profile[filter][aggregationCategoriesMultiLikeAnd] (string)
* profile[filter][creatorUserIdEqual] (string)
* profile[filter][creatorUserIdIn] (string)
* profile[filter][conversionProfileIdEqual] (integer)
* profile[filter][conversionProfileIdIn] (string)
* profile[filter][assetParamsIdEqual] (integer)
* profile[filter][assetParamsIdIn] (string)
* profile[filter][readyBehaviorEqual] (integer) - Enum Type: `KalturaFlavorReadyBehaviorType`
* profile[filter][readyBehaviorIn] (string)
* profile[filter][originEqual] (integer) - Enum Type: `KalturaAssetParamsOrigin`
* profile[filter][originIn] (string)
* profile[filter][defaultEntryIdEqual] (string)
* profile[filter][defaultEntryIdIn] (string)
* profile[filter][cuePointTypeEqual] (string) - Enum Type: `KalturaCuePointType`
* profile[filter][cuePointTypeIn] (string)
* profile[filter][triggeredAtGreaterThanOrEqual] (integer)
* profile[filter][triggeredAtLessThanOrEqual] (integer)
* profile[filter][startTimeGreaterThanOrEqual] (integer)
* profile[filter][startTimeLessThanOrEqual] (integer)
* profile[filter][partnerSortValueEqual] (integer)
* profile[filter][partnerSortValueIn] (string)
* profile[filter][forceStopEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][submittedAtGreaterThanOrEqual] (integer)
* profile[filter][submittedAtLessThanOrEqual] (integer)
* profile[filter][distributionProfileIdEqual] (integer)
* profile[filter][distributionProfileIdIn] (string)
* profile[filter][dirtyStatusEqual] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* profile[filter][dirtyStatusIn] (string)
* profile[filter][sunriseGreaterThanOrEqual] (integer)
* profile[filter][sunriseLessThanOrEqual] (integer)
* profile[filter][sunsetGreaterThanOrEqual] (integer)
* profile[filter][sunsetLessThanOrEqual] (integer)
* profile[filter][fileAssetObjectTypeEqual] (string) - Enum Type: `KalturaFileAssetObjectType`
* profile[filter][groupIdIn] (string)
* profile[filter][channelIdEqual] (string)
* profile[filter][channelIdIn] (string)
* profile[filter][metadataProfileIdEqual] (integer)
* profile[filter][metadataProfileIdIn] (string)
* profile[filter][metadataProfileVersionEqual] (integer)
* profile[filter][metadataProfileVersionGreaterThanOrEqual] (integer)
* profile[filter][metadataProfileVersionLessThanOrEqual] (integer)
* profile[filter][metadataObjectTypeEqual] (string) - Enum Type: `KalturaMetadataObjectType`
* profile[filter][versionEqual] (integer)
* profile[filter][versionGreaterThanOrEqual] (integer)
* profile[filter][versionLessThanOrEqual] (integer)
* profile[filter][nameIn] (string)
* profile[filter][friendlyNameLike] (string)
* profile[filter][descriptionLike] (string)
* profile[filter][dependsOnPermissionNamesMultiLikeOr] (string)
* profile[filter][dependsOnPermissionNamesMultiLikeAnd] (string)
* profile[filter][parentIdNotIn] (string)
* profile[filter][ownerIdEqual] (string)
* profile[filter][ownerIdIn] (string)
* profile[filter][priorityEqual] (integer)
* profile[filter][priorityIn] (string)
* profile[filter][priorityGreaterThanOrEqual] (integer)
* profile[filter][priorityLessThanOrEqual] (integer)
* profile[filter][recurrenceTypeEqual] (integer) - Enum Type: `KalturaScheduleEventRecurrenceType`
* profile[filter][recurrenceTypeIn] (string)
* profile[filter][eventIdEqual] (integer)
* profile[filter][eventIdIn] (string)
* profile[filter][resourceIdEqual] (integer)
* profile[filter][resourceIdIn] (string)
* profile[filter][entryIdNotIn] (string)
* profile[filter][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* profile[filter][extendedStatusIn] (string)
* profile[filter][extendedStatusNotIn] (string)
* profile[filter][loginEmailEqual] (string)
* profile[filter][formatEqual] (string) - Enum Type: `KalturaAttachmentType`
* profile[filter][formatIn] (string)
* profile[filter][captionParamsIdEqual] (integer)
* profile[filter][captionParamsIdIn] (string)
* profile[filter][flavorParamsIdEqual] (integer)
* profile[filter][flavorParamsIdIn] (string)
* profile[filter][thumbParamsIdEqual] (integer)
* profile[filter][thumbParamsIdIn] (string)
* profile[filter][contentLike] (string)
* profile[filter][contentMultiLikeOr] (string)
* profile[filter][contentMultiLikeAnd] (string)
* profile[filter][partnerDescriptionLike] (string)
* profile[filter][partnerDescriptionMultiLikeOr] (string)
* profile[filter][partnerDescriptionMultiLikeAnd] (string)
* profile[filter][languageEqual] (string) - Enum Type: `KalturaLanguage`
* profile[filter][languageIn] (string)
* profile[filter][labelEqual] (string)
* profile[filter][labelIn] (string)
* profile[filter][endTimeGreaterThanOrEqual] (integer)
* profile[filter][endTimeLessThanOrEqual] (integer)
* profile[filter][freeText] (string)
* profile[filter][isRoot] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][categoriesFullNameIn] (string)
* profile[filter][categoryAncestorIdIn] (string) - All entries within this categoy or in child categories
* profile[filter][redirectFromEntryId] (string) - The id of the original entry
* profile[filter][lastPlayedAtGreaterThanOrEqual] (integer)
* profile[filter][lastPlayedAtLessThanOrEqual] (integer)
* profile[filter][durationLessThan] (integer)
* profile[filter][durationGreaterThan] (integer)
* profile[filter][durationLessThanOrEqual] (integer)
* profile[filter][durationGreaterThanOrEqual] (integer)
* profile[filter][durationTypeMatchOr] (string)
* profile[filter][documentTypeEqual] (integer) - Enum Type: `KalturaDocumentType`
* profile[filter][documentTypeIn] (string)
* profile[filter][assetParamsIdsMatchOr] (string)
* profile[filter][assetParamsIdsMatchAnd] (string)
* profile[filter][mediaTypeEqual] (integer) - Enum Type: `KalturaMediaType`
* profile[filter][mediaTypeIn] (string)
* profile[filter][sourceTypeEqual] (string) - Enum Type: `KalturaSourceType`
* profile[filter][sourceTypeNotEqual] (string) - Enum Type: `KalturaSourceType`
* profile[filter][sourceTypeIn] (string)
* profile[filter][sourceTypeNotIn] (string)
* profile[filter][mediaDateGreaterThanOrEqual] (integer)
* profile[filter][mediaDateLessThanOrEqual] (integer)
* profile[filter][flavorParamsIdsMatchOr] (string)
* profile[filter][flavorParamsIdsMatchAnd] (string)
* profile[filter][limit] (integer)
* profile[filter][externalSourceTypeEqual] (string) - Enum Type: `KalturaExternalMediaSourceType`
* profile[filter][externalSourceTypeIn] (string)
* profile[filter][isLive] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][isRecordedEntryIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][hasMediaServerHostname] (string)
* profile[filter][categoryDirectMembers] (boolean) - Return the list of categoryUser that are not inherited from parent category - only the direct categoryUsers.
* profile[filter][relatedGroupsByUserId] (string) - Return a list of categoryUser that related to the userId in this field by groups
* profile[filter][idOrScreenNameStartsWith] (string)
* profile[filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][roleIdEqual] (string)
* profile[filter][roleIdsEqual] (string)
* profile[filter][roleIdsIn] (string)
* profile[filter][firstNameOrLastNameStartsWith] (string)
* profile[filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* profile[filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* profile[filter][flavorParamsVersionEqual] (string)
* profile[filter][flavorAssetIdEqual] (string)
* profile[filter][flavorAssetVersionEqual] (string)
* profile[filter][thumbParamsVersionEqual] (string)
* profile[filter][thumbAssetIdEqual] (string)
* profile[filter][thumbAssetVersionEqual] (string)
* profile[filter][membersIn] (string)
* profile[filter][nameOrReferenceIdStartsWith] (string)
* profile[filter][managerEqual] (string)
* profile[filter][memberEqual] (string)
* profile[filter][fullNameStartsWithIn] (string)
* profile[filter][ancestorIdIn] (string) - not includes the category itself (only sub categories)
* profile[filter][idOrInheritedParentIdIn] (string)
* profile[filter][conversionProfileIdFilter][orderBy] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][objectType] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][value] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][categoriesMatchOr] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][categoryEntryStatusIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* profile[filter][conversionProfileIdFilter][advancedSearch][categoryIdEqual] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][memberIdEq] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][memberIdIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][memberPermissionsMatchOr] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][memberPermissionsMatchAnd] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][noDistributionProfiles] (boolean)
* profile[filter][conversionProfileIdFilter][advancedSearch][distributionProfileId] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* profile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* profile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* profile[filter][conversionProfileIdFilter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* profile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* profile[filter][conversionProfileIdFilter][advancedSearch][contentLike] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][contentMultiLikeOr] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][contentMultiLikeAnd] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][cuePointsFreeText] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][cuePointTypeIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][cuePointSubTypeEqual] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][watermarkId] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][indexIdGreaterThan] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][depthGreaterThanEqual] (integer)
* profile[filter][conversionProfileIdFilter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][conversionProfileIdFilter][advancedSearch][field] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* profile[filter][conversionProfileIdFilter][advancedSearch][items] (array)
* profile[filter][conversionProfileIdFilter][advancedSearch][idEqual] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][idIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][userIdEqual] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][userIdIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][updatedAtLessThanOrEqual] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* profile[filter][conversionProfileIdFilter][advancedSearch][extendedStatusIn] (string)
* profile[filter][conversionProfileIdFilter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* profile[filter][conversionProfileIdFilter][advancedSearch][not] (boolean)
* profile[filter][conversionProfileIdFilter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* profile[filter][conversionProfileIdFilter][advancedSearch][metadataProfileId] (integer)
* profile[filter][conversionProfileIdFilter][idEqual] (integer)
* profile[filter][conversionProfileIdFilter][idIn] (string)
* profile[filter][conversionProfileIdFilter][statusEqual] (string) - Enum Type: `KalturaConversionProfileStatus`
* profile[filter][conversionProfileIdFilter][statusIn] (string)
* profile[filter][conversionProfileIdFilter][typeEqual] (string) - Enum Type: `KalturaConversionProfileType`
* profile[filter][conversionProfileIdFilter][typeIn] (string)
* profile[filter][conversionProfileIdFilter][nameEqual] (string)
* profile[filter][conversionProfileIdFilter][systemNameEqual] (string)
* profile[filter][conversionProfileIdFilter][systemNameIn] (string)
* profile[filter][conversionProfileIdFilter][tagsMultiLikeOr] (string)
* profile[filter][conversionProfileIdFilter][tagsMultiLikeAnd] (string)
* profile[filter][conversionProfileIdFilter][defaultEntryIdEqual] (string)
* profile[filter][conversionProfileIdFilter][defaultEntryIdIn] (string)
* profile[filter][userIdEqualCurrent] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][userIdCurrent] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][protocolTypeEqual] (string) - Enum Type: `KalturaAdProtocolType`
* profile[filter][protocolTypeIn] (string)
* profile[filter][titleLike] (string)
* profile[filter][titleMultiLikeOr] (string)
* profile[filter][titleMultiLikeAnd] (string)
* profile[filter][textLike] (string)
* profile[filter][textMultiLikeOr] (string)
* profile[filter][textMultiLikeAnd] (string)
* profile[filter][isPublicEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][quizUserEntryIdEqual] (string)
* profile[filter][quizUserEntryIdIn] (string)
* profile[filter][codeLike] (string)
* profile[filter][codeMultiLikeOr] (string)
* profile[filter][codeMultiLikeAnd] (string)
* profile[filter][codeEqual] (string)
* profile[filter][codeIn] (string)
* profile[filter][descriptionMultiLikeOr] (string)
* profile[filter][descriptionMultiLikeAnd] (string)
* profile[filter][eventTypeEqual] (string) - Enum Type: `KalturaEventType`
* profile[filter][eventTypeIn] (string)
* profile[filter][questionLike] (string)
* profile[filter][questionMultiLikeOr] (string)
* profile[filter][questionMultiLikeAnd] (string)
* profile[filter][subTypeEqual] (integer) - Enum Type: `KalturaThumbCuePointSubType`
* profile[filter][subTypeIn] (string)
* profile[filter][resourceIdsLike] (string)
* profile[filter][resourceIdsMultiLikeOr] (string)
* profile[filter][resourceIdsMultiLikeAnd] (string)
* profile[filter][parentResourceIdsLike] (string)
* profile[filter][parentResourceIdsMultiLikeOr] (string)
* profile[filter][parentResourceIdsMultiLikeAnd] (string)
* profile[filter][templateEntryCategoriesIdsMultiLikeAnd] (string)
* profile[filter][templateEntryCategoriesIdsMultiLikeOr] (string)
* profile[filter][resourceSystemNamesMultiLikeOr] (string)
* profile[filter][templateEntryCategoriesIdsLike] (string)
* profile[filter][resourceSystemNamesMultiLikeAnd] (string)
* profile[filter][resourceSystemNamesLike] (string)
* profile[filter][templateEntryIdEqual] (string)
* profile[filter][entryIdsLike] (string)
* profile[filter][entryIdsMultiLikeOr] (string)
* profile[filter][entryIdsMultiLikeAnd] (string)
* profile[filter][categoryIdsLike] (string)
* profile[filter][categoryIdsMultiLikeOr] (string)
* profile[filter][categoryIdsMultiLikeAnd] (string)
* profile[filter][parentCategoryIdsLike] (string)
* profile[filter][parentCategoryIdsMultiLikeOr] (string)
* profile[filter][parentCategoryIdsMultiLikeAnd] (string)
* profile[filter][eventIdOrItsParentIdEqual] (integer) - Find event-resource objects that associated with the event, if none found, find by its parent event
* profile[filter][isAnonymous] (integer) - Enum Type: `KalturaNullableBoolean`
* profile[filter][privacyContextIn] (string)
* profile[systemName] (string) - Unique system name

### responseProfile.delete
Delete response profile by id


```js
kaltura.responseProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### responseProfile.get
Get response profile by id


```js
kaltura.responseProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### responseProfile.list
List response profiles by filter and pager


```js
kaltura.responseProfile.list({}, context)
```


### responseProfile.recalculate
Recalculate response profile cached objects


```js
kaltura.responseProfile.recalculate({}, context)
```


### responseProfile.update
Update response profile by id


```js
kaltura.responseProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* updateResponseProfile[name] (string) - Friendly name
* updateResponseProfile[type] (integer) - Enum Type: `KalturaResponseProfileType`
* updateResponseProfile[fields] (string) - Comma separated fields list to be included or excluded
* updateResponseProfile[filter][orderBy] (string)
* updateResponseProfile[filter][advancedSearch][objectType] (string)
* updateResponseProfile[filter][advancedSearch][value] (string)
* updateResponseProfile[filter][advancedSearch][categoriesMatchOr] (string)
* updateResponseProfile[filter][advancedSearch][categoryEntryStatusIn] (string)
* updateResponseProfile[filter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* updateResponseProfile[filter][advancedSearch][categoryIdEqual] (integer)
* updateResponseProfile[filter][advancedSearch][memberIdEq] (string)
* updateResponseProfile[filter][advancedSearch][memberIdIn] (string)
* updateResponseProfile[filter][advancedSearch][memberPermissionsMatchOr] (string)
* updateResponseProfile[filter][advancedSearch][memberPermissionsMatchAnd] (string)
* updateResponseProfile[filter][advancedSearch][noDistributionProfiles] (boolean)
* updateResponseProfile[filter][advancedSearch][distributionProfileId] (integer)
* updateResponseProfile[filter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* updateResponseProfile[filter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* updateResponseProfile[filter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* updateResponseProfile[filter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* updateResponseProfile[filter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* updateResponseProfile[filter][advancedSearch][contentLike] (string)
* updateResponseProfile[filter][advancedSearch][contentMultiLikeOr] (string)
* updateResponseProfile[filter][advancedSearch][contentMultiLikeAnd] (string)
* updateResponseProfile[filter][advancedSearch][cuePointsFreeText] (string)
* updateResponseProfile[filter][advancedSearch][cuePointTypeIn] (string)
* updateResponseProfile[filter][advancedSearch][cuePointSubTypeEqual] (integer)
* updateResponseProfile[filter][advancedSearch][watermarkId] (integer)
* updateResponseProfile[filter][advancedSearch][indexIdGreaterThan] (integer)
* updateResponseProfile[filter][advancedSearch][depthGreaterThanEqual] (integer)
* updateResponseProfile[filter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][advancedSearch][field] (string)
* updateResponseProfile[filter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* updateResponseProfile[filter][advancedSearch][items] (array)
* updateResponseProfile[filter][advancedSearch][idEqual] (string)
* updateResponseProfile[filter][advancedSearch][idIn] (string)
* updateResponseProfile[filter][advancedSearch][userIdEqual] (string)
* updateResponseProfile[filter][advancedSearch][userIdIn] (string)
* updateResponseProfile[filter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* updateResponseProfile[filter][advancedSearch][updatedAtLessThanOrEqual] (string)
* updateResponseProfile[filter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* updateResponseProfile[filter][advancedSearch][extendedStatusIn] (string)
* updateResponseProfile[filter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* updateResponseProfile[filter][advancedSearch][not] (boolean)
* updateResponseProfile[filter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* updateResponseProfile[filter][advancedSearch][metadataProfileId] (integer)
* updateResponseProfile[filter][objectType] (string)
* updateResponseProfile[filter][idEqual] (string)
* updateResponseProfile[filter][idIn] (string)
* updateResponseProfile[filter][entryIdEqual] (string)
* updateResponseProfile[filter][entryIdIn] (string)
* updateResponseProfile[filter][partnerIdEqual] (integer)
* updateResponseProfile[filter][partnerIdIn] (string)
* updateResponseProfile[filter][sizeGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][sizeLessThanOrEqual] (integer)
* updateResponseProfile[filter][tagsLike] (string)
* updateResponseProfile[filter][tagsMultiLikeOr] (string)
* updateResponseProfile[filter][tagsMultiLikeAnd] (string)
* updateResponseProfile[filter][createdAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][createdAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][updatedAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][updatedAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][deletedAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][deletedAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][idNotIn] (string)
* updateResponseProfile[filter][nameLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry names (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][nameMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][nameMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][nameEqual] (string) - This filter should be in use for retrieving entries with a specific name.
* updateResponseProfile[filter][userIdEqual] (string) - This filter parameter should be in use for retrieving only entries, uploaded by/assigned to a specific user (identified by user Id).
* updateResponseProfile[filter][userIdIn] (string)
* updateResponseProfile[filter][userIdNotIn] (string)
* updateResponseProfile[filter][creatorIdEqual] (string)
* updateResponseProfile[filter][adminTagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags set by an ADMIN user (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][adminTagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][adminTagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* updateResponseProfile[filter][categoriesMatchAnd] (string)
* updateResponseProfile[filter][categoriesMatchOr] (string) - All entries within these categories or their child categories.
* updateResponseProfile[filter][categoriesNotContains] (string)
* updateResponseProfile[filter][categoriesIdsMatchAnd] (string)
* updateResponseProfile[filter][categoriesIdsMatchOr] (string) - All entries of the categories, excluding their child categories.
* updateResponseProfile[filter][categoriesIdsNotContains] (string)
* updateResponseProfile[filter][categoriesIdsEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][statusEqual] (string) - Enum Type: `KalturaEntryStatus`
* updateResponseProfile[filter][statusNotEqual] (string) - Enum Type: `KalturaEntryStatus`
* updateResponseProfile[filter][statusIn] (string) - This filter should be in use for retrieving only entries, at few specific {
* updateResponseProfile[filter][statusNotIn] (string) - This filter should be in use for retrieving only entries, not at few specific {
* updateResponseProfile[filter][moderationStatusEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* updateResponseProfile[filter][moderationStatusNotEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* updateResponseProfile[filter][moderationStatusIn] (string)
* updateResponseProfile[filter][moderationStatusNotIn] (string)
* updateResponseProfile[filter][typeEqual] (string) - Enum Type: `KalturaEntryType`
* updateResponseProfile[filter][typeIn] (string) - This filter should be in use for retrieving entries of few {
* updateResponseProfile[filter][totalRankLessThanOrEqual] (integer)
* updateResponseProfile[filter][totalRankGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][groupIdEqual] (integer)
* updateResponseProfile[filter][searchTextMatchAnd] (string) - This filter should be in use for retrieving specific entries while search match the input string within all of the following metadata attributes: name, description, tags, adminTags.
* updateResponseProfile[filter][searchTextMatchOr] (string) - This filter should be in use for retrieving specific entries while search match the input string within at least one of the following metadata attributes: name, description, tags, adminTags.
* updateResponseProfile[filter][accessControlIdEqual] (integer)
* updateResponseProfile[filter][accessControlIdIn] (string)
* updateResponseProfile[filter][startDateGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][startDateLessThanOrEqual] (integer)
* updateResponseProfile[filter][startDateGreaterThanOrEqualOrNull] (integer)
* updateResponseProfile[filter][startDateLessThanOrEqualOrNull] (integer)
* updateResponseProfile[filter][endDateGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][endDateLessThanOrEqual] (integer)
* updateResponseProfile[filter][endDateGreaterThanOrEqualOrNull] (integer)
* updateResponseProfile[filter][endDateLessThanOrEqualOrNull] (integer)
* updateResponseProfile[filter][referenceIdEqual] (string)
* updateResponseProfile[filter][referenceIdIn] (string)
* updateResponseProfile[filter][replacingEntryIdEqual] (string)
* updateResponseProfile[filter][replacingEntryIdIn] (string)
* updateResponseProfile[filter][replacedEntryIdEqual] (string)
* updateResponseProfile[filter][replacedEntryIdIn] (string)
* updateResponseProfile[filter][replacementStatusEqual] (string) - Enum Type: `KalturaEntryReplacementStatus`
* updateResponseProfile[filter][replacementStatusIn] (string)
* updateResponseProfile[filter][partnerSortValueGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][partnerSortValueLessThanOrEqual] (integer)
* updateResponseProfile[filter][rootEntryIdEqual] (string)
* updateResponseProfile[filter][rootEntryIdIn] (string)
* updateResponseProfile[filter][parentEntryIdEqual] (string)
* updateResponseProfile[filter][entitledUsersEditMatchAnd] (string)
* updateResponseProfile[filter][entitledUsersEditMatchOr] (string)
* updateResponseProfile[filter][entitledUsersPublishMatchAnd] (string)
* updateResponseProfile[filter][entitledUsersPublishMatchOr] (string)
* updateResponseProfile[filter][tagsNameMultiLikeOr] (string)
* updateResponseProfile[filter][tagsAdminTagsMultiLikeOr] (string)
* updateResponseProfile[filter][tagsAdminTagsNameMultiLikeOr] (string)
* updateResponseProfile[filter][tagsNameMultiLikeAnd] (string)
* updateResponseProfile[filter][tagsAdminTagsMultiLikeAnd] (string)
* updateResponseProfile[filter][tagsAdminTagsNameMultiLikeAnd] (string)
* updateResponseProfile[filter][categoryIdEqual] (integer)
* updateResponseProfile[filter][categoryIdIn] (string)
* updateResponseProfile[filter][permissionLevelEqual] (integer) - Enum Type: `KalturaCategoryUserPermissionLevel`
* updateResponseProfile[filter][permissionLevelIn] (string)
* updateResponseProfile[filter][updateMethodEqual] (integer) - Enum Type: `KalturaUpdateMethodType`
* updateResponseProfile[filter][updateMethodIn] (string)
* updateResponseProfile[filter][categoryFullIdsStartsWith] (string)
* updateResponseProfile[filter][categoryFullIdsEqual] (string)
* updateResponseProfile[filter][permissionNamesMatchAnd] (string)
* updateResponseProfile[filter][permissionNamesMatchOr] (string)
* updateResponseProfile[filter][permissionNamesNotContains] (string)
* updateResponseProfile[filter][screenNameLike] (string)
* updateResponseProfile[filter][screenNameStartsWith] (string)
* updateResponseProfile[filter][emailLike] (string)
* updateResponseProfile[filter][emailStartsWith] (string)
* updateResponseProfile[filter][firstNameStartsWith] (string)
* updateResponseProfile[filter][lastNameStartsWith] (string)
* updateResponseProfile[filter][isAdminEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][systemNameEqual] (string)
* updateResponseProfile[filter][systemNameIn] (string)
* updateResponseProfile[filter][isSystemDefaultEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][tagsEqual] (string)
* updateResponseProfile[filter][parsedAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][parsedAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][auditObjectTypeEqual] (string) - Enum Type: `KalturaAuditTrailObjectType`
* updateResponseProfile[filter][auditObjectTypeIn] (string)
* updateResponseProfile[filter][objectIdEqual] (string)
* updateResponseProfile[filter][objectIdIn] (string)
* updateResponseProfile[filter][relatedObjectIdEqual] (string)
* updateResponseProfile[filter][relatedObjectIdIn] (string)
* updateResponseProfile[filter][relatedObjectTypeEqual] (string) - Enum Type: `KalturaAuditTrailObjectType`
* updateResponseProfile[filter][relatedObjectTypeIn] (string)
* updateResponseProfile[filter][masterPartnerIdEqual] (integer)
* updateResponseProfile[filter][masterPartnerIdIn] (string)
* updateResponseProfile[filter][requestIdEqual] (string)
* updateResponseProfile[filter][requestIdIn] (string)
* updateResponseProfile[filter][actionEqual] (string) - Enum Type: `KalturaAuditTrailAction`
* updateResponseProfile[filter][actionIn] (string)
* updateResponseProfile[filter][ksEqual] (string)
* updateResponseProfile[filter][contextEqual] (integer) - Enum Type: `KalturaAuditTrailContext`
* updateResponseProfile[filter][contextIn] (string)
* updateResponseProfile[filter][entryPointEqual] (string)
* updateResponseProfile[filter][entryPointIn] (string)
* updateResponseProfile[filter][serverNameEqual] (string)
* updateResponseProfile[filter][serverNameIn] (string)
* updateResponseProfile[filter][ipAddressEqual] (string)
* updateResponseProfile[filter][ipAddressIn] (string)
* updateResponseProfile[filter][clientTagEqual] (string)
* updateResponseProfile[filter][parentIdEqual] (integer)
* updateResponseProfile[filter][parentIdIn] (string)
* updateResponseProfile[filter][depthEqual] (integer)
* updateResponseProfile[filter][fullNameEqual] (string)
* updateResponseProfile[filter][fullNameStartsWith] (string)
* updateResponseProfile[filter][fullNameIn] (string)
* updateResponseProfile[filter][fullIdsEqual] (string)
* updateResponseProfile[filter][fullIdsStartsWith] (string)
* updateResponseProfile[filter][fullIdsMatchOr] (string)
* updateResponseProfile[filter][appearInListEqual] (integer) - Enum Type: `KalturaAppearInListType`
* updateResponseProfile[filter][privacyEqual] (integer) - Enum Type: `KalturaPrivacyType`
* updateResponseProfile[filter][privacyIn] (string)
* updateResponseProfile[filter][inheritanceTypeEqual] (integer) - Enum Type: `KalturaInheritanceType`
* updateResponseProfile[filter][inheritanceTypeIn] (string)
* updateResponseProfile[filter][referenceIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][contributionPolicyEqual] (integer) - Enum Type: `KalturaContributionPolicyType`
* updateResponseProfile[filter][membersCountGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][membersCountLessThanOrEqual] (integer)
* updateResponseProfile[filter][pendingMembersCountGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][pendingMembersCountLessThanOrEqual] (integer)
* updateResponseProfile[filter][privacyContextEqual] (string)
* updateResponseProfile[filter][inheritedParentIdEqual] (integer)
* updateResponseProfile[filter][inheritedParentIdIn] (string)
* updateResponseProfile[filter][aggregationCategoriesMultiLikeOr] (string)
* updateResponseProfile[filter][aggregationCategoriesMultiLikeAnd] (string)
* updateResponseProfile[filter][creatorUserIdEqual] (string)
* updateResponseProfile[filter][creatorUserIdIn] (string)
* updateResponseProfile[filter][conversionProfileIdEqual] (integer)
* updateResponseProfile[filter][conversionProfileIdIn] (string)
* updateResponseProfile[filter][assetParamsIdEqual] (integer)
* updateResponseProfile[filter][assetParamsIdIn] (string)
* updateResponseProfile[filter][readyBehaviorEqual] (integer) - Enum Type: `KalturaFlavorReadyBehaviorType`
* updateResponseProfile[filter][readyBehaviorIn] (string)
* updateResponseProfile[filter][originEqual] (integer) - Enum Type: `KalturaAssetParamsOrigin`
* updateResponseProfile[filter][originIn] (string)
* updateResponseProfile[filter][defaultEntryIdEqual] (string)
* updateResponseProfile[filter][defaultEntryIdIn] (string)
* updateResponseProfile[filter][cuePointTypeEqual] (string) - Enum Type: `KalturaCuePointType`
* updateResponseProfile[filter][cuePointTypeIn] (string)
* updateResponseProfile[filter][triggeredAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][triggeredAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][startTimeGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][startTimeLessThanOrEqual] (integer)
* updateResponseProfile[filter][partnerSortValueEqual] (integer)
* updateResponseProfile[filter][partnerSortValueIn] (string)
* updateResponseProfile[filter][forceStopEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][submittedAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][submittedAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][distributionProfileIdEqual] (integer)
* updateResponseProfile[filter][distributionProfileIdIn] (string)
* updateResponseProfile[filter][dirtyStatusEqual] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* updateResponseProfile[filter][dirtyStatusIn] (string)
* updateResponseProfile[filter][sunriseGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][sunriseLessThanOrEqual] (integer)
* updateResponseProfile[filter][sunsetGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][sunsetLessThanOrEqual] (integer)
* updateResponseProfile[filter][fileAssetObjectTypeEqual] (string) - Enum Type: `KalturaFileAssetObjectType`
* updateResponseProfile[filter][groupIdIn] (string)
* updateResponseProfile[filter][channelIdEqual] (string)
* updateResponseProfile[filter][channelIdIn] (string)
* updateResponseProfile[filter][metadataProfileIdEqual] (integer)
* updateResponseProfile[filter][metadataProfileIdIn] (string)
* updateResponseProfile[filter][metadataProfileVersionEqual] (integer)
* updateResponseProfile[filter][metadataProfileVersionGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][metadataProfileVersionLessThanOrEqual] (integer)
* updateResponseProfile[filter][metadataObjectTypeEqual] (string) - Enum Type: `KalturaMetadataObjectType`
* updateResponseProfile[filter][versionEqual] (integer)
* updateResponseProfile[filter][versionGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][versionLessThanOrEqual] (integer)
* updateResponseProfile[filter][nameIn] (string)
* updateResponseProfile[filter][friendlyNameLike] (string)
* updateResponseProfile[filter][descriptionLike] (string)
* updateResponseProfile[filter][dependsOnPermissionNamesMultiLikeOr] (string)
* updateResponseProfile[filter][dependsOnPermissionNamesMultiLikeAnd] (string)
* updateResponseProfile[filter][parentIdNotIn] (string)
* updateResponseProfile[filter][ownerIdEqual] (string)
* updateResponseProfile[filter][ownerIdIn] (string)
* updateResponseProfile[filter][priorityEqual] (integer)
* updateResponseProfile[filter][priorityIn] (string)
* updateResponseProfile[filter][priorityGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][priorityLessThanOrEqual] (integer)
* updateResponseProfile[filter][recurrenceTypeEqual] (integer) - Enum Type: `KalturaScheduleEventRecurrenceType`
* updateResponseProfile[filter][recurrenceTypeIn] (string)
* updateResponseProfile[filter][eventIdEqual] (integer)
* updateResponseProfile[filter][eventIdIn] (string)
* updateResponseProfile[filter][resourceIdEqual] (integer)
* updateResponseProfile[filter][resourceIdIn] (string)
* updateResponseProfile[filter][entryIdNotIn] (string)
* updateResponseProfile[filter][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* updateResponseProfile[filter][extendedStatusIn] (string)
* updateResponseProfile[filter][extendedStatusNotIn] (string)
* updateResponseProfile[filter][loginEmailEqual] (string)
* updateResponseProfile[filter][formatEqual] (string) - Enum Type: `KalturaAttachmentType`
* updateResponseProfile[filter][formatIn] (string)
* updateResponseProfile[filter][captionParamsIdEqual] (integer)
* updateResponseProfile[filter][captionParamsIdIn] (string)
* updateResponseProfile[filter][flavorParamsIdEqual] (integer)
* updateResponseProfile[filter][flavorParamsIdIn] (string)
* updateResponseProfile[filter][thumbParamsIdEqual] (integer)
* updateResponseProfile[filter][thumbParamsIdIn] (string)
* updateResponseProfile[filter][contentLike] (string)
* updateResponseProfile[filter][contentMultiLikeOr] (string)
* updateResponseProfile[filter][contentMultiLikeAnd] (string)
* updateResponseProfile[filter][partnerDescriptionLike] (string)
* updateResponseProfile[filter][partnerDescriptionMultiLikeOr] (string)
* updateResponseProfile[filter][partnerDescriptionMultiLikeAnd] (string)
* updateResponseProfile[filter][languageEqual] (string) - Enum Type: `KalturaLanguage`
* updateResponseProfile[filter][languageIn] (string)
* updateResponseProfile[filter][labelEqual] (string)
* updateResponseProfile[filter][labelIn] (string)
* updateResponseProfile[filter][endTimeGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][endTimeLessThanOrEqual] (integer)
* updateResponseProfile[filter][freeText] (string)
* updateResponseProfile[filter][isRoot] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][categoriesFullNameIn] (string)
* updateResponseProfile[filter][categoryAncestorIdIn] (string) - All entries within this categoy or in child categories
* updateResponseProfile[filter][redirectFromEntryId] (string) - The id of the original entry
* updateResponseProfile[filter][lastPlayedAtGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][lastPlayedAtLessThanOrEqual] (integer)
* updateResponseProfile[filter][durationLessThan] (integer)
* updateResponseProfile[filter][durationGreaterThan] (integer)
* updateResponseProfile[filter][durationLessThanOrEqual] (integer)
* updateResponseProfile[filter][durationGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][durationTypeMatchOr] (string)
* updateResponseProfile[filter][documentTypeEqual] (integer) - Enum Type: `KalturaDocumentType`
* updateResponseProfile[filter][documentTypeIn] (string)
* updateResponseProfile[filter][assetParamsIdsMatchOr] (string)
* updateResponseProfile[filter][assetParamsIdsMatchAnd] (string)
* updateResponseProfile[filter][mediaTypeEqual] (integer) - Enum Type: `KalturaMediaType`
* updateResponseProfile[filter][mediaTypeIn] (string)
* updateResponseProfile[filter][sourceTypeEqual] (string) - Enum Type: `KalturaSourceType`
* updateResponseProfile[filter][sourceTypeNotEqual] (string) - Enum Type: `KalturaSourceType`
* updateResponseProfile[filter][sourceTypeIn] (string)
* updateResponseProfile[filter][sourceTypeNotIn] (string)
* updateResponseProfile[filter][mediaDateGreaterThanOrEqual] (integer)
* updateResponseProfile[filter][mediaDateLessThanOrEqual] (integer)
* updateResponseProfile[filter][flavorParamsIdsMatchOr] (string)
* updateResponseProfile[filter][flavorParamsIdsMatchAnd] (string)
* updateResponseProfile[filter][limit] (integer)
* updateResponseProfile[filter][externalSourceTypeEqual] (string) - Enum Type: `KalturaExternalMediaSourceType`
* updateResponseProfile[filter][externalSourceTypeIn] (string)
* updateResponseProfile[filter][isLive] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][isRecordedEntryIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][hasMediaServerHostname] (string)
* updateResponseProfile[filter][categoryDirectMembers] (boolean) - Return the list of categoryUser that are not inherited from parent category - only the direct categoryUsers.
* updateResponseProfile[filter][relatedGroupsByUserId] (string) - Return a list of categoryUser that related to the userId in this field by groups
* updateResponseProfile[filter][idOrScreenNameStartsWith] (string)
* updateResponseProfile[filter][loginEnabledEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][roleIdEqual] (string)
* updateResponseProfile[filter][roleIdsEqual] (string)
* updateResponseProfile[filter][roleIdsIn] (string)
* updateResponseProfile[filter][firstNameOrLastNameStartsWith] (string)
* updateResponseProfile[filter][permissionNamesMultiLikeOr] (string) - Permission names filter expression
* updateResponseProfile[filter][permissionNamesMultiLikeAnd] (string) - Permission names filter expression
* updateResponseProfile[filter][flavorParamsVersionEqual] (string)
* updateResponseProfile[filter][flavorAssetIdEqual] (string)
* updateResponseProfile[filter][flavorAssetVersionEqual] (string)
* updateResponseProfile[filter][thumbParamsVersionEqual] (string)
* updateResponseProfile[filter][thumbAssetIdEqual] (string)
* updateResponseProfile[filter][thumbAssetVersionEqual] (string)
* updateResponseProfile[filter][membersIn] (string)
* updateResponseProfile[filter][nameOrReferenceIdStartsWith] (string)
* updateResponseProfile[filter][managerEqual] (string)
* updateResponseProfile[filter][memberEqual] (string)
* updateResponseProfile[filter][fullNameStartsWithIn] (string)
* updateResponseProfile[filter][ancestorIdIn] (string) - not includes the category itself (only sub categories)
* updateResponseProfile[filter][idOrInheritedParentIdIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][orderBy] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][objectType] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][value] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][categoriesMatchOr] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][categoryEntryStatusIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][categoryIdEqual] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][memberIdEq] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][memberIdIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][memberPermissionsMatchOr] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][memberPermissionsMatchAnd] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][noDistributionProfiles] (boolean)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][distributionProfileId] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][contentLike] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][contentMultiLikeOr] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][contentMultiLikeAnd] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][cuePointsFreeText] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][cuePointTypeIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][cuePointSubTypeEqual] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][watermarkId] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][indexIdGreaterThan] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][depthGreaterThanEqual] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][field] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][items] (array)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][idEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][idIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][userIdEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][userIdIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][updatedAtLessThanOrEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][extendedStatusIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][not] (boolean)
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* updateResponseProfile[filter][conversionProfileIdFilter][advancedSearch][metadataProfileId] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][idEqual] (integer)
* updateResponseProfile[filter][conversionProfileIdFilter][idIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][statusEqual] (string) - Enum Type: `KalturaConversionProfileStatus`
* updateResponseProfile[filter][conversionProfileIdFilter][statusIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][typeEqual] (string) - Enum Type: `KalturaConversionProfileType`
* updateResponseProfile[filter][conversionProfileIdFilter][typeIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][nameEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][systemNameEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][systemNameIn] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][tagsMultiLikeOr] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][tagsMultiLikeAnd] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][defaultEntryIdEqual] (string)
* updateResponseProfile[filter][conversionProfileIdFilter][defaultEntryIdIn] (string)
* updateResponseProfile[filter][userIdEqualCurrent] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][userIdCurrent] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][protocolTypeEqual] (string) - Enum Type: `KalturaAdProtocolType`
* updateResponseProfile[filter][protocolTypeIn] (string)
* updateResponseProfile[filter][titleLike] (string)
* updateResponseProfile[filter][titleMultiLikeOr] (string)
* updateResponseProfile[filter][titleMultiLikeAnd] (string)
* updateResponseProfile[filter][textLike] (string)
* updateResponseProfile[filter][textMultiLikeOr] (string)
* updateResponseProfile[filter][textMultiLikeAnd] (string)
* updateResponseProfile[filter][isPublicEqual] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][quizUserEntryIdEqual] (string)
* updateResponseProfile[filter][quizUserEntryIdIn] (string)
* updateResponseProfile[filter][codeLike] (string)
* updateResponseProfile[filter][codeMultiLikeOr] (string)
* updateResponseProfile[filter][codeMultiLikeAnd] (string)
* updateResponseProfile[filter][codeEqual] (string)
* updateResponseProfile[filter][codeIn] (string)
* updateResponseProfile[filter][descriptionMultiLikeOr] (string)
* updateResponseProfile[filter][descriptionMultiLikeAnd] (string)
* updateResponseProfile[filter][eventTypeEqual] (string) - Enum Type: `KalturaEventType`
* updateResponseProfile[filter][eventTypeIn] (string)
* updateResponseProfile[filter][questionLike] (string)
* updateResponseProfile[filter][questionMultiLikeOr] (string)
* updateResponseProfile[filter][questionMultiLikeAnd] (string)
* updateResponseProfile[filter][subTypeEqual] (integer) - Enum Type: `KalturaThumbCuePointSubType`
* updateResponseProfile[filter][subTypeIn] (string)
* updateResponseProfile[filter][resourceIdsLike] (string)
* updateResponseProfile[filter][resourceIdsMultiLikeOr] (string)
* updateResponseProfile[filter][resourceIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][parentResourceIdsLike] (string)
* updateResponseProfile[filter][parentResourceIdsMultiLikeOr] (string)
* updateResponseProfile[filter][parentResourceIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][templateEntryCategoriesIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][templateEntryCategoriesIdsMultiLikeOr] (string)
* updateResponseProfile[filter][resourceSystemNamesMultiLikeOr] (string)
* updateResponseProfile[filter][templateEntryCategoriesIdsLike] (string)
* updateResponseProfile[filter][resourceSystemNamesMultiLikeAnd] (string)
* updateResponseProfile[filter][resourceSystemNamesLike] (string)
* updateResponseProfile[filter][templateEntryIdEqual] (string)
* updateResponseProfile[filter][entryIdsLike] (string)
* updateResponseProfile[filter][entryIdsMultiLikeOr] (string)
* updateResponseProfile[filter][entryIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][categoryIdsLike] (string)
* updateResponseProfile[filter][categoryIdsMultiLikeOr] (string)
* updateResponseProfile[filter][categoryIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][parentCategoryIdsLike] (string)
* updateResponseProfile[filter][parentCategoryIdsMultiLikeOr] (string)
* updateResponseProfile[filter][parentCategoryIdsMultiLikeAnd] (string)
* updateResponseProfile[filter][eventIdOrItsParentIdEqual] (integer) - Find event-resource objects that associated with the event, if none found, find by its parent event
* updateResponseProfile[filter][isAnonymous] (integer) - Enum Type: `KalturaNullableBoolean`
* updateResponseProfile[filter][privacyContextIn] (string)
* updateResponseProfile[systemName] (string) - Unique system name

### responseProfile.updateStatus
Update response profile status by id


```js
kaltura.responseProfile.updateStatus({
  "id": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* status (integer) **required** - Enum Type: `KalturaResponseProfileStatus`

### scheduleEvent.add
Allows you to add a new KalturaScheduleEvent object


```js
kaltura.scheduleEvent.add({}, context)
```


### scheduleEvent.addFromBulkUpload
Add new bulk upload batch job


```js
kaltura.scheduleEvent.addFromBulkUpload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries
* bulkUploadData[eventsType] (integer) - Enum Type: `KalturaScheduleEventType`

### scheduleEvent.cancel
Mark the KalturaScheduleEvent object as cancelled


```js
kaltura.scheduleEvent.cancel({
  "scheduleEventId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**

### scheduleEvent.delete
Mark the KalturaScheduleEvent object as deleted


```js
kaltura.scheduleEvent.delete({
  "scheduleEventId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**

### scheduleEvent.get
Retrieve a KalturaScheduleEvent object by ID


```js
kaltura.scheduleEvent.get({
  "scheduleEventId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**

### scheduleEvent.getConflicts
List conflicting events for resourcesIds by event's dates


```js
kaltura.scheduleEvent.getConflicts({
  "resourceIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* resourceIds (string) **required** - comma separated
* scheduleEvent[summary] (string) - Defines a short summary or subject for the event
* scheduleEvent[description] (string)
* scheduleEvent[startDate] (integer)
* scheduleEvent[endDate] (integer)
* scheduleEvent[referenceId] (string)
* scheduleEvent[classificationType] (integer) - Enum Type: `KalturaScheduleEventClassificationType`
* scheduleEvent[geoLatitude] (number) - Specifies the global position for the activity
* scheduleEvent[geoLongitude] (number) - Specifies the global position for the activity
* scheduleEvent[location] (string) - Defines the intended venue for the activity
* scheduleEvent[organizer] (string)
* scheduleEvent[ownerId] (string)
* scheduleEvent[priority] (integer) - The value for the priority field.
* scheduleEvent[sequence] (integer) - Defines the revision sequence number.
* scheduleEvent[recurrenceType] (integer) - Enum Type: `KalturaScheduleEventRecurrenceType`
* scheduleEvent[duration] (integer) - Duration in seconds
* scheduleEvent[contact] (string) - Used to represent contact information or alternately a reference to contact information.
* scheduleEvent[comment] (string) - Specifies non-processing information intended to provide a comment to the calendar user.
* scheduleEvent[tags] (string)
* scheduleEvent[recurrence][name] (string)
* scheduleEvent[recurrence][frequency] (string) - Enum Type: `KalturaScheduleEventRecurrenceFrequency`
* scheduleEvent[recurrence][until] (integer)
* scheduleEvent[recurrence][timeZone] (string) - TimeZone String
* scheduleEvent[recurrence][count] (integer)
* scheduleEvent[recurrence][interval] (integer)
* scheduleEvent[recurrence][bySecond] (string) - Comma separated numbers between 0 to 59
* scheduleEvent[recurrence][byMinute] (string) - Comma separated numbers between 0 to 59
* scheduleEvent[recurrence][byHour] (string) - Comma separated numbers between 0 to 23
* scheduleEvent[recurrence][byDay] (string) - Comma separated of KalturaScheduleEventRecurrenceDay
* scheduleEvent[recurrence][byMonthDay] (string) - Comma separated of numbers between -31 to 31, excluding 0.
* scheduleEvent[recurrence][byYearDay] (string) - Comma separated of numbers between -366 to 366, excluding 0.
* scheduleEvent[recurrence][byWeekNumber] (string) - Comma separated of numbers between -53 to 53, excluding 0.
* scheduleEvent[recurrence][byMonth] (string) - Comma separated numbers between 1 to 12
* scheduleEvent[recurrence][byOffset] (string) - Comma separated of numbers between -366 to 366, excluding 0.
* scheduleEvent[recurrence][weekStartDay] (string) - Enum Type: `KalturaScheduleEventRecurrenceDay`
* scheduleEventIdToIgnore (string)

### scheduleEvent.list
List KalturaScheduleEvent objects


```js
kaltura.scheduleEvent.list({}, context)
```


### scheduleEvent.update
Update an existing KalturaScheduleEvent object


```js
kaltura.scheduleEvent.update({
  "scheduleEventId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**
* scheduleEvent[summary] (string) - Defines a short summary or subject for the event
* scheduleEvent[description] (string)
* scheduleEvent[startDate] (integer)
* scheduleEvent[endDate] (integer)
* scheduleEvent[referenceId] (string)
* scheduleEvent[classificationType] (integer) - Enum Type: `KalturaScheduleEventClassificationType`
* scheduleEvent[geoLatitude] (number) - Specifies the global position for the activity
* scheduleEvent[geoLongitude] (number) - Specifies the global position for the activity
* scheduleEvent[location] (string) - Defines the intended venue for the activity
* scheduleEvent[organizer] (string)
* scheduleEvent[ownerId] (string)
* scheduleEvent[priority] (integer) - The value for the priority field.
* scheduleEvent[sequence] (integer) - Defines the revision sequence number.
* scheduleEvent[recurrenceType] (integer) - Enum Type: `KalturaScheduleEventRecurrenceType`
* scheduleEvent[duration] (integer) - Duration in seconds
* scheduleEvent[contact] (string) - Used to represent contact information or alternately a reference to contact information.
* scheduleEvent[comment] (string) - Specifies non-processing information intended to provide a comment to the calendar user.
* scheduleEvent[tags] (string)
* scheduleEvent[recurrence][name] (string)
* scheduleEvent[recurrence][frequency] (string) - Enum Type: `KalturaScheduleEventRecurrenceFrequency`
* scheduleEvent[recurrence][until] (integer)
* scheduleEvent[recurrence][timeZone] (string) - TimeZone String
* scheduleEvent[recurrence][count] (integer)
* scheduleEvent[recurrence][interval] (integer)
* scheduleEvent[recurrence][bySecond] (string) - Comma separated numbers between 0 to 59
* scheduleEvent[recurrence][byMinute] (string) - Comma separated numbers between 0 to 59
* scheduleEvent[recurrence][byHour] (string) - Comma separated numbers between 0 to 23
* scheduleEvent[recurrence][byDay] (string) - Comma separated of KalturaScheduleEventRecurrenceDay
* scheduleEvent[recurrence][byMonthDay] (string) - Comma separated of numbers between -31 to 31, excluding 0.
* scheduleEvent[recurrence][byYearDay] (string) - Comma separated of numbers between -366 to 366, excluding 0.
* scheduleEvent[recurrence][byWeekNumber] (string) - Comma separated of numbers between -53 to 53, excluding 0.
* scheduleEvent[recurrence][byMonth] (string) - Comma separated numbers between 1 to 12
* scheduleEvent[recurrence][byOffset] (string) - Comma separated of numbers between -366 to 366, excluding 0.
* scheduleEvent[recurrence][weekStartDay] (string) - Enum Type: `KalturaScheduleEventRecurrenceDay`

### scheduleEventResource.add
Allows you to add a new KalturaScheduleEventResource object


```js
kaltura.scheduleEventResource.add({}, context)
```


### scheduleEventResource.delete
Mark the KalturaScheduleEventResource object as deleted


```js
kaltura.scheduleEventResource.delete({
  "scheduleEventId": 0,
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**
* scheduleResourceId (integer) **required**

### scheduleEventResource.get
Retrieve a KalturaScheduleEventResource object by ID


```js
kaltura.scheduleEventResource.get({
  "scheduleEventId": 0,
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**
* scheduleResourceId (integer) **required**

### scheduleEventResource.list
List KalturaScheduleEventResource objects


```js
kaltura.scheduleEventResource.list({}, context)
```


### scheduleEventResource.update
Update an existing KalturaScheduleEventResource object


```js
kaltura.scheduleEventResource.update({
  "scheduleEventId": 0,
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleEventId (integer) **required**
* scheduleResourceId (integer) **required**
* scheduleEventResource[eventId] (integer) - `insertOnly`
* scheduleEventResource[resourceId] (integer) - `insertOnly`

### scheduleResource.add
Allows you to add a new KalturaScheduleResource object


```js
kaltura.scheduleResource.add({}, context)
```


### scheduleResource.addFromBulkUpload
Add new bulk upload batch job


```js
kaltura.scheduleResource.addFromBulkUpload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries
* bulkUploadData[columns] (array)

### scheduleResource.delete
Mark the KalturaScheduleResource object as deleted


```js
kaltura.scheduleResource.delete({
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleResourceId (integer) **required**

### scheduleResource.get
Retrieve a KalturaScheduleResource object by ID


```js
kaltura.scheduleResource.get({
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleResourceId (integer) **required**

### scheduleResource.list
List KalturaScheduleResource objects


```js
kaltura.scheduleResource.list({}, context)
```


### scheduleResource.update
Update an existing KalturaScheduleResource object


```js
kaltura.scheduleResource.update({
  "scheduleResourceId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduleResourceId (integer) **required**
* scheduleResource[parentId] (integer)
* scheduleResource[name] (string) - Defines a short name
* scheduleResource[systemName] (string) - Defines a unique system-name
* scheduleResource[description] (string)
* scheduleResource[tags] (string)
* scheduleResource[objectType] (string)
* scheduleResource[streamUrl] (string) - URL of the stream
* scheduleResource[entryId] (string)

### scheduledTaskProfile.add
Add a new scheduled task profile


```js
kaltura.scheduledTaskProfile.add({}, context)
```


### scheduledTaskProfile.delete
Delete a scheduled task profile


```js
kaltura.scheduledTaskProfile.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### scheduledTaskProfile.get
Retrieve a scheduled task profile by id


```js
kaltura.scheduledTaskProfile.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### scheduledTaskProfile.getDryRunResults



```js
kaltura.scheduledTaskProfile.getDryRunResults({
  "requestId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* requestId (integer) **required**

### scheduledTaskProfile.list
List scheduled task profiles


```js
kaltura.scheduledTaskProfile.list({}, context)
```


### scheduledTaskProfile.requestDryRun



```js
kaltura.scheduledTaskProfile.requestDryRun({
  "scheduledTaskProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* scheduledTaskProfileId (integer) **required**
* maxResults (integer)

### scheduledTaskProfile.update
Update an existing scheduled task profile


```js
kaltura.scheduledTaskProfile.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* scheduledTaskProfile[name] (string)
* scheduledTaskProfile[systemName] (string)
* scheduledTaskProfile[description] (string)
* scheduledTaskProfile[status] (integer) - Enum Type: `KalturaScheduledTaskProfileStatus`
* scheduledTaskProfile[objectFilterEngineType] (string) - Enum Type: `KalturaObjectFilterEngineType`
* scheduledTaskProfile[objectFilter][orderBy] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][objectType] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][value] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][categoriesMatchOr] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][categoryEntryStatusIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* scheduledTaskProfile[objectFilter][advancedSearch][categoryIdEqual] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][memberIdEq] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][memberIdIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][memberPermissionsMatchOr] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][memberPermissionsMatchAnd] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][noDistributionProfiles] (boolean)
* scheduledTaskProfile[objectFilter][advancedSearch][distributionProfileId] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* scheduledTaskProfile[objectFilter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* scheduledTaskProfile[objectFilter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* scheduledTaskProfile[objectFilter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* scheduledTaskProfile[objectFilter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* scheduledTaskProfile[objectFilter][advancedSearch][contentLike] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][contentMultiLikeOr] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][contentMultiLikeAnd] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][cuePointsFreeText] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][cuePointTypeIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][cuePointSubTypeEqual] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][watermarkId] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][indexIdGreaterThan] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][depthGreaterThanEqual] (integer)
* scheduledTaskProfile[objectFilter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* scheduledTaskProfile[objectFilter][advancedSearch][field] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* scheduledTaskProfile[objectFilter][advancedSearch][items] (array)
* scheduledTaskProfile[objectFilter][advancedSearch][idEqual] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][idIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][userIdEqual] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][userIdIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][updatedAtLessThanOrEqual] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* scheduledTaskProfile[objectFilter][advancedSearch][extendedStatusIn] (string)
* scheduledTaskProfile[objectFilter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* scheduledTaskProfile[objectFilter][advancedSearch][not] (boolean)
* scheduledTaskProfile[objectFilter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* scheduledTaskProfile[objectFilter][advancedSearch][metadataProfileId] (integer)

### schema.serve
Serves the requested XSD according to the type and name.


```js
kaltura.schema.serve({
  "type": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* type (string) **required** - Enum Type: `KalturaSchemaType`

### serverNode.add
Adds a server node to the Kaltura DB.


```js
kaltura.serverNode.add({}, context)
```


### serverNode.delete
delete server node by id


```js
kaltura.serverNode.delete({
  "serverNodeId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* serverNodeId (string) **required**

### serverNode.disable
Disable server node by id


```js
kaltura.serverNode.disable({
  "serverNodeId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* serverNodeId (string) **required**

### serverNode.enable
Enable server node by id


```js
kaltura.serverNode.enable({
  "serverNodeId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* serverNodeId (string) **required**

### serverNode.get
Get server node by id


```js
kaltura.serverNode.get({
  "serverNodeId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* serverNodeId (integer) **required**

### serverNode.list



```js
kaltura.serverNode.list({}, context)
```


### serverNode.reportStatus
Update server node status


```js
kaltura.serverNode.reportStatus({
  "hostName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* hostName (string) **required**
* serverNode[name] (string) - serverNode name
* serverNode[systemName] (string) - serverNode uniqe system name
* serverNode[description] (string)
* serverNode[hostName] (string) - serverNode hostName
* serverNode[tags] (string) - serverNode tags
* serverNode[parentId] (string) - Id of the parent serverNode
* serverNode[objectType] (string)
* serverNode[deliveryProfileIds] (array)
* serverNode[playbackDomain] (string) - Delivery server playback Domain
* serverNode[config] (string) - Overdie edge server default configuration - json format
* serverNode[applicationName] (string) - Media server application name
* serverNode[mediaServerPortConfig] (array)
* serverNode[mediaServerPlaybackDomainConfig] (array)
* serverNode[appPrefix] (string) - Wowza Media server app prefix
* serverNode[transcoder] (string) - Wowza Media server transcoder configuration overide
* serverNode[GPUID] (integer) - Wowza Media server GPU index id
* serverNode[liveServicePort] (integer) - Live service port
* serverNode[liveServiceProtocol] (string) - Live service protocol
* serverNode[liveServiceInternalDomain] (string) - Wowza media server live service internal domain

### serverNode.update
Update server node by id


```js
kaltura.serverNode.update({
  "serverNodeId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* serverNodeId (integer) **required**
* serverNode[name] (string) - serverNode name
* serverNode[systemName] (string) - serverNode uniqe system name
* serverNode[description] (string)
* serverNode[hostName] (string) - serverNode hostName
* serverNode[tags] (string) - serverNode tags
* serverNode[parentId] (string) - Id of the parent serverNode
* serverNode[objectType] (string)
* serverNode[deliveryProfileIds] (array)
* serverNode[playbackDomain] (string) - Delivery server playback Domain
* serverNode[config] (string) - Overdie edge server default configuration - json format
* serverNode[applicationName] (string) - Media server application name
* serverNode[mediaServerPortConfig] (array)
* serverNode[mediaServerPlaybackDomainConfig] (array)
* serverNode[appPrefix] (string) - Wowza Media server app prefix
* serverNode[transcoder] (string) - Wowza Media server transcoder configuration overide
* serverNode[GPUID] (integer) - Wowza Media server GPU index id
* serverNode[liveServicePort] (integer) - Live service port
* serverNode[liveServiceProtocol] (string) - Live service protocol
* serverNode[liveServiceInternalDomain] (string) - Wowza media server live service internal domain

### session.end
End a session with the Kaltura server, making the current KS invalid.


```js
kaltura.session.end({}, context)
```


### session.get
Parse session key and return its info


```js
kaltura.session.get({}, context)
```


### session.impersonate
Start an impersonated session with Kaltura's server.

The result KS is the session key that you should pass to all services that requires a ticket.


```js
kaltura.session.impersonate({
  "secret": "",
  "impersonatedPartnerId": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* secret (string) **required** - - should be the secret (admin or user) of the original partnerId (not impersonatedPartnerId).
* impersonatedPartnerId (integer) **required**
* userId (string) - - impersonated userId
* type (integer) - Enum Type: `KalturaSessionType`
* partnerId (integer)
* expiry (integer) - KS expiry time in seconds
* privileges (string)

### session.impersonateByKs
Start an impersonated session with Kaltura's server.

The result KS info contains the session key that you should pass to all services that requires a ticket.

Type, expiry and privileges won't be changed if they're not set


```js
kaltura.session.impersonateByKs({
  "session": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* session (string) **required** - The old KS of the impersonated partner
* type (integer) - Enum Type: `KalturaSessionType`
* expiry (integer) - Expiry time in seconds of the new KS
* privileges (string) - Privileges of the new KS

### session.start
Start a session with Kaltura's server.

The result KS is the session key that you should pass to all services that requires a ticket.


```js
kaltura.session.start({
  "secret": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* secret (string) **required** - Remember to provide the correct secret according to the sessionType you want
* userId (string)
* type (integer) - Enum Type: `KalturaSessionType`
* partnerId (integer)
* expiry (integer) - KS expiry time in seconds
* privileges (string)

### session.startWidgetSession
Start a session for Kaltura's flash widgets


```js
kaltura.session.startWidgetSession({
  "widgetId": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* widgetId (string) **required**
* expiry (integer)

### shortLink.add
Allows you to add a short link object


```js
kaltura.shortLink.add({}, context)
```


### shortLink.delete
Mark the short link as deleted


```js
kaltura.shortLink.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### shortLink.get
Retrieve an short link object by id


```js
kaltura.shortLink.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### shortLink.goto
Serves short link


```js
kaltura.shortLink.goto({
  "id": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* id (string) **required**
* proxy (boolean) - proxy the response instead of redirect

### shortLink.list
List short link objects by filter and pager


```js
kaltura.shortLink.list({}, context)
```


### shortLink.update
Update exisitng short link


```js
kaltura.shortLink.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* shortLink[expiresAt] (integer)
* shortLink[userId] (string)
* shortLink[name] (string)
* shortLink[systemName] (string)
* shortLink[fullUrl] (string)
* shortLink[status] (integer) - Enum Type: `KalturaShortLinkStatus`

### stats.collect
Will write to the event log a single line representing the event

client version - will help interprete the line structure. different client versions might have slightly different data/data formats in the line
event_id - number is the row number in yuval's excel
datetime - same format as MySql's datetime - can change and should reflect the time zone
session id - can be some big random number or guid
partner id
entry id
unique viewer
widget id
ui_conf id
uid - the puser id as set by the ppartner
current point - in milliseconds
duration - milliseconds
user ip
process duration - in milliseconds
control id
seek
new point
referrer

KalturaStatsEvent $event


```js
kaltura.stats.collect({}, context)
```


### stats.kmcCollect
Will collect the kmcEvent sent form the KMC client

// this will actually be an empty function because all events will be sent using GET and will anyway be logged in the apache log


```js
kaltura.stats.kmcCollect({}, context)
```


### stats.reportDeviceCapabilities
Use this action to report device capabilities to the kaltura server.


```js
kaltura.stats.reportDeviceCapabilities({
  "data": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* data (string) **required**

### stats.reportError
Use this action to report errors to the kaltura server.


```js
kaltura.stats.reportError({
  "errorCode": "",
  "errorMessage": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* errorCode (string) **required**
* errorMessage (string) **required**

### stats.reportKceError



```js
kaltura.stats.reportKceError({}, context)
```


### storageProfile.add
Adds a storage profile to the Kaltura DB.


```js
kaltura.storageProfile.add({}, context)
```


### storageProfile.get
Get storage profile by id


```js
kaltura.storageProfile.get({
  "storageProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* storageProfileId (integer) **required**

### storageProfile.list



```js
kaltura.storageProfile.list({}, context)
```


### storageProfile.update
Update storage profile by id


```js
kaltura.storageProfile.update({
  "storageProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* storageProfileId (integer) **required**
* storageProfile[name] (string)
* storageProfile[systemName] (string)
* storageProfile[desciption] (string)
* storageProfile[status] (integer) - Enum Type: `KalturaStorageProfileStatus`
* storageProfile[protocol] (string) - Enum Type: `KalturaStorageProfileProtocol`
* storageProfile[storageUrl] (string)
* storageProfile[storageBaseDir] (string)
* storageProfile[storageUsername] (string)
* storageProfile[storagePassword] (string)
* storageProfile[storageFtpPassiveMode] (boolean)
* storageProfile[minFileSize] (integer)
* storageProfile[maxFileSize] (integer)
* storageProfile[flavorParamsIds] (string)
* storageProfile[maxConcurrentConnections] (integer)
* storageProfile[pathManagerClass] (string)
* storageProfile[pathManagerParams] (array)
* storageProfile[trigger] (integer) - No need to create enum for temp field
* storageProfile[deliveryPriority] (integer) - Delivery Priority
* storageProfile[deliveryStatus] (integer) - Enum Type: `KalturaStorageProfileDeliveryStatus`
* storageProfile[readyBehavior] (integer) - Enum Type: `KalturaStorageProfileReadyBehavior`
* storageProfile[allowAutoDelete] (integer) - Flag sugnifying that the storage exported content should be deleted when soure entry is deleted
* storageProfile[createFileLink] (boolean) - Indicates to the local file transfer manager to create a link to the file instead of copying it
* storageProfile[rules] (array)
* storageProfile[deliveryProfileIds] (array)
* storageProfile[privateKey] (string)
* storageProfile[publicKey] (string)
* storageProfile[passPhrase] (string)
* storageProfile[shouldExportThumbs] (boolean)
* storageProfile[objectType] (string)
* storageProfile[filesPermissionInS3] (string) - Enum Type: `KalturaAmazonS3StorageProfileFilesPermissionLevel`
* storageProfile[s3Region] (string)
* storageProfile[sseType] (string)
* storageProfile[sseKmsKeyId] (string)
* storageProfile[signatureType] (string)
* storageProfile[endPoint] (string)
* storageProfile[serviceToken] (string)

### storageProfile.updateStatus



```js
kaltura.storageProfile.updateStatus({
  "storageId": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* storageId (integer) **required**
* status (integer) **required** - Enum Type: `KalturaStorageProfileStatus`

### synacorHbo.getFeed



```js
kaltura.synacorHbo.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### syndicationFeed.add
Add new Syndication Feed


```js
kaltura.syndicationFeed.add({}, context)
```


### syndicationFeed.delete
Delete Syndication Feed by ID


```js
kaltura.syndicationFeed.delete({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### syndicationFeed.get
Get Syndication Feed by ID


```js
kaltura.syndicationFeed.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### syndicationFeed.getEntryCount
get entry count for a syndication feed


```js
kaltura.syndicationFeed.getEntryCount({
  "feedId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* feedId (string) **required**

### syndicationFeed.list
List Syndication Feeds by filter with paging support


```js
kaltura.syndicationFeed.list({}, context)
```


### syndicationFeed.requestConversion
request conversion for all entries that doesnt have the required flavor param

returns a comma-separated ids of conversion jobs


```js
kaltura.syndicationFeed.requestConversion({
  "feedId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* feedId (string) **required**

### syndicationFeed.update
Update Syndication Feed by ID


```js
kaltura.syndicationFeed.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* syndicationFeed[playlistId] (string) - link a playlist that will set what content the feed will include
* syndicationFeed[name] (string) - feed name
* syndicationFeed[type] (integer) - `insertOnly`
* syndicationFeed[landingPage] (string) - Base URL for each video, on the partners site
* syndicationFeed[allowEmbed] (boolean) - allow_embed tells google OR yahoo weather to allow embedding the video on google OR yahoo video results
* syndicationFeed[playerUiconfId] (integer) - Select a uiconf ID as player skin to include in the kwidget url
* syndicationFeed[flavorParamId] (integer)
* syndicationFeed[transcodeExistingContent] (boolean)
* syndicationFeed[addToDefaultConversionProfile] (boolean)
* syndicationFeed[categories] (string)
* syndicationFeed[storageId] (integer)
* syndicationFeed[entriesOrderBy] (string) - Enum Type: `KalturaSyndicationFeedEntriesOrderBy`
* syndicationFeed[enforceEntitlement] (boolean) - Should enforce entitlement on feed entries
* syndicationFeed[privacyContext] (string) - Set privacy context for search entries that assiged to private and public categories within a category privacy context.
* syndicationFeed[useCategoryEntries] (boolean)
* syndicationFeed[feedContentTypeHeader] (string) - Feed content-type header value
* syndicationFeed[objectType] (string)
* syndicationFeed[feedDescription] (string) - feed description
* syndicationFeed[feedLandingPage] (string) - feed landing page (i.e publisher website)
* syndicationFeed[entryFilter][orderBy] (string)
* syndicationFeed[entryFilter][advancedSearch][objectType] (string)
* syndicationFeed[entryFilter][advancedSearch][value] (string)
* syndicationFeed[entryFilter][advancedSearch][categoriesMatchOr] (string)
* syndicationFeed[entryFilter][advancedSearch][categoryEntryStatusIn] (string)
* syndicationFeed[entryFilter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* syndicationFeed[entryFilter][advancedSearch][categoryIdEqual] (integer)
* syndicationFeed[entryFilter][advancedSearch][memberIdEq] (string)
* syndicationFeed[entryFilter][advancedSearch][memberIdIn] (string)
* syndicationFeed[entryFilter][advancedSearch][memberPermissionsMatchOr] (string)
* syndicationFeed[entryFilter][advancedSearch][memberPermissionsMatchAnd] (string)
* syndicationFeed[entryFilter][advancedSearch][noDistributionProfiles] (boolean)
* syndicationFeed[entryFilter][advancedSearch][distributionProfileId] (integer)
* syndicationFeed[entryFilter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* syndicationFeed[entryFilter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* syndicationFeed[entryFilter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* syndicationFeed[entryFilter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* syndicationFeed[entryFilter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* syndicationFeed[entryFilter][advancedSearch][contentLike] (string)
* syndicationFeed[entryFilter][advancedSearch][contentMultiLikeOr] (string)
* syndicationFeed[entryFilter][advancedSearch][contentMultiLikeAnd] (string)
* syndicationFeed[entryFilter][advancedSearch][cuePointsFreeText] (string)
* syndicationFeed[entryFilter][advancedSearch][cuePointTypeIn] (string)
* syndicationFeed[entryFilter][advancedSearch][cuePointSubTypeEqual] (integer)
* syndicationFeed[entryFilter][advancedSearch][watermarkId] (integer)
* syndicationFeed[entryFilter][advancedSearch][indexIdGreaterThan] (integer)
* syndicationFeed[entryFilter][advancedSearch][depthGreaterThanEqual] (integer)
* syndicationFeed[entryFilter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[entryFilter][advancedSearch][field] (string)
* syndicationFeed[entryFilter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* syndicationFeed[entryFilter][advancedSearch][items] (array)
* syndicationFeed[entryFilter][advancedSearch][idEqual] (string)
* syndicationFeed[entryFilter][advancedSearch][idIn] (string)
* syndicationFeed[entryFilter][advancedSearch][userIdEqual] (string)
* syndicationFeed[entryFilter][advancedSearch][userIdIn] (string)
* syndicationFeed[entryFilter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* syndicationFeed[entryFilter][advancedSearch][updatedAtLessThanOrEqual] (string)
* syndicationFeed[entryFilter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* syndicationFeed[entryFilter][advancedSearch][extendedStatusIn] (string)
* syndicationFeed[entryFilter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* syndicationFeed[entryFilter][advancedSearch][not] (boolean)
* syndicationFeed[entryFilter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* syndicationFeed[entryFilter][advancedSearch][metadataProfileId] (integer)
* syndicationFeed[entryFilter][idEqual] (string) - This filter should be in use for retrieving only a specific entry (identified by its entryId).
* syndicationFeed[entryFilter][idIn] (string) - This filter should be in use for retrieving few specific entries (string should include comma separated list of entryId strings).
* syndicationFeed[entryFilter][idNotIn] (string)
* syndicationFeed[entryFilter][nameLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry names (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][nameMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][nameMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][nameEqual] (string) - This filter should be in use for retrieving entries with a specific name.
* syndicationFeed[entryFilter][partnerIdEqual] (integer) - This filter should be in use for retrieving only entries which were uploaded by/assigned to users of a specific Kaltura Partner (identified by Partner ID).
* syndicationFeed[entryFilter][partnerIdIn] (string) - This filter should be in use for retrieving only entries within Kaltura network which were uploaded by/assigned to users of few Kaltura Partners  (string should include comma separated list of PartnerIDs)
* syndicationFeed[entryFilter][userIdEqual] (string) - This filter parameter should be in use for retrieving only entries, uploaded by/assigned to a specific user (identified by user Id).
* syndicationFeed[entryFilter][userIdIn] (string)
* syndicationFeed[entryFilter][userIdNotIn] (string)
* syndicationFeed[entryFilter][creatorIdEqual] (string)
* syndicationFeed[entryFilter][tagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][tagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][tagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][adminTagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags set by an ADMIN user (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][adminTagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][adminTagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* syndicationFeed[entryFilter][categoriesMatchAnd] (string)
* syndicationFeed[entryFilter][categoriesMatchOr] (string) - All entries within these categories or their child categories.
* syndicationFeed[entryFilter][categoriesNotContains] (string)
* syndicationFeed[entryFilter][categoriesIdsMatchAnd] (string)
* syndicationFeed[entryFilter][categoriesIdsMatchOr] (string) - All entries of the categories, excluding their child categories.
* syndicationFeed[entryFilter][categoriesIdsNotContains] (string)
* syndicationFeed[entryFilter][categoriesIdsEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[entryFilter][statusEqual] (string) - Enum Type: `KalturaEntryStatus`
* syndicationFeed[entryFilter][statusNotEqual] (string) - Enum Type: `KalturaEntryStatus`
* syndicationFeed[entryFilter][statusIn] (string) - This filter should be in use for retrieving only entries, at few specific {
* syndicationFeed[entryFilter][statusNotIn] (string) - This filter should be in use for retrieving only entries, not at few specific {
* syndicationFeed[entryFilter][moderationStatusEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* syndicationFeed[entryFilter][moderationStatusNotEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* syndicationFeed[entryFilter][moderationStatusIn] (string)
* syndicationFeed[entryFilter][moderationStatusNotIn] (string)
* syndicationFeed[entryFilter][typeEqual] (string) - Enum Type: `KalturaEntryType`
* syndicationFeed[entryFilter][typeIn] (string) - This filter should be in use for retrieving entries of few {
* syndicationFeed[entryFilter][createdAtGreaterThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system after a specific time/date (standard timestamp format).
* syndicationFeed[entryFilter][createdAtLessThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system before a specific time/date (standard timestamp format).
* syndicationFeed[entryFilter][updatedAtGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][updatedAtLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][totalRankLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][totalRankGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][groupIdEqual] (integer)
* syndicationFeed[entryFilter][searchTextMatchAnd] (string) - This filter should be in use for retrieving specific entries while search match the input string within all of the following metadata attributes: name, description, tags, adminTags.
* syndicationFeed[entryFilter][searchTextMatchOr] (string) - This filter should be in use for retrieving specific entries while search match the input string within at least one of the following metadata attributes: name, description, tags, adminTags.
* syndicationFeed[entryFilter][accessControlIdEqual] (integer)
* syndicationFeed[entryFilter][accessControlIdIn] (string)
* syndicationFeed[entryFilter][startDateGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][startDateLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][startDateGreaterThanOrEqualOrNull] (integer)
* syndicationFeed[entryFilter][startDateLessThanOrEqualOrNull] (integer)
* syndicationFeed[entryFilter][endDateGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][endDateLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][endDateGreaterThanOrEqualOrNull] (integer)
* syndicationFeed[entryFilter][endDateLessThanOrEqualOrNull] (integer)
* syndicationFeed[entryFilter][referenceIdEqual] (string)
* syndicationFeed[entryFilter][referenceIdIn] (string)
* syndicationFeed[entryFilter][replacingEntryIdEqual] (string)
* syndicationFeed[entryFilter][replacingEntryIdIn] (string)
* syndicationFeed[entryFilter][replacedEntryIdEqual] (string)
* syndicationFeed[entryFilter][replacedEntryIdIn] (string)
* syndicationFeed[entryFilter][replacementStatusEqual] (string) - Enum Type: `KalturaEntryReplacementStatus`
* syndicationFeed[entryFilter][replacementStatusIn] (string)
* syndicationFeed[entryFilter][partnerSortValueGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][partnerSortValueLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][rootEntryIdEqual] (string)
* syndicationFeed[entryFilter][rootEntryIdIn] (string)
* syndicationFeed[entryFilter][parentEntryIdEqual] (string)
* syndicationFeed[entryFilter][entitledUsersEditMatchAnd] (string)
* syndicationFeed[entryFilter][entitledUsersEditMatchOr] (string)
* syndicationFeed[entryFilter][entitledUsersPublishMatchAnd] (string)
* syndicationFeed[entryFilter][entitledUsersPublishMatchOr] (string)
* syndicationFeed[entryFilter][tagsNameMultiLikeOr] (string)
* syndicationFeed[entryFilter][tagsAdminTagsMultiLikeOr] (string)
* syndicationFeed[entryFilter][tagsAdminTagsNameMultiLikeOr] (string)
* syndicationFeed[entryFilter][tagsNameMultiLikeAnd] (string)
* syndicationFeed[entryFilter][tagsAdminTagsMultiLikeAnd] (string)
* syndicationFeed[entryFilter][tagsAdminTagsNameMultiLikeAnd] (string)
* syndicationFeed[entryFilter][freeText] (string)
* syndicationFeed[entryFilter][isRoot] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[entryFilter][categoriesFullNameIn] (string)
* syndicationFeed[entryFilter][categoryAncestorIdIn] (string) - All entries within this categoy or in child categories
* syndicationFeed[entryFilter][redirectFromEntryId] (string) - The id of the original entry
* syndicationFeed[entryFilter][objectType] (string)
* syndicationFeed[entryFilter][lastPlayedAtGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][lastPlayedAtLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][durationLessThan] (integer)
* syndicationFeed[entryFilter][durationGreaterThan] (integer)
* syndicationFeed[entryFilter][durationLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][durationGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][durationTypeMatchOr] (string)
* syndicationFeed[entryFilter][documentTypeEqual] (integer) - Enum Type: `KalturaDocumentType`
* syndicationFeed[entryFilter][documentTypeIn] (string)
* syndicationFeed[entryFilter][assetParamsIdsMatchOr] (string)
* syndicationFeed[entryFilter][assetParamsIdsMatchAnd] (string)
* syndicationFeed[entryFilter][mediaTypeEqual] (integer) - Enum Type: `KalturaMediaType`
* syndicationFeed[entryFilter][mediaTypeIn] (string)
* syndicationFeed[entryFilter][sourceTypeEqual] (string) - Enum Type: `KalturaSourceType`
* syndicationFeed[entryFilter][sourceTypeNotEqual] (string) - Enum Type: `KalturaSourceType`
* syndicationFeed[entryFilter][sourceTypeIn] (string)
* syndicationFeed[entryFilter][sourceTypeNotIn] (string)
* syndicationFeed[entryFilter][mediaDateGreaterThanOrEqual] (integer)
* syndicationFeed[entryFilter][mediaDateLessThanOrEqual] (integer)
* syndicationFeed[entryFilter][flavorParamsIdsMatchOr] (string)
* syndicationFeed[entryFilter][flavorParamsIdsMatchAnd] (string)
* syndicationFeed[entryFilter][limit] (integer)
* syndicationFeed[entryFilter][externalSourceTypeEqual] (string) - Enum Type: `KalturaExternalMediaSourceType`
* syndicationFeed[entryFilter][externalSourceTypeIn] (string)
* syndicationFeed[entryFilter][isLive] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[entryFilter][isRecordedEntryIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[entryFilter][hasMediaServerHostname] (string)
* syndicationFeed[adultContent] (string) - Enum Type: `KalturaGoogleSyndicationFeedAdultValues`
* syndicationFeed[language] (string) - feed language
* syndicationFeed[ownerName] (string) - author/publisher name
* syndicationFeed[ownerEmail] (string) - publisher email
* syndicationFeed[feedImageUrl] (string) - podcast thumbnail
* syndicationFeed[feedAuthor] (string)
* syndicationFeed[enforceOrder] (integer) - Enum Type: `KalturaNullableBoolean`
* syndicationFeed[xslt] (string)
* syndicationFeed[itemXpathsToExtend] (array)

### system.getTime



```js
kaltura.system.getTime({}, context)
```


### system.getVersion



```js
kaltura.system.getVersion({}, context)
```


### system.ping



```js
kaltura.system.ping({}, context)
```


### system.pingDatabase



```js
kaltura.system.pingDatabase({}, context)
```


### tag.deletePending
Action goes over all tags with instanceCount==0 and checks whether they need to be removed from the DB. Returns number of removed tags.


```js
kaltura.tag.deletePending({}, context)
```


### tag.indexCategoryEntryTags



```js
kaltura.tag.indexCategoryEntryTags({
  "categoryId": 0,
  "pcToDecrement": "",
  "pcToIncrement": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* categoryId (integer) **required**
* pcToDecrement (string) **required**
* pcToIncrement (string) **required**

### tag.search



```js
kaltura.tag.search({}, context)
```


### thumbAsset.add
Add thumbnail asset


```js
kaltura.thumbAsset.add({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* thumbAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* thumbAsset[fileExt] (string) - `insertOnly`
* thumbAsset[partnerData] (string) - Partner private data
* thumbAsset[partnerDescription] (string) - Partner friendly description
* thumbAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* thumbAsset[thumbParamsId] (integer) - `insertOnly`
* thumbAsset[objectType] (string)
* thumbAsset[cuePointId] (string) - `insertOnly`

### thumbAsset.addFromImage



```js
kaltura.thumbAsset.addFromImage({
  "entryId": "",
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* fileData (string) **required**

### thumbAsset.addFromUrl



```js
kaltura.thumbAsset.addFromUrl({
  "entryId": "",
  "url": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* url (string) **required**

### thumbAsset.delete



```js
kaltura.thumbAsset.delete({
  "thumbAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* thumbAssetId (string) **required**

### thumbAsset.export
manually export an asset


```js
kaltura.thumbAsset.export({
  "assetId": "",
  "storageProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* assetId (string) **required**
* storageProfileId (integer) **required**

### thumbAsset.generate



```js
kaltura.thumbAsset.generate({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* thumbParams[partnerId] (integer)
* thumbParams[name] (string) - The name of the Flavor Params
* thumbParams[systemName] (string) - System name of the Flavor Params
* thumbParams[description] (string) - The description of the Flavor Params
* thumbParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* thumbParams[requiredPermissions] (array)
* thumbParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* thumbParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* thumbParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* thumbParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* thumbParams[cropType] (integer) - Enum Type: `KalturaThumbCropType`
* thumbParams[quality] (integer)
* thumbParams[cropX] (integer)
* thumbParams[cropY] (integer)
* thumbParams[cropWidth] (integer)
* thumbParams[cropHeight] (integer)
* thumbParams[videoOffset] (number)
* thumbParams[width] (integer)
* thumbParams[height] (integer)
* thumbParams[scaleWidth] (number)
* thumbParams[scaleHeight] (number)
* thumbParams[backgroundColor] (string) - Hexadecimal value
* thumbParams[sourceParamsId] (integer) - Id of the flavor params or the thumbnail params to be used as source for the thumbnail creation
* thumbParams[format] (string) - Enum Type: `KalturaContainerFormat`
* thumbParams[density] (integer) - The image density (dpi) for example: 72 or 96
* thumbParams[stripProfiles] (boolean) - Strip profiles and comments
* thumbParams[videoOffsetInPercentage] (integer) - Create thumbnail from the videoLengthpercentage second
* thumbParams[objectType] (string)
* thumbParams[thumbParamsId] (integer)
* thumbParams[thumbParamsVersion] (string)
* thumbParams[thumbAssetId] (string)
* thumbParams[thumbAssetVersion] (string)
* thumbParams[rotate] (integer)
* sourceAssetId (string) - id of the source asset (flavor or thumbnail) to be used as source for the thumbnail generation

### thumbAsset.generateByEntryId



```js
kaltura.thumbAsset.generateByEntryId({
  "entryId": "",
  "destThumbParamsId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* destThumbParamsId (integer) **required** - indicate the id of the ThumbParams to be generate this thumbnail by

### thumbAsset.get



```js
kaltura.thumbAsset.get({
  "thumbAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* thumbAssetId (string) **required**

### thumbAsset.getByEntryId



```js
kaltura.thumbAsset.getByEntryId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**

### thumbAsset.getRemotePaths
Get remote storage existing paths for the asset


```js
kaltura.thumbAsset.getRemotePaths({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### thumbAsset.getUrl
Get download URL for the asset


```js
kaltura.thumbAsset.getUrl({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* storageId (integer)
* thumbParams[partnerId] (integer)
* thumbParams[name] (string) - The name of the Flavor Params
* thumbParams[systemName] (string) - System name of the Flavor Params
* thumbParams[description] (string) - The description of the Flavor Params
* thumbParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* thumbParams[requiredPermissions] (array)
* thumbParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* thumbParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* thumbParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* thumbParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* thumbParams[cropType] (integer) - Enum Type: `KalturaThumbCropType`
* thumbParams[quality] (integer)
* thumbParams[cropX] (integer)
* thumbParams[cropY] (integer)
* thumbParams[cropWidth] (integer)
* thumbParams[cropHeight] (integer)
* thumbParams[videoOffset] (number)
* thumbParams[width] (integer)
* thumbParams[height] (integer)
* thumbParams[scaleWidth] (number)
* thumbParams[scaleHeight] (number)
* thumbParams[backgroundColor] (string) - Hexadecimal value
* thumbParams[sourceParamsId] (integer) - Id of the flavor params or the thumbnail params to be used as source for the thumbnail creation
* thumbParams[format] (string) - Enum Type: `KalturaContainerFormat`
* thumbParams[density] (integer) - The image density (dpi) for example: 72 or 96
* thumbParams[stripProfiles] (boolean) - Strip profiles and comments
* thumbParams[videoOffsetInPercentage] (integer) - Create thumbnail from the videoLengthpercentage second
* thumbParams[objectType] (string)
* thumbParams[thumbParamsId] (integer)
* thumbParams[thumbParamsVersion] (string)
* thumbParams[thumbAssetId] (string)
* thumbParams[thumbAssetVersion] (string)
* thumbParams[rotate] (integer)

### thumbAsset.list
List Thumbnail Assets by filter and pager


```js
kaltura.thumbAsset.list({}, context)
```


### thumbAsset.regenerate



```js
kaltura.thumbAsset.regenerate({
  "thumbAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* thumbAssetId (string) **required**

### thumbAsset.serve
Serves thumbnail by its id


```js
kaltura.thumbAsset.serve({
  "thumbAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* thumbAssetId (string) **required**
* version (integer)
* thumbParams[partnerId] (integer)
* thumbParams[name] (string) - The name of the Flavor Params
* thumbParams[systemName] (string) - System name of the Flavor Params
* thumbParams[description] (string) - The description of the Flavor Params
* thumbParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* thumbParams[requiredPermissions] (array)
* thumbParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* thumbParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* thumbParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* thumbParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* thumbParams[cropType] (integer) - Enum Type: `KalturaThumbCropType`
* thumbParams[quality] (integer)
* thumbParams[cropX] (integer)
* thumbParams[cropY] (integer)
* thumbParams[cropWidth] (integer)
* thumbParams[cropHeight] (integer)
* thumbParams[videoOffset] (number)
* thumbParams[width] (integer)
* thumbParams[height] (integer)
* thumbParams[scaleWidth] (number)
* thumbParams[scaleHeight] (number)
* thumbParams[backgroundColor] (string) - Hexadecimal value
* thumbParams[sourceParamsId] (integer) - Id of the flavor params or the thumbnail params to be used as source for the thumbnail creation
* thumbParams[format] (string) - Enum Type: `KalturaContainerFormat`
* thumbParams[density] (integer) - The image density (dpi) for example: 72 or 96
* thumbParams[stripProfiles] (boolean) - Strip profiles and comments
* thumbParams[videoOffsetInPercentage] (integer) - Create thumbnail from the videoLengthpercentage second
* thumbParams[objectType] (string)
* thumbParams[thumbParamsId] (integer)
* thumbParams[thumbParamsVersion] (string)
* thumbParams[thumbAssetId] (string)
* thumbParams[thumbAssetVersion] (string)
* thumbParams[rotate] (integer)
* options[download] (boolean)
* options[referrer] (string)

### thumbAsset.serveByEntryId
Serves thumbnail by entry id and thumnail params id


```js
kaltura.thumbAsset.serveByEntryId({
  "entryId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryId (string) **required**
* thumbParamId (integer) - if not set, default thumbnail will be used.

### thumbAsset.setAsDefault
Tags the thumbnail as DEFAULT_THUMB and removes that tag from all other thumbnail assets of the entry.

Create a new file sync link on the entry thumbnail that points to the thumbnail asset file sync.


```js
kaltura.thumbAsset.setAsDefault({
  "thumbAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* thumbAssetId (string) **required**

### thumbAsset.setContent
Update content of thumbnail asset


```js
kaltura.thumbAsset.setContent({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* contentResource[objectType] (string)
* contentResource[url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[forceAsyncDownload] (boolean) - Force Import Job
* contentResource[assetId] (string) - ID of the source asset
* contentResource[entryId] (string) - ID of the source entry
* contentResource[flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[objectId] (string) - The object id of the file sync object
* contentResource[version] (string) - The version of the file sync object
* contentResource[resource][objectType] (string)
* contentResource[resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][assetId] (string) - ID of the source asset
* contentResource[resource][entryId] (string) - ID of the source entry
* contentResource[resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][objectType] (string)
* contentResource[resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][objectType] (string)
* contentResource[resource][resource][resource][url] (string) - Remote URL, FTP, HTTP or HTTPS
* contentResource[resource][resource][resource][forceAsyncDownload] (boolean) - Force Import Job
* contentResource[resource][resource][resource][assetId] (string) - ID of the source asset
* contentResource[resource][resource][resource][entryId] (string) - ID of the source entry
* contentResource[resource][resource][resource][flavorParamsId] (integer) - ID of the source flavor params, set to null to use the source flavor
* contentResource[resource][resource][resource][fileSyncObjectType] (integer) - The object type of the file sync object
* contentResource[resource][resource][resource][objectSubType] (integer) - The object sub-type of the file sync object
* contentResource[resource][resource][resource][objectId] (string) - The object id of the file sync object
* contentResource[resource][resource][resource][version] (string) - The version of the file sync object
* contentResource[resource][resource][resource][resources] (array)
* contentResource[resource][resource][resource][content] (string) - Textual content
* contentResource[resource][resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resource][resources] (array)
* contentResource[resource][resource][content] (string) - Textual content
* contentResource[resource][resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][resource][privateKey] (string) - SSH private key
* contentResource[resource][resource][publicKey] (string) - SSH public key
* contentResource[resource][resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resource][resources] (array)
* contentResource[resource][content] (string) - Textual content
* contentResource[resource][storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[resource][privateKey] (string) - SSH private key
* contentResource[resource][publicKey] (string) - SSH public key
* contentResource[resource][keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[resource][dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[resource][localFilePath] (string) - Full path to the local file
* contentResource[resource][keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[resource][fileData] (string) - Represents the $_FILE
* contentResource[resource][token] (string) - Token that returned from upload.upload action or uploadToken.add action.
* contentResource[resources] (array)
* contentResource[content] (string) - Textual content
* contentResource[storageProfileId] (integer) - ID of storage profile to be associated with the created file sync, used for file serving URL composing.
* contentResource[privateKey] (string) - SSH private key
* contentResource[publicKey] (string) - SSH public key
* contentResource[keyPassphrase] (string) - Passphrase for SSH keys
* contentResource[dropFolderFileId] (integer) - Id of the drop folder file object
* contentResource[localFilePath] (string) - Full path to the local file
* contentResource[keepOriginalFile] (boolean) - Should keep original file (false = mv, true = cp)
* contentResource[fileData] (string) - Represents the $_FILE
* contentResource[token] (string) - Token that returned from upload.upload action or uploadToken.add action.

### thumbAsset.update
Update thumbnail asset


```js
kaltura.thumbAsset.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* thumbAsset[tags] (string) - Tags used to identify the Flavor Asset in various scenarios
* thumbAsset[fileExt] (string) - `insertOnly`
* thumbAsset[partnerData] (string) - Partner private data
* thumbAsset[partnerDescription] (string) - Partner friendly description
* thumbAsset[actualSourceAssetParamsIds] (string) - Comma separated list of source flavor params ids
* thumbAsset[thumbParamsId] (integer) - `insertOnly`
* thumbAsset[objectType] (string)
* thumbAsset[cuePointId] (string) - `insertOnly`

### thumbParams.add
Add new Thumb Params


```js
kaltura.thumbParams.add({}, context)
```


### thumbParams.delete
Delete Thumb Params by ID


```js
kaltura.thumbParams.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### thumbParams.get
Get Thumb Params by ID


```js
kaltura.thumbParams.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### thumbParams.getByConversionProfileId
Get Thumb Params by Conversion Profile ID


```js
kaltura.thumbParams.getByConversionProfileId({
  "conversionProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* conversionProfileId (integer) **required**

### thumbParams.list
List Thumb Params by filter with paging support (By default - all system default params will be listed too)


```js
kaltura.thumbParams.list({}, context)
```


### thumbParams.update
Update Thumb Params by ID


```js
kaltura.thumbParams.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* thumbParams[partnerId] (integer)
* thumbParams[name] (string) - The name of the Flavor Params
* thumbParams[systemName] (string) - System name of the Flavor Params
* thumbParams[description] (string) - The description of the Flavor Params
* thumbParams[tags] (string) - The Flavor Params tags are used to identify the flavor for different usage (e.g. web, hd, mobile)
* thumbParams[requiredPermissions] (array)
* thumbParams[sourceRemoteStorageProfileId] (integer) - Id of remote storage profile that used to get the source, zero indicates Kaltura data center
* thumbParams[remoteStorageProfileIds] (integer) - Comma seperated ids of remote storage profiles that the flavor distributed to, the distribution done by the conversion engine
* thumbParams[mediaParserType] (string) - Enum Type: `KalturaMediaParserType`
* thumbParams[sourceAssetParamsIds] (string) - Comma seperated ids of source flavor params this flavor is created from
* thumbParams[cropType] (integer) - Enum Type: `KalturaThumbCropType`
* thumbParams[quality] (integer)
* thumbParams[cropX] (integer)
* thumbParams[cropY] (integer)
* thumbParams[cropWidth] (integer)
* thumbParams[cropHeight] (integer)
* thumbParams[videoOffset] (number)
* thumbParams[width] (integer)
* thumbParams[height] (integer)
* thumbParams[scaleWidth] (number)
* thumbParams[scaleHeight] (number)
* thumbParams[backgroundColor] (string) - Hexadecimal value
* thumbParams[sourceParamsId] (integer) - Id of the flavor params or the thumbnail params to be used as source for the thumbnail creation
* thumbParams[format] (string) - Enum Type: `KalturaContainerFormat`
* thumbParams[density] (integer) - The image density (dpi) for example: 72 or 96
* thumbParams[stripProfiles] (boolean) - Strip profiles and comments
* thumbParams[videoOffsetInPercentage] (integer) - Create thumbnail from the videoLengthpercentage second
* thumbParams[objectType] (string)
* thumbParams[thumbParamsId] (integer)
* thumbParams[thumbParamsVersion] (string)
* thumbParams[thumbAssetId] (string)
* thumbParams[thumbAssetVersion] (string)
* thumbParams[rotate] (integer)

### thumbParamsOutput.get
Get thumb params output object by ID


```js
kaltura.thumbParamsOutput.get({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### thumbParamsOutput.list
List thumb params output objects by filter and pager


```js
kaltura.thumbParamsOutput.list({}, context)
```


### timeWarner.getFeed



```js
kaltura.timeWarner.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### tvCom.getFeed



```js
kaltura.tvCom.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### uiConf.add
UIConf Add action allows you to add a UIConf to Kaltura DB


```js
kaltura.uiConf.add({}, context)
```


### uiConf.clone
Clone an existing UIConf


```js
kaltura.uiConf.clone({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### uiConf.delete
Delete an existing UIConf


```js
kaltura.uiConf.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### uiConf.get
Retrieve a UIConf by id


```js
kaltura.uiConf.get({
  "id": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* id (integer) **required**

### uiConf.getAvailableTypes
Retrieve a list of all available versions by object type


```js
kaltura.uiConf.getAvailableTypes({}, context)
```


### uiConf.list
Retrieve a list of available UIConfs


```js
kaltura.uiConf.list({}, context)
```


### uiConf.listTemplates
retrieve a list of available template UIConfs


```js
kaltura.uiConf.listTemplates({}, context)
```


### uiConf.update
Update an existing UIConf


```js
kaltura.uiConf.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* uiConf[name] (string) - Name of the uiConf, this is not a primary key
* uiConf[description] (string)
* uiConf[objType] (integer) - Enum Type: `KalturaUiConfObjType`
* uiConf[width] (integer)
* uiConf[height] (integer)
* uiConf[htmlParams] (string)
* uiConf[swfUrl] (string)
* uiConf[confFile] (string)
* uiConf[confFileFeatures] (string)
* uiConf[config] (string)
* uiConf[confVars] (string)
* uiConf[useCdn] (boolean)
* uiConf[tags] (string)
* uiConf[swfUrlVersion] (string)
* uiConf[creationMode] (integer) - Enum Type: `KalturaUiConfCreationMode`
* uiConf[html5Url] (string)
* uiConf[partnerTags] (string)

### unicorn.notify



```js
kaltura.unicorn.notify({
  "id": 0
}, context)
```

#### Parameters
* format (integer) - The format of the response
* id (integer) **required** - distribution job id

### upload.getUploadedFileTokenByFileName



```js
kaltura.upload.getUploadedFileTokenByFileName({
  "fileName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileName (string) **required**

### upload.upload



```js
kaltura.upload.upload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required** - The file data

### uploadToken.add
Adds new upload token to upload a file


```js
kaltura.uploadToken.add({}, context)
```


### uploadToken.delete
Deletes the upload token by upload token id


```js
kaltura.uploadToken.delete({
  "uploadTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* uploadTokenId (string) **required**

### uploadToken.get
Get upload token by id


```js
kaltura.uploadToken.get({
  "uploadTokenId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* uploadTokenId (string) **required**

### uploadToken.list
List upload token by filter with pager support. 

When using a user session the service will be restricted to users objects only.


```js
kaltura.uploadToken.list({}, context)
```


### uploadToken.upload
Upload a file using the upload token id, returns an error on failure (an exception will be thrown when using one of the Kaltura clients)

Chunks can be uploaded in parallel and they will be appended according to their resumeAt position.

A parallel upload session should have three stages:

1. A single upload with resume=false and finalChunk=false

2. Parallel upload requests each with resume=true,finalChunk=false and the expected resumetAt position.

If a chunk fails to upload it can be re-uploaded.

3. After all of the chunks have been uploaded a final chunk (can be of zero size) should be uploaded 

with resume=true, finalChunk=true and the expected resumeAt position. In case an UPLOAD_TOKEN_CANNOT_MATCH_EXPECTED_SIZE exception

has been returned (indicating not all of the chunks were appended yet) the final request can be retried.


```js
kaltura.uploadToken.upload({
  "uploadTokenId": "",
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* uploadTokenId (string) **required**
* fileData (string) **required**
* resume (boolean)
* finalChunk (boolean)
* resumeAt (number)

### user.add
Adds a new user to an existing account in the Kaltura database.

Input param $id is the unique identifier in the partner's system.


```js
kaltura.user.add({}, context)
```


### user.addFromBulkUpload



```js
kaltura.user.addFromBulkUpload({
  "fileData": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* fileData (string) **required**
* bulkUploadData[fileName] (string) - Friendly name of the file, used to be recognized later in the logs.
* bulkUploadData[objectData][objectType] (string)
* bulkUploadData[objectData][conversionProfileId] (integer) - Selected profile id for all bulk entries

### user.checkLoginDataExists
Action which checks whther user login


```js
kaltura.user.checkLoginDataExists({}, context)
```


### user.delete
Deletes a user from a partner account.


```js
kaltura.user.delete({
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required** - The user's unique identifier in the partner's system

### user.disableLogin
Disables a user's ability to log into a partner account using an email address and a password.

You may use either a userId or a loginId parameter for this action.


```js
kaltura.user.disableLogin({}, context)
```


### user.enableLogin
Enables a user to log into a partner account using an email address and a password


```js
kaltura.user.enableLogin({
  "userId": "",
  "loginId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required** - The user's unique identifier in the partner's system
* loginId (string) **required** - The user's email address that identifies the user for login
* password (string) - The user's password

### user.get
Retrieves a user object for a specified user ID.


```js
kaltura.user.get({}, context)
```


### user.getByLoginId
Retrieves a user object for a user's login ID and partner ID.

A login ID is the email address used by a user to log into the system.


```js
kaltura.user.getByLoginId({
  "loginId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* loginId (string) **required** - The user's email address that identifies the user for login

### user.index
Index an entry by id.


```js
kaltura.user.index({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* shouldUpdate (boolean)

### user.list
Lists user objects that are associated with an account.

Blocked users are listed unless you use a filter to exclude them.

Deleted users are not listed unless you use a filter to include them.


```js
kaltura.user.list({}, context)
```


### user.login
Logs a user into a partner account with a partner ID, a partner user ID (puser), and a user password.


```js
kaltura.user.login({
  "partnerId": 0,
  "userId": "",
  "password": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* partnerId (integer) **required** - The identifier of the partner account
* userId (string) **required** - The user's unique identifier in the partner's system
* password (string) **required** - The user's password
* expiry (integer) - The requested time (in seconds) before the generated KS expires (By default, a KS expires after 24 hours).
* privileges (string) - Special privileges

### user.loginByLoginId
Logs a user into a partner account with a user login ID and a user password.


```js
kaltura.user.loginByLoginId({
  "loginId": "",
  "password": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* loginId (string) **required** - The user's email address that identifies the user for login
* password (string) **required** - The user's password
* partnerId (integer) - The identifier of the partner account
* expiry (integer) - The requested time (in seconds) before the generated KS expires (By default, a KS expires after 24 hours).
* privileges (string) - Special privileges
* otp (string) - the user's one-time password

### user.notifyBan
Notifies that a user is banned from an account.


```js
kaltura.user.notifyBan({
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required** - The user's unique identifier in the partner's system

### user.resetPassword
Reset user's password and send the user an email to generate a new one.


```js
kaltura.user.resetPassword({
  "email": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* email (string) **required** - The user's email address (login email)

### user.setInitialPassword
Set initial users password


```js
kaltura.user.setInitialPassword({
  "hashKey": "",
  "newPassword": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* hashKey (string) **required** - The hash key used to identify the user (retrieved by email)
* newPassword (string) **required** - The new password to set for the user

### user.update
Updates an existing user object.

You can also use this action to update the userId.


```js
kaltura.user.update({
  "userId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userId (string) **required** - The user's unique identifier in the partner's system
* user[id] (string)
* user[type] (integer) - Enum Type: `KalturaUserType`
* user[screenName] (string)
* user[fullName] (string)
* user[email] (string)
* user[dateOfBirth] (integer)
* user[country] (string)
* user[state] (string)
* user[city] (string)
* user[zip] (string)
* user[thumbnailUrl] (string)
* user[description] (string)
* user[tags] (string)
* user[adminTags] (string) - Admin tags can be updated only by using an admin session
* user[gender] (integer) - Enum Type: `KalturaGender`
* user[status] (integer) - Enum Type: `KalturaUserStatus`
* user[partnerData] (string) - Can be used to store various partner related data as a string
* user[indexedPartnerDataInt] (integer)
* user[indexedPartnerDataString] (string)
* user[password] (string) - `insertOnly` `writeOnly`
* user[firstName] (string)
* user[lastName] (string)
* user[isAdmin] (boolean)
* user[language] (string) - Enum Type: `KalturaLanguageCode`
* user[roleIds] (string)
* user[allowedPartnerIds] (string)
* user[allowedPartnerPackages] (string)
* user[objectType] (string)

### user.updateLoginData
Updates a user's login data: email, password, name.


```js
kaltura.user.updateLoginData({
  "oldLoginId": "",
  "password": ""
}, context)
```

#### Parameters
* format (integer) - The format of the response
* oldLoginId (string) **required** - The user's current email address that identified the user for login
* password (string) **required** - The user's current email address that identified the user for login
* newLoginId (string) - Optional, The user's email address that will identify the user for login
* newPassword (string) - Optional, The user's new password
* newFirstName (string) - Optional, The user's new first name
* newLastName (string) - Optional, The user's new last name

### userEntry.add
Adds a user_entry to the Kaltura DB.


```js
kaltura.userEntry.add({}, context)
```


### userEntry.bulkDelete



```js
kaltura.userEntry.bulkDelete({}, context)
```


### userEntry.delete



```js
kaltura.userEntry.delete({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### userEntry.get



```js
kaltura.userEntry.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### userEntry.list



```js
kaltura.userEntry.list({}, context)
```


### userEntry.submitQuiz
Submits the quiz so that it's status will be submitted and calculates the score for the quiz


```js
kaltura.userEntry.submitQuiz({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**

### userEntry.update



```js
kaltura.userEntry.update({
  "id": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* userEntry[entryId] (string) - `insertOnly`
* userEntry[userId] (string) - `insertOnly`
* userEntry[extendedStatus] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* userEntry[objectType] (string)
* userEntry[playbackContext] (string) - Playback context
* userEntry[lastTimeReached] (integer) - Last playback time reached by user
* userEntry[lastUpdateTime] (integer)

### userRole.add
Adds a new user role object to the account.


```js
kaltura.userRole.add({}, context)
```


### userRole.clone
Creates a new user role object that is a duplicate of an existing role.


```js
kaltura.userRole.clone({
  "userRoleId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userRoleId (integer) **required** - The user role's unique identifier

### userRole.delete
Deletes an existing user role object.


```js
kaltura.userRole.delete({
  "userRoleId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userRoleId (integer) **required** - The user role's unique identifier

### userRole.get
Retrieves a user role object using its ID.


```js
kaltura.userRole.get({
  "userRoleId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userRoleId (integer) **required** - The user role's unique identifier

### userRole.list
Lists user role objects that are associated with an account.

Blocked user roles are listed unless you use a filter to exclude them.

Deleted user roles are not listed unless you use a filter to include them.


```js
kaltura.userRole.list({}, context)
```


### userRole.update
Updates an existing user role object.


```js
kaltura.userRole.update({
  "userRoleId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* userRoleId (integer) **required** - The user role's unique identifier
* userRole[name] (string)
* userRole[systemName] (string)
* userRole[description] (string)
* userRole[status] (integer) - Enum Type: `KalturaUserRoleStatus`
* userRole[permissionNames] (string)
* userRole[tags] (string)

### uverseClickToOrder.getFeed



```js
kaltura.uverseClickToOrder.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### uverse.getFeed



```js
kaltura.uverse.getFeed({
  "distributionProfileId": 0,
  "hash": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* distributionProfileId (integer) **required**
* hash (string) **required**

### varConsole.getPartnerUsage
Function which calulates partner usage of a group of a VAR's sub-publishers


```js
kaltura.varConsole.getPartnerUsage({}, context)
```


### varConsole.updateStatus
Function to change a sub-publisher's status


```js
kaltura.varConsole.updateStatus({
  "id": 0,
  "status": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (integer) **required**
* status (integer) **required** - Enum Type: `KalturaPartnerStatus`

### virusScanProfile.add
Allows you to add an virus scan profile object and virus scan profile content associated with Kaltura object


```js
kaltura.virusScanProfile.add({}, context)
```


### virusScanProfile.delete
Mark the virus scan profile as deleted


```js
kaltura.virusScanProfile.delete({
  "virusScanProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* virusScanProfileId (integer) **required**

### virusScanProfile.get
Retrieve an virus scan profile object by id


```js
kaltura.virusScanProfile.get({
  "virusScanProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* virusScanProfileId (integer) **required**

### virusScanProfile.list
List virus scan profile objects by filter and pager


```js
kaltura.virusScanProfile.list({}, context)
```


### virusScanProfile.scan
Scan flavor asset according to virus scan profile


```js
kaltura.virusScanProfile.scan({
  "flavorAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* flavorAssetId (string) **required**
* virusScanProfileId (integer)

### virusScanProfile.update
Update exisitng virus scan profile, it is possible to update the virus scan profile id too


```js
kaltura.virusScanProfile.update({
  "virusScanProfileId": 0
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* virusScanProfileId (integer) **required**
* virusScanProfile[name] (string)
* virusScanProfile[status] (integer) - Enum Type: `KalturaVirusScanProfileStatus`
* virusScanProfile[engineType] (string) - Enum Type: `KalturaVirusScanEngineType`
* virusScanProfile[entryFilter][orderBy] (string)
* virusScanProfile[entryFilter][advancedSearch][objectType] (string)
* virusScanProfile[entryFilter][advancedSearch][value] (string)
* virusScanProfile[entryFilter][advancedSearch][categoriesMatchOr] (string)
* virusScanProfile[entryFilter][advancedSearch][categoryEntryStatusIn] (string)
* virusScanProfile[entryFilter][advancedSearch][orderBy] (string) - Enum Type: `KalturaCategoryEntryAdvancedOrderBy`
* virusScanProfile[entryFilter][advancedSearch][categoryIdEqual] (integer)
* virusScanProfile[entryFilter][advancedSearch][memberIdEq] (string)
* virusScanProfile[entryFilter][advancedSearch][memberIdIn] (string)
* virusScanProfile[entryFilter][advancedSearch][memberPermissionsMatchOr] (string)
* virusScanProfile[entryFilter][advancedSearch][memberPermissionsMatchAnd] (string)
* virusScanProfile[entryFilter][advancedSearch][noDistributionProfiles] (boolean)
* virusScanProfile[entryFilter][advancedSearch][distributionProfileId] (integer)
* virusScanProfile[entryFilter][advancedSearch][distributionSunStatus] (integer) - Enum Type: `KalturaEntryDistributionSunStatus`
* virusScanProfile[entryFilter][advancedSearch][entryDistributionFlag] (integer) - Enum Type: `KalturaEntryDistributionFlag`
* virusScanProfile[entryFilter][advancedSearch][entryDistributionStatus] (integer) - Enum Type: `KalturaEntryDistributionStatus`
* virusScanProfile[entryFilter][advancedSearch][hasEntryDistributionValidationErrors] (boolean)
* virusScanProfile[entryFilter][advancedSearch][entryDistributionValidationErrors] (string) - Comma seperated validation error types
* virusScanProfile[entryFilter][advancedSearch][contentLike] (string)
* virusScanProfile[entryFilter][advancedSearch][contentMultiLikeOr] (string)
* virusScanProfile[entryFilter][advancedSearch][contentMultiLikeAnd] (string)
* virusScanProfile[entryFilter][advancedSearch][cuePointsFreeText] (string)
* virusScanProfile[entryFilter][advancedSearch][cuePointTypeIn] (string)
* virusScanProfile[entryFilter][advancedSearch][cuePointSubTypeEqual] (integer)
* virusScanProfile[entryFilter][advancedSearch][watermarkId] (integer)
* virusScanProfile[entryFilter][advancedSearch][indexIdGreaterThan] (integer)
* virusScanProfile[entryFilter][advancedSearch][depthGreaterThanEqual] (integer)
* virusScanProfile[entryFilter][advancedSearch][isQuiz] (integer) - Enum Type: `KalturaNullableBoolean`
* virusScanProfile[entryFilter][advancedSearch][field] (string)
* virusScanProfile[entryFilter][advancedSearch][type] (integer) - Enum Type: `KalturaSearchOperatorType`
* virusScanProfile[entryFilter][advancedSearch][items] (array)
* virusScanProfile[entryFilter][advancedSearch][idEqual] (string)
* virusScanProfile[entryFilter][advancedSearch][idIn] (string)
* virusScanProfile[entryFilter][advancedSearch][userIdEqual] (string)
* virusScanProfile[entryFilter][advancedSearch][userIdIn] (string)
* virusScanProfile[entryFilter][advancedSearch][updatedAtGreaterThanOrEqual] (string)
* virusScanProfile[entryFilter][advancedSearch][updatedAtLessThanOrEqual] (string)
* virusScanProfile[entryFilter][advancedSearch][extendedStatusEqual] (string) - Enum Type: `KalturaUserEntryExtendedStatus`
* virusScanProfile[entryFilter][advancedSearch][extendedStatusIn] (string)
* virusScanProfile[entryFilter][advancedSearch][comparison] (string) - Enum Type: `KalturaSearchConditionComparison`
* virusScanProfile[entryFilter][advancedSearch][not] (boolean)
* virusScanProfile[entryFilter][advancedSearch][attribute] (string) - Enum Type: `KalturaBaseEntryCompareAttribute`
* virusScanProfile[entryFilter][advancedSearch][metadataProfileId] (integer)
* virusScanProfile[entryFilter][idEqual] (string) - This filter should be in use for retrieving only a specific entry (identified by its entryId).
* virusScanProfile[entryFilter][idIn] (string) - This filter should be in use for retrieving few specific entries (string should include comma separated list of entryId strings).
* virusScanProfile[entryFilter][idNotIn] (string)
* virusScanProfile[entryFilter][nameLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry names (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][nameMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][nameMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry names, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][nameEqual] (string) - This filter should be in use for retrieving entries with a specific name.
* virusScanProfile[entryFilter][partnerIdEqual] (integer) - This filter should be in use for retrieving only entries which were uploaded by/assigned to users of a specific Kaltura Partner (identified by Partner ID).
* virusScanProfile[entryFilter][partnerIdIn] (string) - This filter should be in use for retrieving only entries within Kaltura network which were uploaded by/assigned to users of few Kaltura Partners  (string should include comma separated list of PartnerIDs)
* virusScanProfile[entryFilter][userIdEqual] (string) - This filter parameter should be in use for retrieving only entries, uploaded by/assigned to a specific user (identified by user Id).
* virusScanProfile[entryFilter][userIdIn] (string)
* virusScanProfile[entryFilter][userIdNotIn] (string)
* virusScanProfile[entryFilter][creatorIdEqual] (string)
* virusScanProfile[entryFilter][tagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][tagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][tagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][adminTagsLike] (string) - This filter should be in use for retrieving specific entries. It should include only one string to search for in entry tags set by an ADMIN user (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][adminTagsMultiLikeOr] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an OR logic to retrieve entries that contain at least one input string (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][adminTagsMultiLikeAnd] (string) - This filter should be in use for retrieving specific entries. It could include few (comma separated) strings for searching in entry tags, set by an ADMIN user, while applying an AND logic to retrieve entries that contain all input strings (no wildcards, spaces are treated as part of the string).
* virusScanProfile[entryFilter][categoriesMatchAnd] (string)
* virusScanProfile[entryFilter][categoriesMatchOr] (string) - All entries within these categories or their child categories.
* virusScanProfile[entryFilter][categoriesNotContains] (string)
* virusScanProfile[entryFilter][categoriesIdsMatchAnd] (string)
* virusScanProfile[entryFilter][categoriesIdsMatchOr] (string) - All entries of the categories, excluding their child categories.
* virusScanProfile[entryFilter][categoriesIdsNotContains] (string)
* virusScanProfile[entryFilter][categoriesIdsEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* virusScanProfile[entryFilter][statusEqual] (string) - Enum Type: `KalturaEntryStatus`
* virusScanProfile[entryFilter][statusNotEqual] (string) - Enum Type: `KalturaEntryStatus`
* virusScanProfile[entryFilter][statusIn] (string) - This filter should be in use for retrieving only entries, at few specific {
* virusScanProfile[entryFilter][statusNotIn] (string) - This filter should be in use for retrieving only entries, not at few specific {
* virusScanProfile[entryFilter][moderationStatusEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* virusScanProfile[entryFilter][moderationStatusNotEqual] (integer) - Enum Type: `KalturaEntryModerationStatus`
* virusScanProfile[entryFilter][moderationStatusIn] (string)
* virusScanProfile[entryFilter][moderationStatusNotIn] (string)
* virusScanProfile[entryFilter][typeEqual] (string) - Enum Type: `KalturaEntryType`
* virusScanProfile[entryFilter][typeIn] (string) - This filter should be in use for retrieving entries of few {
* virusScanProfile[entryFilter][createdAtGreaterThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system after a specific time/date (standard timestamp format).
* virusScanProfile[entryFilter][createdAtLessThanOrEqual] (integer) - This filter parameter should be in use for retrieving only entries which were created at Kaltura system before a specific time/date (standard timestamp format).
* virusScanProfile[entryFilter][updatedAtGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][updatedAtLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][totalRankLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][totalRankGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][groupIdEqual] (integer)
* virusScanProfile[entryFilter][searchTextMatchAnd] (string) - This filter should be in use for retrieving specific entries while search match the input string within all of the following metadata attributes: name, description, tags, adminTags.
* virusScanProfile[entryFilter][searchTextMatchOr] (string) - This filter should be in use for retrieving specific entries while search match the input string within at least one of the following metadata attributes: name, description, tags, adminTags.
* virusScanProfile[entryFilter][accessControlIdEqual] (integer)
* virusScanProfile[entryFilter][accessControlIdIn] (string)
* virusScanProfile[entryFilter][startDateGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][startDateLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][startDateGreaterThanOrEqualOrNull] (integer)
* virusScanProfile[entryFilter][startDateLessThanOrEqualOrNull] (integer)
* virusScanProfile[entryFilter][endDateGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][endDateLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][endDateGreaterThanOrEqualOrNull] (integer)
* virusScanProfile[entryFilter][endDateLessThanOrEqualOrNull] (integer)
* virusScanProfile[entryFilter][referenceIdEqual] (string)
* virusScanProfile[entryFilter][referenceIdIn] (string)
* virusScanProfile[entryFilter][replacingEntryIdEqual] (string)
* virusScanProfile[entryFilter][replacingEntryIdIn] (string)
* virusScanProfile[entryFilter][replacedEntryIdEqual] (string)
* virusScanProfile[entryFilter][replacedEntryIdIn] (string)
* virusScanProfile[entryFilter][replacementStatusEqual] (string) - Enum Type: `KalturaEntryReplacementStatus`
* virusScanProfile[entryFilter][replacementStatusIn] (string)
* virusScanProfile[entryFilter][partnerSortValueGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][partnerSortValueLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][rootEntryIdEqual] (string)
* virusScanProfile[entryFilter][rootEntryIdIn] (string)
* virusScanProfile[entryFilter][parentEntryIdEqual] (string)
* virusScanProfile[entryFilter][entitledUsersEditMatchAnd] (string)
* virusScanProfile[entryFilter][entitledUsersEditMatchOr] (string)
* virusScanProfile[entryFilter][entitledUsersPublishMatchAnd] (string)
* virusScanProfile[entryFilter][entitledUsersPublishMatchOr] (string)
* virusScanProfile[entryFilter][tagsNameMultiLikeOr] (string)
* virusScanProfile[entryFilter][tagsAdminTagsMultiLikeOr] (string)
* virusScanProfile[entryFilter][tagsAdminTagsNameMultiLikeOr] (string)
* virusScanProfile[entryFilter][tagsNameMultiLikeAnd] (string)
* virusScanProfile[entryFilter][tagsAdminTagsMultiLikeAnd] (string)
* virusScanProfile[entryFilter][tagsAdminTagsNameMultiLikeAnd] (string)
* virusScanProfile[entryFilter][freeText] (string)
* virusScanProfile[entryFilter][isRoot] (integer) - Enum Type: `KalturaNullableBoolean`
* virusScanProfile[entryFilter][categoriesFullNameIn] (string)
* virusScanProfile[entryFilter][categoryAncestorIdIn] (string) - All entries within this categoy or in child categories
* virusScanProfile[entryFilter][redirectFromEntryId] (string) - The id of the original entry
* virusScanProfile[entryFilter][objectType] (string)
* virusScanProfile[entryFilter][lastPlayedAtGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][lastPlayedAtLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][durationLessThan] (integer)
* virusScanProfile[entryFilter][durationGreaterThan] (integer)
* virusScanProfile[entryFilter][durationLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][durationGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][durationTypeMatchOr] (string)
* virusScanProfile[entryFilter][documentTypeEqual] (integer) - Enum Type: `KalturaDocumentType`
* virusScanProfile[entryFilter][documentTypeIn] (string)
* virusScanProfile[entryFilter][assetParamsIdsMatchOr] (string)
* virusScanProfile[entryFilter][assetParamsIdsMatchAnd] (string)
* virusScanProfile[entryFilter][mediaTypeEqual] (integer) - Enum Type: `KalturaMediaType`
* virusScanProfile[entryFilter][mediaTypeIn] (string)
* virusScanProfile[entryFilter][sourceTypeEqual] (string) - Enum Type: `KalturaSourceType`
* virusScanProfile[entryFilter][sourceTypeNotEqual] (string) - Enum Type: `KalturaSourceType`
* virusScanProfile[entryFilter][sourceTypeIn] (string)
* virusScanProfile[entryFilter][sourceTypeNotIn] (string)
* virusScanProfile[entryFilter][mediaDateGreaterThanOrEqual] (integer)
* virusScanProfile[entryFilter][mediaDateLessThanOrEqual] (integer)
* virusScanProfile[entryFilter][flavorParamsIdsMatchOr] (string)
* virusScanProfile[entryFilter][flavorParamsIdsMatchAnd] (string)
* virusScanProfile[entryFilter][limit] (integer)
* virusScanProfile[entryFilter][externalSourceTypeEqual] (string) - Enum Type: `KalturaExternalMediaSourceType`
* virusScanProfile[entryFilter][externalSourceTypeIn] (string)
* virusScanProfile[entryFilter][isLive] (integer) - Enum Type: `KalturaNullableBoolean`
* virusScanProfile[entryFilter][isRecordedEntryIdEmpty] (integer) - Enum Type: `KalturaNullableBoolean`
* virusScanProfile[entryFilter][hasMediaServerHostname] (string)

### widevineDrm.getLicense
Get license for encrypted content playback


```js
kaltura.widevineDrm.getLicense({
  "flavorAssetId": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* flavorAssetId (string) **required**
* referrer (string) - 64base encoded

### widget.add
Add new widget, can be attached to entry or kshow

SourceWidget is ignored.


```js
kaltura.widget.add({}, context)
```


### widget.clone
Add widget based on existing widget.

Must provide valid sourceWidgetId


```js
kaltura.widget.clone({}, context)
```


### widget.get
Get widget by id


```js
kaltura.widget.get({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**

### widget.list
Retrieve a list of available widget depends on the filter given


```js
kaltura.widget.list({}, context)
```


### widget.update
Update exisiting widget


```js
kaltura.widget.update({
  "id": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* id (string) **required**
* widget[sourceWidgetId] (string)
* widget[entryId] (string)
* widget[uiConfId] (integer)
* widget[securityType] (integer) - Enum Type: `KalturaWidgetSecurityType`
* widget[securityPolicy] (integer)
* widget[partnerData] (string) - Can be used to store various partner related data as a string
* widget[enforceEntitlement] (boolean) - Should enforce entitlement on feed entries
* widget[privacyContext] (string) - Set privacy context for search entries that assiged to private and public categories within a category privacy context.
* widget[addEmbedHtml5Support] (boolean) - Addes the HTML5 script line to the widget's embed code
* widget[roles] (string)

### liveConversionProfile.serve
Serve XML rendition of the Kaltura Live Transcoding Profile usable by the Wowza transcoding add-on


```js
kaltura.liveConversionProfile.serve({
  "streamName": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* streamName (string) **required** - the id of the live entry with it's stream suffix
* hostname (string) - the media server host name
* extraParams (string) - is a json object containing the stream parameters transfered by the encoder

### xInternal.xAddBulkDownload
Creates new download job for multiple entry ids (comma separated), an email will be sent when the job is done

This sevice support the following entries: 

- MediaEntry

- Video will be converted using the flavor params id

- Audio will be downloaded as MP3

- Image will be downloaded as Jpeg

- MixEntry will be flattened using the flavor params id

- Other entry types are not supported

Returns the admin email that the email message will be sent to


```js
kaltura.xInternal.xAddBulkDownload({
  "entryIds": ""
}, context)
```

#### Parameters
* ks (string)
* format (integer) - The format of the response
* entryIds (string) **required** - Comma separated list of entry ids
* flavorParamsId (string)
