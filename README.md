# Tradingview Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Tradingview Scraper](https://oxylabs.io/products/scraper-api/web/tradingview?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Tradingview website effortlessly. This brief guide explains how an Tradingview Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Tradingview results by providing your own URLs to our service. We can return the HTML for any Tradingview page you like.

#### Python code example

The example below illustrates how you can get HTML of Tradingview page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.tradingview.com/pricing/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/tradingview-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE html>\n<html lang=\"en\" dir=\"ltr\" class=\"is-not-authenticated is-not-pro is-not-trial \">\n<h ... </html>",
      "created_at": "2023-12-18 10:41:59",
      "updated_at": "2023-12-18 10:42:01",
      "page": 1,
      "url": "https://www.tradingview.com/pricing/",
      "job_id": "7142464006102464513",
      "status_code": 200
    }
  ]
}
```
With our Tradingview Scraper, you can fluidly harvest public data from any Tradingview web page. Accumulate essential financial info, like stock prices, user feedback, and detailed analysis to stay informed about the markets and outpace your business rivals. Should you need any assistance, our dedicated support team can be reached either via live chat or by sending an email to hello@oxylabs.io.