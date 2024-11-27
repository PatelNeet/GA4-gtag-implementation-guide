# GA4-gtag-implementation-guide

# gtag initalization

<!-- Global site tag for Google Analytics -->

<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || []; 
  function gtag() {
    dataLayer.push(arguments);
  }
  
  // Config tag for Measurement ID 1
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');

  // Config tag for Measurement ID 2
  gtag('config', 'G-YYYYYYYYYY');
</script>

# send custom event to GA4 proeprty 
// Send event to 1 proeprty only 
<script>
  gtag('event', 'button_click', {
    'event_category': 'user_interaction',
    'event_label': 'specific_button',
    'value': 1,
    'send_to': 'G-YYYYYYYYYY' // Specify the target Measurement ID
  });
</script>

# cross domain setup 
<script>
  gtag('config', 'G-XXXXXXXXXX', {
    'linker': {
      'domains': ['example1.com', 'example2.com']
    }
  });
</script>
