---
title: Ignored files and directories
tags:
 - ignored-files
 - ignored-directories
 - beginner
sitemap: true
articleidx: 5
---

Websrvr ignores the following:

  1. Files and directories starting with a dot. e.g. `.hello.html`, `.foo.png`
  2. Directories in the root folder with a name matching `Untitled Folder` or `New Folder` (ignoring the case). e.g. `untitled folder 3`, 'New Folder'.

In the future we'll make this configurable via a `websrvr.yml` file :) Till
then, don't get confused if your files start with a `.` and don't show up
online.
