---
title: Useful Snippets
id: 58
date: 2013-11-12 13:41:55
---

This page is for those useful code snippets or commands that I use every now and then but never remember.

### Linux

Secure copy over ssh **from server:** (username is pi hostname is xbmc)

    $ scp pi@xbmc:file.txt /local/directory`</pre>
    Secure copy over ssh **to server:**
    <pre>`$ scp file.txt pi@xbmc:/remote/directory`
    `$ scp -r folder pi@xbmc:/remote/directory`</pre>
    Chown syntax
    <pre>`$ sudo chown -R ryanralph dotfiles

&nbsp;

This page is a work in progress and things will be added and removed as needed