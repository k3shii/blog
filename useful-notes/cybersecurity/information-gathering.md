# Information Gathering

## Hunting Subdomains

* sublist3r (kali)
* [crt.sh](http://crt.sh)

## Identify Website Technologies

💡 Check what technologies used on the website

* builtwith
* wappalyzer (wirefox extension)
* whatweb

```python
┌──(root㉿kali)-[/home/k3shi]
└─# whatweb https://tesla.com
https://tesla.com [403 Forbidden] Akamai-Global-Host, Country[UNITED STATES][US], HTTPServer[AkamaiGHost], IP[23.218.192.46], Strict-Transport-Security[max-age=15768000], Title[Access Denied], UncommonHeaders[x-reference-error,permissions-policy]

```

## Burp Suite

web proxy

1. Firefox Setting → General Setting
2. [http://burp](http://burp) → download CA Certificate
3. Firefox Setting → Privacy & Security → Import Certificate

## Google Fu

* `site:tesla.com`: show all url contain tesla.com
* `site:tesla.com -www`: show all url contain tesla.com without www
* `site:tesla.com filetype:pdf`: show content based on filetype
