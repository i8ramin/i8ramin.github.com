---
layout: post
title: "Triggering Zepto Tap Event using Click"
date: 2012-03-04 21:10
comments: true
categories: zepto mobile debugging
---

This one will come in handy if you are testing/debugging your mobile website on a Desktop browser (i.e. Safari, Chrome) with a custom User-Agent set and are utilizing the `tap` event provided by [Zepto JS](http://zeptojs.com/).

The issue with binding the `tap` event is that you cannot trigger them with a mouse click. And we all know that debugging on simulator and emulators is a pain in the ass, so hopefully this little code snippet will save you some time.

```javascript
(function($) {
    // only do this if not on a touch device
    if (!('ontouchend' in window)) {
        $(document).delegate('body', 'click', function(e) {
            $(e.target).trigger('tap');
        });
    }
})(window.Zepto);
```

You can use the same technique to trigger `touchstart` and `touchend` events using `mousedown` and `mouseup`.