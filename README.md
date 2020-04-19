# About sitedorks
Search Google or Bing for a search term with different websites. A default list is already provided, which contains Github, Gitlab, Trello etc. Also a list available with googledorks for communication invites like WhatsApp, Skype and Zoom.

# Why sitedorks?
Why wouldn't you just enter dorks for several websites manually? 
The script has a few useful functions. Google ignores too many keywords in a query and with argument -c it's easy to split a file with websites into new queries. Also, it's easy to create different input files for different uses. Adding new websites to your search query can be arranged by just adding them to an input file.

# Install
Sitedork should be able to run with a default Kali Linux installation without installing additional Python packages. If you're running into trouble running grepaddr, please drop me an issue and I'll try to fix it :)

# Usage
```
usage: sitedorks [-h] [-c <count>] [-f <file>] -q <query>

Search Google for a search term with different websites. Use escaped quotes when necessary: \"

optional arguments:
  -h, --help  show this help message and exit
  -c <count>  How many websites checked per query. Google has a maximum length for queries.
  -f <file>   Enter a custom website list.
  -q <query>  Enter a search term.
```
# Examples
Want to look for "uber.com" with different sites containing all kinds of content? Use the following command:
```
sitedorks -q \"uber.com\"
```
This opens 2 URLs in your default webbrowser like these:

* https://www.google.nl/search?num=100&filter=0&q=%22uber.com%22+site:123formbuilder.com+|site:amazonaws.com+|site:bitbucket.org+|site:cloudformz.com+|site:cloudfront.net+|site:codebeautify.org+|site:codepen.io+|site:cognitoforms.com+|site:core.windows.net+|site:ecitydoc.com+|site:emaze.com+|site:formdesk.com+|site:form.jotform.com+|site:formlets.com+|site:formsite.com+|site:forms.office.com+|site:formstack.com+|site:github.com+|site:gitlab.com+|site:haikudeck.com+|site:hubspot.net+|site:ideone.com+|site:jsfiddle.net+|site:multiscreensite.com+|site:pastebin.com+|site:pastefs.com+|site:pastelink.net+|site:prezi.com+|site:repl.it+|site:slidebean.com
* https://www.google.nl/search?num=100&filter=0&q=%22uber.com%22+site:slides.com+|site:slideshare.net+|site:slidex.tips+|site:sway.office.com+|site:trello.com+|site:visme.co+|site:webflow.com+|site:wufoo.com+|site:ziladoc.com+|site:zoho.com+|site:zonebourse.com

Want to search for communication invites? Use the following command:
```
sitedorks -f commdorks.txt -s disable -c 10
```
This opens 2 URLs in your default webbrowser like these:

* https://www.google.com/search?num=100&filter=0&q=%20%22bcwt.webex.com%22+|+%22bluejeans.com%22+|+%22chat.whatsapp.com%22+|+%22gotomeet.me%22+|+%22hangouts.google.com/group%22+|+%22join.slack.com/t%22+|+%22join.skype.com/invite%22+|+%22meet.google.com%22+|+%22meet.jit.si%22+|+%22meet.starleaf.com%22
* https://www.google.com/search?num=100&filter=0&q=%20%22teams.microsoft.com/l/meetup-join%22+|+%22t.me/joinchat%22+|+%22zoom.us/j%22

# Contribute?
Do you have some usefull additions to the script or to the list of websites, please send in a pull request to help make this script better :)
