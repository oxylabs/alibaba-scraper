# Alibaba Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Alibaba Scraper](https://oxylabs.io/products/scraper-api/ecommerce/alibaba?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Alibaba website effortlessly. This brief guide showcases how Alibaba Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Alibaba results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Alibaba page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.alibaba.com/trade/search?spm=a2700.galleryofferlist.pagemodule_fy23_pc_search_bar.keydown__enter&tab=all&searchtext=phone'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/alibaba-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": " ... </html>",
      "created_at": "2024-01-10 09:36:34",
      "updated_at": "2024-01-10 09:37:07",
      "page": 1,
      "url": "https://www.alibaba.com/trade/search?spm=a2700.galleryofferlist.pagemodule_fy23_pc_search_bar.keydown__enter&tab=all&searchtext=phone",
      "job_id": "7150782465571876865",
      "status_code": 613
    }
  ]
}
```
With our Alibaba Scraper, you can seamlessly pull public data from any Alibaba web page. Gather essential clothing information, such as fabric, styles, price, and customer reviews, to understand the fashion industry trends and outpace your competitors. If you encounter any issues, reach out to our support team through live chat or email us at hello@oxylabs.io.
