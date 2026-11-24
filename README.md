# Alibaba Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=alibaba-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

Oxylabs' [Alibaba Scraper](https://oxylabs.io/products/scraper-api/ecommerce/alibaba?utm_source=github&utm_medium=repositories&utm_campaign=product) (a part of Web Scraper API) is a data gathering solution allowing you to extract real-time information from an Alibaba website effortlessly. This brief guide showcases how Alibaba Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Alibaba results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Alibaba page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
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
      "created_at": "2025-01-10 09:36:34",
      "updated_at": "2025-01-10 09:37:07",
      "page": 1,
      "url": "https://www.alibaba.com/trade/search?spm=a2700.galleryofferlist.pagemodule_fy23_pc_search_bar.keydown__enter&tab=all&searchtext=phone",
      "job_id": "7150782465571876865",
      "status_code": 613
    }
  ]
}
```
With our Alibaba Scraper, you can seamlessly pull public data from any Alibaba web page. Gather essential clothing information, such as fabric, styles, price, and customer reviews, to understand the fashion industry trends and outpace your competitors. If you encounter any issues, reach out to our support team through live chat or email us at support@oxylabs.io.
