This is a very simple project than takes a war file and uploads it to Google App Engine

It's designed to be drop-in deploy stage in your build pipeline. The input is a war file and one property file dropped into the artifacts folder.

For example:
```
artifacts/foo.war
artifacts/deploy.properties
```

And deploy.properties contains

```
deploy.name=foo-appid
deploy.war=foo.war
```

Then just setup your build pipeline to trigger this project and supply your `deploy.username` and `deploy.password` as properties.

If you want more control then use the appcfg task directly.