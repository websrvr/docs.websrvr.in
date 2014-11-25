---
title: Why are my folders getting renamed?
tags:
 - debugging
 - folders
sitemap: true
articleidx: 2
---

You may notice that sometimes your root folders (folders inside your
Dropbox/Apps/websrvr/) get renamed. For instance, if your folder is named
`Sterling Archer`, it will be renamed to `sterlingarcher`. We do this because
your folder's name is used as a subdomain for hosting your website.


We do the following to 'fix' folder names:

  1. Remove any character which is not in a-z or 0-9. e.g. 'lana kane (cyril)' will be renamed to 'lanakanecyril'.
  2. Lowercase the name. e.g. 'DipperPines' will be renamed to 'dipperpines'.
  3. Pad a 'w' if your folder name starts with a number. e.g. '3 Gravity Falls' will
     be renamed to 'w3gravityfalls'.
  4. Pad w's if your folder name is less than 4 characters long. e.g. 'ob' will
     be renamed to 'wwob'.
  5. Pad with a random string if your folder name is reserved. e.g. 'www'
     will be renamed to 'wwwsomerandomstring'
  6. Pad with a random string if your folder name is already taken. e.g.
     'minhajuddin' will be renamed to 'minhajuddinrandomstring' because
     'minhajuddin' is already taken. (check it out at
     http://minhajuddin.websrvr.in/)


Whew, so if your folder is renamed, it must be because of one of the above
reasons. If it has been renamed incorrectly, please let us know by sending an
email to support@websrvr.zendesk.com
