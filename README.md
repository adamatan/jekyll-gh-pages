# Adding Google Analytics to GH pages with the minimal theme 

## Adding GA to your site 
Find the `_config.yml` file in your repo - it should be in the same directory as the `README.md` file being parsed into HTLM. Add the `google_analytics` key to it:

```
theme: jekyll-theme-minimal
google_analytics: UA—XXXXXXXX-X
```

1. Use your own key (rather than the X stubs). 
2. The `theme` should be `jekyll-theme-minimal`. It might work with other themes, but I have not tested it.

## Testing
Reload the site. You might need to [force-refresh your cache](http://refreshyourcache.com/en/cache/), and it might take a minute for the changes to propogate. View the site source and make sure the analytics function appears at the bottom of the `<body`> part. 

## Why isn't my code in the `<head>`? 
That's how GH pages works. You can't [tweak HTML manually](https://desiredpersona.com/google-analytics-jekyll/), just change `README.md` files and `_config.yml`s. They chose to place the code in the bottom of the `<body>` part rather than in the `<head>`. It [should not change much](https://stackoverflow.com/a/3173593/51197), unless the user closes the page before it finished loading.
