
[![License: CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)


YDigital Media Client Side Libraries
====

This set of libraries makes integration to YDigital Media systems a breeze.


## TagYD (third-party publisher tag)
The third-party publisher tag is a way to easily distribute YDigital Media state of the art creatives to our clients and publishers. It will work for ads that use iframe/JavaScript and improves verification and reporting data. Some benefits of using this kind of tag:

* **For advertisers:** Great insights with easier distribution of YDigital Media state of the art creatives
* **For publishers:** Well documented and easier tag implementation on the publisher side

**Note:** This kind of tag requires a browser with support for JavaScript.


#### Table of Contents
1. [About the tag](#about-the-tag)
2. [Sample tag](#sample-tag)
3. [How to edit the tag](#how-to-edit-the-tag)
4. [Table of data attributes](#table-of-data-attributes)
5. [Full tag example](#full-tag-example)
6. [Tag and macro examples](#tag-and-macro-examples)


#### About the tag
*   **Supported ads:**  The tag works for any ads that use iframe/JavaScript or JavaScript tags.
*   **Tag format:**  The tag uses HTML attributes rather than URL parameters. When the tag fires on your site, the HTML attributes will change into the corresponding parameters in the tag and then return the requested content.
*   **Browser support:**  The browser must support both iframes and JavaScript for the ad to load. The browser must  _always_  support JavaScript for these tags because there is no noscript portion of the tag.



#### Sample tag
You will see `<ins` at the beginning of the tag, and the tag will contain `class='ydads'`.
This simple sample tag includes three attributes: one for the placement (`data-yd-placement`), one for creative format (`data-yd-format`) and one for click tracker (`data-yd-click-tracker`).
```html
<ins class="ydads" style="display:inline"
    data-yd-placement='cHQtMC1mYWN0b3J5dGVzdC0wLTAtdA==.aHR0cHM6Ly92aWJyb2NpbC55ZGlnaXRhbG1lZGlhLmNvbS9zY3JlZW5jbGVhbmVyLw==.Mjk5OS0xMi0zMQ==.'
    data-yd-format='interstitial'
    data-yd-click-tracker='{INSERT_CLICK_MACRO}'>
    <script type="text/javascript" src="//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js"></script>
</ins>
```


#### How to edit the tag
If you want to use ad parameters in the tag, enter them as HTML attributes in the HTML code of the tag.
1.  Find the data attributes you need in the table below;
2.  Add each HTML attribute you need on its own line. This makes it easier to find and edit them in your tag. Only add the HTML attributes.
3.  When the tag fires on your site, its HTML attributes will change into the corresponding parameters and then return the requested content.


#### Table of data attributes

|HTML attribute|Purpose|
|-|-|
|`data-yd-placement`          |YDigital Media placement ID (do not change this value).|
|`data-yd-impression-id`      |This is the publisher impression ID. In case you do not set this value, the tag will automatically generate an impression.|
|`data-yd-impression-tracker` |Third party impression tracker URL. If this is not a valid URL it will be ignored.|
|`data-yd-click-tracker`      |Third party click URL/MACRO. If this is not a valid URL it will be ignored. Check examples below.|
|`data-yd-parameters`         |A JSON string containing a list of custom parameters to add to the creative URL. Example: `{"src": "ydigital"}`.|
|`data-yd-format`             |Can be one of the following values: `interstitial` (default), `ticker` or `banner`.|
|`data-yd-ticker-height`      |Set ticker height. Only applies when `data-yd-format` is `ticker`). Default is `250px`.|
|`data-yd-frame-background`   |Frame background, can be any color (in hexadecimal representation). Default value is transparent.|
|`data-yd-closebtn`           |Tell the tag to show the close button. IMPORTANT: only use if the tag is serving directly in the publisher. Default is `false`.|
|`data-yd-closebtn-position`  |Position of the closed button. Only applies when attribute `data-yd-closebtn` is `true`. Default is `top+10px right+10px`.|
|`data-yd-closebtn-timeout`   |Timeout, in seconds, before showing close button. Only applies when attribute `data-yd-closebtn` is `true`. Default is `0`|
|`data-yd-close-timeout`      |Timeout, in seconds, before the creative is closed. The default is `0` (values <= 0 will be ignored)|
|`data-yd-hide-timeout-layer` |If true, it will hide the close timeout layer. Only applies when attribute `data-yd-hide-timeout-layer` is greater than 0. Default is `false`.|
|`data-yd-audit`              |Whether to include YDigital Media third party auditor pixel. Default is `true`.|
|`data-yd-publisher`          |Publisher ID|


#### Full tag example
```html
<ins class="ydads" style="display:inline"
    data-yd-placement='cHQtMC1mYWN0b3J5dGVzdC0wLTAtdA==.aHR0cHM6Ly92aWJyb2NpbC55ZGlnaXRhbG1lZGlhLmNvbS9zY3JlZW5jbGVhbmVyLw==.Mjk5OS0xMi0zMQ==.'
    data-yd-impression-id=''
    data-yd-impression-tracker=''
    data-yd-click-tracker=''
    data-yd-parameters=''
    data-yd-format='interstitial'
    data-yd-ticker-height='250px'
    data-yd-frame-background='transparent'
    data-yd-closebtn='false'
    data-yd-closebtn-position='top+10px right+10px'
    data-yd-closebtn-timeout='0'
    data-yd-close-timeout='0'
    data-yd-hide-timeout-layer='false'
    data-yd-audit='true'
    data-yd-publisher=''>
    <script type="text/javascript" src="//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js"></script>
</ins>
```


## Tag and macro examples
#### Display and Video 360 (DV360)
* **Before adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker='' 
    data-yd-click-tracker='' 
    data-yd-format='interstitial'> 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```
* **After adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker='' 
    data-yd-click-tracker='${CLICK_URL}' 
    data-yd-format='interstitial' > 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```

#### Xandr (AppNexus)
* **Before adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker='' 
    data-yd-click-tracker='' 
    data-yd-format='interstitial' > 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```
* **After adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker='' 
    data-yd-click-tracker='${CLICK_URL}'
    data-yd-format='interstitial'> 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```

#### Adform
* **Before adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker='' 
    data-yd-click-tracker='' 
    data-yd-format='interstitial'> 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```
* **After adding click macros**
```html
<ins class='ydads' style='display:inline;'
    data-yd-placement='cHQtNzc5NjEtTWlsbGVubml1bVJNMDQyMC03NjgzOC0yLTE=.' 
    data-yd-impression-tracker=''
    data-yd-click-tracker='%%c1;cpdir='
    data-yd-format='interstitial'> 
    <script type='text/javascript' src='//pkg.ydigitalmedia.com/publisher-tag@6/yd-publisher.js'></script>
</ins>
```


## License
#### Attribution-NonCommercial-NoDerivatives 4.0 International
[creativecommons.org/licenses/by-nc-nd/4.0/](https://creativecommons.org/licenses/by-nc-nd/4.0/)
