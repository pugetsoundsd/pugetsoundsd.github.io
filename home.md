---
layout: page
title: Home
permalink: /
donation_links: 
    donation_1:
        text: "donation1"
        id: 7334HG9754
    
}
---

# Welcome to the homepage of Puget Sound Speech and Debate!

This site is under construction! For more information, please take a look at our about page.

# Donations

{% for i in page.donation_links%}
  <form class="paypalform" action="https://www.paypal.com/cgi-bin/webscr" method="post">
    <input type="hidden" name="cmd" value="_s-xclick">
    <input type="hidden" name="hosted_button_id" value="{{ i.id | default: 'UNCONFIGURED' }}">
    <button class="donations uk-button uk-button-primary" name="submit">
      <span>{{ i.text | default: 'Donations' }}</span>
    </button>
    <img alt="" border="0" src="https://www.paypal.com/en_US/i/scr/pixel.gif" width="1" height="1">
  </form>
{% endfor %}