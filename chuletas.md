### Instructions:
#### [How can I use dot.tk domain with GitHub Pages?](https://stackoverflow.com/questions/44081863/how-can-i-use-dot-tk-domain-with-github-pages/49963795#49963795)
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
