# Browser Testing and Support

We default to supporting the newest and the last previous two releases of popular browsers (Edge, Safari, Chrome, Firefox, and Android Browser) for mobile and desktop devices. We also support Internet Explorer 11 but not older versions of Internet Explorer, as [Microsoft no longer supports these browsers](https://www.microsoft.com/en-us/windowsforbusiness/end-of-ie-support)

Older versions are much harder, more time consuming and hence more expensive to design for, develop for and support.

In limited special cases, user demographics will dictate that supporting a less common or older version of a browser is required. Those special cases should be identified early on so we can plan for additional time and expense to support the version.

As important tools for our development and testing process, we use [BrowserStack](http://browserstack.com/) as our device lab, [Modernizr](https://modernizr.com/) for browser feature detection and [Browserl.ist](https://browserl.ist/) to share target browsers between different front-end tools.