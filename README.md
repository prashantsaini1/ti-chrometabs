# Titanium Android - Chrome Custom Tabs
Now show the web-content within your app without opening other apps or webview with a nice-matching theme.

* Improve your app's web-experience by utlisign powers of Google Chrome like security, cookies & lifecycle management.
* Match the web-content with your app by giving custom 'Toolbar colors'
* Fade transition animations


![](https://github.com/prashantsaini1/ti-chrometabs/blob/master/sample.png)


## Requirements & Installation
* Ti SDK >= 6.3.0.GA
* [Download latest module version from here](https://github.com/prashantsaini1/ti-chrometabs/tree/master/android/dist)
* Unzip it, put it in your Titanium project modules folder & add module to your tiapp.xml <modules> node.

```
<module platform="android">ti.chrometabs</module>
```


# Methods
1. **openURL()**
* Shows the chrome custom tabs within your app, returns boolean on successfully presenting the custom tab.
* If no browser is available, returns false.
* If more than 1 browsers are available, but none of them is able to handle the custom tabs, then it fallbacks to open the URL in default browser outside the app, else shows a list of all browsers which can show chrome-custom-tabs.

| Argument              | Description           | Info              |
| --------------------- |:--------------------- | :------------------------- |
|  String **url**     | URL to open | mandatory |
|  String **toolbarColor**    |  ActionBar or Toolbar color. Default to colorPrimary value defined in colors.xml | Default black |
|  boolean **showTitle**   | Set false to hide Title of the URL   | Default false |
|  boolean **fadeTransition**    |  set to true to enable fade-in-out transitions for better UX | default false |

```javascript
require("ti.chrometabs").openURL({
	url : 'www.ushyaku.com',		// mandatory
	toolbarColor : '#50a260',		// optional
	showTitle : true,				// optional
	fadeTransition : true			// optional
});
```



## LICENSE
    Copyright (c) 2017 by Prashant Saini

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
