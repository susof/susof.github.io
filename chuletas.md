### Instructions:

First of all, if you want to use an apex domain (just root domain address, no subdomains) you must follow an order:
<https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain>
And then ...

#### [How can I use dot.tk domain with GitHub Pages?](https://stackoverflow.com/questions/44081863/how-can-i-use-dot-tk-domain-with-github-pages/49963795#49963795) (see also [here](https://stackoverflow.com/questions/67652848/freenom-url-forwarding-to-github-hosted-repo-is-returning-a-502-bad-gateway-erro/67737607#67737607))

1. Login to freenom.com
2. Go to _Services -> My Domains -> Manage Domain_
3. _Management Tools -> Nameservers_
4. Select **_Use default nameservers (Freenom Nameservers)_**
5. Now Go To _Manage Freenom DNS_, and set up your records like this:

   - Name: empty / Type: A / TTL: default? / Target: one of github IP's ([see here]([url](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)))
   - Name: empty / Type: A / TTL: default? / Target: another github IP's ([see here]([url](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)))
   - ...
   - Name: `www.` / Type: CNAME / TTL: default? / Target: your-user-or-project-name.github.io  

   (that last line will change from `www.` to `WWW` when you save the records)
5. Optionally, check the _enforce HTTPS_ checkbox so your pages are served through secure connection


#### Regarding subdomains & subpages, check these:
- <https://superuser.com/questions/1499092/subdomains-through-freenom-with-github>


#### freenom.com (dot.tk) domain github tools:
- <https://github.com/topics/freenom> also by languages: [Python](https://github.com/topics/freenom?l=python)
