# Instructions and code snippets for the upcoming PARKROYAL COLLECTION KL campaigns

## Google Ads (adwords) Remarketing Tag & Landing Page View Conversion Action Combined code snippet
To be installed on every page of the site, firing on page load

```
<!-- Google tag (gtag.js) Remarketing Tag and LandingPageView Conversion Action Combined-->
<script async src="https://www.googletagmanager.com/gtag/js?id=AW-11017965890"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'AW-11017965890');
  
  // Event snippet for Landing Page View conversion page -->
  gtag('event', 'conversion', {'send_to': 'AW-11017965890/6HX0CJLXjYEYEMKi44Up'});

</script>
```

## Additional Google Ads (adwords) Conversion Tags

### Event Snippet for Lead (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Lead conversion -->
<script>
  gtag('event', 'conversion', {'send_to': 'AW-11017965890/xaaeCJXXjYEYEMKi44Up'});
</script>
```


### Event Snippet for Begin Checkout (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Begin Checkout conversion page -->
<script>
  gtag('event', 'conversion', {
      'send_to': 'AW-11017965890/5suCCJvXjYEYEMKi44Up',
      'value': 1.0,       // CONFIGURE THIS TO PULL BASKET VALUE DYNAMICALLY FROM THE USERS 'CART'
      'currency': 'USD'   // SET TO USER's CURRENCY
  });
</script>
```

### Event Snippet for Purchase (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Purchase conversion page -->
<script>
  gtag('event', 'conversion', {
      'send_to': 'AW-11017965890/cXoRCJjXjYEYEMKi44Up',
      'value': 1.0,         // CONFIGURE THIS TO PULL BASKET VALUE DYNAMICALLY FROM THE USERS 'CART'
      'currency': 'USD',    // SET TO USER's CURRENCY
      'transaction_id': ''  // CONFIGURE THIS TO PULL TRANSACTION ID DYNAMICALLY FROM THE USERS 'CART'
  });
</script>
```
