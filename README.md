
Add to the bottom of /opt/slack/resources/app.asar.unpacked/src/static/ssb-interop.js 
( or wherever ssb-interop.js is installed for your distro )

```
document.addEventListener('DOMContentLoaded', function() {
    $.ajax({
    	url: 'https://raw.githubusercontent.com/jnse/slack_theme/master/custom.css',
        async: false,
        cache: false,
        success: function(css) {
            $("<style></style>").appendTo('head').html(css);
        }
    });
});
```


