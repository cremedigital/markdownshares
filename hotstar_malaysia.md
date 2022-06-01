# Disney Hotstar Project

## Tik Tok

```
<script>
!function (w, d, t) {
  w.TiktokAnalyticsObject=t;var ttq=w[t]=w[t]||[];ttq.methods=["page","track","identify","instances","debug","on","off","once","ready","alias","group","enableCookie","disableCookie"],ttq.setAndDefer=function(t,e){t[e]=function(){t.push([e].concat(Array.prototype.slice.call(arguments,0)))}};for(var i=0;i<ttq.methods.length;i++)ttq.setAndDefer(ttq,ttq.methods[i]);ttq.instance=function(t){for(var e=ttq._i[t]||[],n=0;n<ttq.methods.length;n++)ttq.setAndDefer(e,ttq.methods[n]);return e},ttq.load=function(e,n){var i="https://analytics.tiktok.com/i18n/pixel/events.js";ttq._i=ttq._i||{},ttq._i[e]=[],ttq._i[e]._u=i,ttq._t=ttq._t||{},ttq._t[e]=+new Date,ttq._o=ttq._o||{},ttq._o[e]=n||{};var o=document.createElement("script");o.type="text/javascript",o.async=!0,o.src=i+"?sdkid="+e+"&lib="+t;var a=document.getElementsByTagName("script")[0];a.parentNode.insertBefore(o,a)};

  ttq.load('CA2QFR3C77U70J019350');
  ttq.enableCookie(); //enable use of first-party cookies
  ttq.page();
}(window, document, 'ttq');
</script>

Events:

<script>
  ttq.instance('CA2QFR3C77U70J019350').track('SubmitForm');
</script>

questions:
advanced matching - https://ads.tiktok.com/help/article?aid=10007891
allow 1st-party cookies

Docu:
https://ads.tiktok.com/help/article?aid=10028
```

# AppsFlyer

```
<!-- AppsFlyer web SDK -->
<script>
!function(t,e,n,s,a,c,i,o,p){t.AppsFlyerSdkObject=a,t.AF=t.AF||function(){
(t.AF.q=t.AF.q||[]).push([Date.now()].concat(Array.prototype.slice.call(arguments)))},
t.AF.id=t.AF.id||i,t.AF.plugins={},o=e.createElement(n),p=e.getElementsByTagName(n)[0],o.async=1,
o.src="https://websdk.appsflyer.com?"+(c.length>0?"st="+c.split(",").sort().join(",")+"&":"")+(i.length>0?"af_id="+i:""),
p.parentNode.insertBefore(o,p)}(window,document,"script",0,"AF","pba",{pba: {webAppId: "WEB_DEV_KEY", measurementStatus:true}})
</script>
```
```
<script>
// set customer user id upon logging in
AF('pba', 'setCustomerUserId' , '663274')
</script>
```

```
<script>
// purchase event of shoes with associated revenue
AF('pba', 'event', {
    eventType: 'EVENT',
    eventName: 'subscribe',
    eventRevenue: 54.90,
    eventValue: {
        "package": "family",
        "plan": "name",
        "currency": "MYR"
        }
    });
</script>
```


Do the following: 

Get the Web SDK Web Dev Key. Note! This is not the same key used by mobile apps.
To get the Web Dev Key: 
In AppsFlyer, go to the My Apps tab.
Click View brand bundles.
Copy the required Web Dev Key. (WEB_DEV_KEY)
If you implement Smart Banners, get the Smart Banner key. 
To get the Smart Banner Key:
In AppsFlyer, go to Engagement & Deep Linking > Smart Banners.
Copy the required Smart Banner Key. 


To set conversion events:

From the Brand Bundles page, select the brand bundle.
The Update Brand bundles page opens.
Go to the Web event settings tab.
Turn on Mark as conversion event as required.
Click Update bundle.

Web users are identified in AppsFlyer by using the unique CUID you allocate them. Typically the CUID is managed by your backend servers. 
Use the same CUID value you use in the mobile environment. Doing so enables you to have a holistic view of user activity across multiple platforms. The function in the mobile SDK is setCustomerUserId function (iOS, Android, Unity).
To set the CUID in the web SDK:
Set the CUID at the earliest point that you have access to it. Most times this means you need to wait for the user to identify via login or sign up.
Fire the JavaScript call to setCustomerUserId() as shown in the example that follows. 
Note! Send the CUID as a string even if it is a number. Do so enclosing it in quotation marks.

Associate all current user web events to distinct ID 663274 

## Facebook Pixel

Best is to use the Disney existing pixel, but we can provide indahash pixel also if needed.
`Pixel ID: 1410048749070946`