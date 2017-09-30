# wtfayg.js

### Easy exit intent detection

WTFAYG is a simple script that detect when a user is about to exit your pages or landing pages and call your callback function when this happen.


## TODO

 - Remove jQuery dependency and make it dependency free


## How can I use it?

```html
<script src="./test_files/whereTheFuckAreYouGoing.js"></script>
<script>
  function showDialog(){
    $('.exit_intent_popup_selector').show();
  }
  wtfayg(showDialog, options);
</script>
```


## Options

#### Default options

```js
var defaultOptions = {
    minimumView: 50,
    scrollUp: 10,
    scrollOnlyMobile: true,
    limit: 5,
    scrollDelay: 500
};
```

#### minimumView

Default: `50`

The minimum view percentage of the page to activate the scroll-up detection.

#### scrollUp

Default: `10`

The minimum scroll-up percentage to detect exit intent.

#### scrollOnlyMobile

Default: `true`

When true, the scroll-up detection method is active only on mobile devices.

#### limit

Default: `1`

How many times the callback can be called. By default it show the popup (callback function) 1 time, after that, the script is disabled.

#### scrollDelay

Default: `500`

Amount of time in ms to ignore detection after scrolling. This is to prevent incorrect detection. 0 to disable.
