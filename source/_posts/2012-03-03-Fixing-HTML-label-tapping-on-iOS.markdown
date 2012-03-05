---
layout: post
title: "Fixing HTML label tapping on iOS"
date: 2012-03-03 15:54
comments: true
categories: 
---

This one should be filed under the WTF category. Apparently, clicking/tapping on HTML
`<label>` in current versions (5.0 or older) of iOS Mobile Safari does not focus the corresponding
`form` element. Not sure if this a bug or done intentionally, but not only is it annoying, but also an accessibility issue.

There is a simple CSS "fix" for this, and it is seems to work pretty well across all form elements:

```css
label { cursor: pointer; }
```

Yeah, that's it. Go figure.