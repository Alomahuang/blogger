---
title: "Github Pages with HTTPS"
date: 2022-11-12 T00:00:00-00:00
categories:
  - Web
tags:
  - Github Pages
---

When using a custom domain for my GitHub Pages, and after waiting for DNS to work, I still get the message that my DNS provider is not properly configured to support HTTPS.

I registered my domain and configured the DNS service with GoDaddy, and here's how I solved the problem.

![problem]({{ site.baseurl }}/assets/images/2022/11/01.png)

### Before troubleshooting
First, you must follow the [documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages) to configure everything it asks you to do.
So, in the DNS service, you should have records with type A to GitHub server IPs( there are 4.) And a record with type TXT to validate that you own the address.

### My problem
After researching, I discovered that the default records in a newly registered address in GoDaddy would have an A record with the value **parked**. 

![problem]({{ site.baseurl }}/assets/images/2022/11/02.png)

After **deleting** this record and waiting for 5 minutes( for DNS service, it always takes some time and patience), I refresh the setting page for the Github pages, finally allowing me to enforce HTTPS.

![problem]({{ site.baseurl }}/assets/images/2022/11/03.png)

### Further help
I also follow a helpful tip[^1] from a GitHub user, [codelahiru](https://github.com/codelahiru), who suggests to
> go to https://support.github.com/ -> type "custom domain https" in search field -> select "Our virtual assistant can help" -> follow along with the bots questions.

The bot is amazingly helpful in detecting the problem with my domain issue.

[^1]: the original post is [here](https://github.com/orgs/community/discussions/23049)










