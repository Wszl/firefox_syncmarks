# SyncMarks (Chrome)
This is a Webextension for Google Chrome to share your bookmarks across WebDAV Shares or a PHP Backend. This is Extension is migrated from the Firefox Extension. It should be compatible to that Extension and the Backends. However, since i didn't use Chrome, i have never fully tested this. Currently the extension is not available in the Chrome Store, because I don't use Chrome and therefore have no use for it. But maybe this will change in the future. However, the extension can be used and tested via the developer mode (chrome://extensions) as an "unpacked extension".

You can use this plugin to export,import, sync your bookmarks to a WebDAV share of your choice. This works with known solutions like NextCloud, OwnCloud, SabreDAV or any other WebDAV providers. To logon, the most used authentication, http-basic, is supported. Syncing via a [PHP Backend](https://github.com/Offerel/SyncMarks) is also possible.

The bookmarks can be exported manually or optionally fully automatically. There are corresponding options in the addon settings.

The Export/Import process is compatible with Firefox Sync.

The exported bookmarks are also be compatible with the corresponding [Roundcube plugin](https://github.com/Offerel/roundcube_ffbookmarks), so that they can also be used in Roundcube.

### Permissions

There are some permissions needed, so that DAVMarks can work properly.

##### access your data for all sites

The WebDAV share can theoretically be located on any website. Since I don't know beforehand which one this can be, the AddOn needs the permission to store the data on any page. However, the data is only exchanged with the server specified in the settings.

##### read and modify bookmarks

Since you export and import all your bookmarks, the AddOn needs access to them.

##### access browser tabs

This is needed since you can open the settings panel from within the AddOn

##### storage

Here all the settings you specify are saved.

##### notifications

If the AddOn finds some problems or would like to tell you how many bookmarks are imported, this is done with a notification.

##### webRequest

The bookmarks are imported and exported with a webRequest. Only https connections other http-basic-authentications are supported.
