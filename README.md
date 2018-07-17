
[![License: CC BY-NC-ND 4.0](https://licensebuttons.net/l/by-nc-nd/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)


YDigital Media Client Side Libraries
====

This set of libraries makes integration to YDigital Media systems a breeze.



## Publisher Tag
The publisher tag is a way to easily distribute YDigital Media state of the art creatives to our clients and publishers. It will work for ads that use iframe/JavaScript and improves verification and reporting data. Some benefits of using this kind of tag:

* **For advertisers:** Great insights with easier distribution of YDigital Media state of the art creatives
* **For publishers:** Well documented and easier tag implementation on the publisher side

**Note:** This kind of tag requires a browser with support for JavaScript.


#### Table of Contents
1. [About the tag](#about-the-tag)
2. [Sample tag](#sample-tag)
3. [How to edit the tag](#how-to-edit-the-tag)
4. [Table of data attributes](#table-of-data-attributes)
5. [Full tag example](#full-tag-example)



#### About the tag
*   **Supported ads:**  The tag works for any ads that use iframe/JavaScript or JavaScript tags.
*   **Tag format:**  The tag uses HTML attributes rather than URL parameters. When the tag fires on your site, the HTML attributes will change into the corresponding parameters in the tag and then return the requested content.
*   **Browser support:**  The browser must support both iframes and JavaScript for the ad to load. The browser must  _always_  support JavaScript for these tags because there is no noscript portion of the tag.



#### Sample tag
You will see `<ins` at the beginning of the tag, and the tag will contain `class='ydads'`.
This simple sample tag includes three attributes: one for the placement (`data-yd-placement`), one for a custom key-value pairs in JSON formar (`data-yd-parameters`), and one for creative format (`data-yd-format`).
```
<ins class="ydads" style="display:inline"
    data-yd-placement='cHQtMC1mYWN0b3J5dGVzdC0wLTAtVA==.aHR0cHM6Ly9jb3JhbC55ZGlnaXRhbG1lZGlhLmNvbS9jb3Jkb2FubzIwMTgv.'
    data-yd-format='interstitial'
    data-yd-parameters='{"src":"ydigital"}'>
    <script type="text/javascript" src="//cdn.jsdelivr.net/gh/ydigitalmedia/publisher-tag@4.1.0/yd-publisher.js"></script>
</ins>
```



#### How to edit the tag
If you want to use ad parameters in the tag, enter them as HTML attributes in the HTML code of the tag.
1.  Find the data attributes you need in the table below;
2.  Add each HTML attribute you need on its own line. This makes it easier to find and edit them in your tag. Only add the HTML attributes.
3.  When the tag fires on your site, its HTML attributes will change into the corresponding parameters and then return the requested content.



#### Table of data attributes

|HTML attribute               |Purpose                        |
|-----------------------------|-------------------------------|
|`data-yd-placement`          |YDigital Media placement ID, this parameter should not be changed by any means|
|`data-yd-impression-id`      |This is the publisher impression ID. In case you do not set this value, the tag will automatically generate an impression ID.|
|`data-yd-impression-tracker` |Third party impression tracker URL. If this is not a valid URL it will be ignored.|
|`data-yd-click-tracker`      |Third party click tracker URL. If this is not a valid URL it will be ignored.|
|`data-yd-parameters`         |List of custom parameters to add to your LP or click tracker URL on call time.|
|`data-yd-lp`                 |Landing page URL. If this is not a valid URL it will be ignored.|
|`data-yd-format`             |Can be one of the following values: `interstitial` (default) or `banner`. Usually you don't need to set or change this parameter, YDigital Media may set it for you|



#### Full tag example
```
<ins class="ydads" style="display:inline"
    data-yd-placement='cHQtMC1mYWN0b3J5dGVzdC0wLTAtVA==.aHR0cHM6Ly9jb3JhbC55ZGlnaXRhbG1lZGlhLmNvbS9jb3Jkb2FubzIwMTgv.'
    data-yd-impression-id='{ord}'
    data-yd-impression-tracker='https://impression.ydigitalmedia.com'
    data-yd-click-tracker='https://cliks.ydigitalmedia.com'
    data-yd-lp='https://www.ydigitalmedia.com'
    data-yd-parameters='{"src":"ydigital"}'
    data-yd-format='interstitial'>
    <script type="text/javascript" src="//cdn.jsdelivr.net/gh/ydigitalmedia/publisher-tag@4.1.0/yd-publisher.js"></script>
</ins>
```




## License
#### Attribution-NonCommercial-NoDerivatives 4.0 International
[creativecommons.org/licenses/by-nc-nd/4.0/](https://creativecommons.org/licenses/by-nc-nd/4.0/)
