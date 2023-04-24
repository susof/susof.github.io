### Instructions:
#### [How can I use dot.tk domain with GitHub Pages?](https://stackoverflow.com/questions/44081863/how-can-i-use-dot-tk-domain-with-github-pages/49963795#49963795)
1. Login to freenom.com
2. Go to Services -> My Domains -> Manage Domain
3. Management Tools -> Nameservers
4. Select **Use default nameservers (Freenom Nameservers)**
5. Now Go To Manage Freenom DNS, and set up your records like this:

   - Name: empty / Type: A / TTL: default? / Target: one of github IP's ([see here]([url](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)))
   - Name: empty / Type: A / TTL: default? / Target: another github IP's ([see here]([url](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)))
   - ...
   - Name: `www.` / Type: CNAME / TTL: default? / Target: your-user-or-project-name.github.io 

   (that last line will change from `www.` to `WWW` when you save the records)
