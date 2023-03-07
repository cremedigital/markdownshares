# Instructions and code snippets for the upcoming PARKROYAL LANGKAWI RESORT campaigns

## Google Ads (adwords) Remarketing Tag & Landing Page View Conversion Action Combined code snippet
To be installed on every page of the site, firing on page load

```
<!-- Google tag (gtag.js) Remarketing Tag and LandingPageView Conversion Action Combined-->
<script async src="https://www.googletagmanager.com/gtag/js?id=AW-11110343340"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'AW-11110343340');
</script>
  
  // Event snippet for Landing Page View conversion page -->
  
<script>
  gtag('event', 'conversion', {'send_to': 'AW-11110343340/c6MUCOr3kJAYEKzF6bEp'});
</script>
```

## Additional Google Ads (adwords) Conversion Tags

### Event Snippet for Lead (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Lead conversion page -->
<script>
  gtag('event', 'conversion', {'send_to': 'AW-11110343340/IK2CCPufiJAYEKzF6bEp'});
</script>
```

### Event Snippet for Begin Checkout (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Begin Checkout conversion page -->
<script>
  gtag('event', 'conversion', {
      'send_to': 'AW-11110343340/bgmICKLBkJAYEKzF6bEp',
      'value': 1.0,         // CONFIGURE THIS TO PULL BASKET VALUE DYNAMICALLY FROM THE USERS 'CART'
      'currency': 'USD'     // SET TO USER's CURRENCY
  });
</script>
```

### Event Snippet for Purchase (Requires the above gtag config tag to have fired on the page already)
```
<!-- Event snippet for Purchase conversion page -->
<script>
  gtag('event', 'conversion', {
      'send_to': 'AW-11110343340/TtB0CLbrjpAYEKzF6bEp',
      'value': 1.0,          // CONFIGURE THIS TO PULL BASKET VALUE DYNAMICALLY FROM THE USERS 'CART'
      'currency': 'USD',     // SET TO USER's CURRENCY
      'transaction_id': ''   // CONFIGURE THIS TO PULL TRANSACTION ID DYNAMICALLY FROM THE USERS 'CART'
  });
</script>

```
