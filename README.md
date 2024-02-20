# Kobo Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Kobo Scraper](https://oxylabs.io/products/scraper-api/ecommerce/kobo?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Kobo website effortlessly. This brief guide showcases how Kobo Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Kobo results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Kobo page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.kobo.com/us/en'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/kobo-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\r\n\r\n\r\n<!doctype html>\r\n<html lang=\"en-us\">\r\n<head>\r\n    \r\n\r\n\r\n\r\n\r\n<meta charset=\"UTF-8\">\r\n<meta name ... </html>",
      "created_at": "2024-02-20 12:54:07",
      "updated_at": "2024-02-20 12:54:10",
      "page": 1,
      "url": "https://www.kobo.com/us/en",
      "job_id": "7165690082605671425",
      "status_code": 200
    }
  ]
}
```
With our Kobo Scraper, you can efficiently extract public data from any Kobo webpage. Gather the necessary book information, including price, user ratings, and synopsis, for a comprehensive market analysis and outperform your competitors. If you need any assistance, our support team is readily available through live chat, or you can email us at hello@oxylabs.io.