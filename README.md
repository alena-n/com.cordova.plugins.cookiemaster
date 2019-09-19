IMPORTANT: This plugin is no longer maintained. It is possible that some functionality may be deprecated in newer target SDKs.

Cookie Master
==============

Fork of kristianhristov/cordova-cookie-master plugin with additional method to get cookies by domain

## Supported Platforms
* Android
* iOS

## Usage
### Get cookie value
```javascript
cookieMaster.getCookieValue('http://<some host>:<some port>', '<cookie name>', function(data) {
  console.log(data.cookieValue);
}, function(error) {
  if (error) {
    console.log('error: ' + error);
  }
});
```
### Get cookie value by domain and path
You can access a cookie from a special domain. Replace `.domain.com` with a desired value.
```javascript
cookieMaster.getCookieValueByDomainPath('.domain.com', '/', '<cookie name>', function(data) {
  console.log(data.cookieValue);
}, function(error) {
  if (error) {
    console.log('error: ' + error);
  }
});
```
### Set cookie value
```javascript
cookieMaster.setCookieValue('http://<some host>:<some port>', '<cookie name>', '<cookie value>',
    function() {
        console.log('A cookie has been set');
    },
    function(error) {
        console.log('Error setting cookie: '+error);
    });
```
The cookie value should be formatted just like a regular <code>document.cookie</code> value.

### Clear all cookies
```javascript
cookieMaster.clear(
    function() {
    console.log('Cookies have been cleared');
    },
    function() {
        console.log('Cookies could not be cleared');
    });
```

## Limitations
* This version has been tested on Android 4.4 ~ 5.1 devices, iOS 7.1 ~ 9 devices. Experience may vary for different OS versions.


## License
This plugin is distributed under the MIT License.

## Thanks to
This plugin was inspired by the great work on the CookieMonster plugin by @barrettc
