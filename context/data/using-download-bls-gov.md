---
title: Using https://download.bls.gov/
description: Downloading BLS data in flat file format directly into your R or Python session from https://download.bls.gov/ can be a convenient way to access the data.
parent: index.md
max_lines: 250
source: slab
---

# Using https://download.bls.gov/

Downloading BLS data in flat file format directly into your R or Python session from [https://download.bls.gov/](https://download.bls.gov/) can be a convenient way to access the data. However, BLS is using a bot detection system that may interfere with your script. Sharing here my correspondence with BLS in which they explain how the data can be accessed without problem.

## BLS email reply

Per our [usage policy](https://www.bls.gov/bls/pss.htm), simply set the user agent to your email address and your script should work fine. Depending on the programming language that you use the syntax of adding your email address to the user-agent will be different. 

For example:

**Add:**

`user_agent = {'User-agent': 'johnqsmith@abc.com' }`

**Update get statement:**

`response = requests.get(url, headers = user_agent, proxies=proxies)`

or

`curl -A "johnqsmith@abc.com" https://download.bls.gov/pub/time.series/bd/bd.dataclass`

or

`wget -U "johnqsmith@abc.com" https://download.bls.gov/pub/time.series/bd/bd.dataclass`

Additional samples of user-agent policy are available at [https://meta.wikimedia.org/wiki/User-Agent_policy](https://meta.wikimedia.org/wiki/User-Agent_policy). Please view our [FAQs page](https://www.bls.gov/developers/api_faqs.htm) to read more.
