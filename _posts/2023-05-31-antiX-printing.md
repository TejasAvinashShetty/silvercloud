---
toc: true
layout: post
description: Setting up HP Printer in AntiX linux distribution.
categories: [markdown]
title: HP Printer meets AntiX Linux
comments: true
hide: false
search_exclude: false
---
# HP Printer meets AntiX Linux

## Acknowledgements
- [Install HP Printer drivers in Ubuntu, Linux Mint, and elementary OS : FossLinux](https://www.fosslinux.com/1547/install-hp-printer-drivers-in-ubuntu-linux-mint-and-elementary-os.htm)
- [How to get HELP with an antiX PROBLEM](https://www.antixforum.com/forums/topic/how-to-get-help-with-an-antix-problem/)
- [Unable to access CUPS or configure a printer on AntiX-19](https://www.antixforum.com/forums/topic/unable-to-access-cups-or-configure-a-printer-on-antix-19/)
- [How to Fix "Systemctl Command Not Found" Error in Linux](https://allthings.how/how-to-fix-systemctl-command-not-found-error-in-linux/)
- [Installing Printers in Linux | CUPS, Printing, and Scanning - YouTube : Chris Titus](https://www.youtube.com/watch?v=En2DJAMpwmY&pp=ygUcaHAgcHJpbnRlciBub3Qgd29ya2luZyBsaW51eA%3D%3D)

c headings as you wish but repeating the hash character, such as you see in the line `## File names` above.


## Basic formatting
```bash
sudo apt-get update
sudo apt-get install cups
sudo apt-get install cups-browsed
sudo apt-get install cups-filters
sudo service cups start
```

after which you should be able to login in browser using

```html
http://localhost:631
```
## An aside
AntiX is not a systemd distro. So, systemctl won't work in it. So tutorials such as [Installing Printers in Linux | CUPS, Printing, and Scanning - YouTube : Chris Titus](https://www.youtube.com/watch?v=En2DJAMpwmY&pp=ygUcaHAgcHJpbnRlciBub3Qgd29ya2luZyBsaW51eA%3D%3D)
won't work off the bat. We need to improvise. So we looked at [How to Fix "Systemctl Command Not Found" Error in Linux](https://allthings.how/how-to-fix-systemctl-command-not-found-error-in-linux/)
There we got the idea of replacing systemctl with service.
So we have `sudo service cups start` instead of `sudo systemctl enable cups 
sudo systemctl start cups`

## Continuing further
We have this page for CUPS
![image](https://github.com/TejasAvinashShetty/silvercloud/assets/27445854/98cd139d-a363-4667-84fa-36f6a7268ce4)
We then click on the highlighted area ![image](https://github.com/TejasAvinashShetty/silvercloud/assets/27445854/0406d58b-fa38-4f58-859b-5505de8546d3)



It seems to do stuff from the command line you could do the following
CUPS Setup - localhost:631
Setup user with modification to use printers
```bash

sudo usermod -aG lpadmin username
```
## more about AntiX
If this post has intrigued you about AntiX linux please see

<iframe width="560" height="315" src="https://www.youtube.com/embed/JCTaUAP6sSg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

or see [run with dolphin ](https://www.youtube.com/@runwiththedolphin)
You can use *italics*, **bold**, `code font text`, and create [links](https://www.markdownguide.org/cheat-sheet/). Here's a footnote [^1]. Here's a horizontal rule:

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![]({{ site.baseurl }}/images/logo.png "fast.ai's logo")

## Code

You can format text and code per usual 

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

Formatting text as shell commands:

```shell
echo "hello world"
./some_script.sh --option "value"
wget https://example.com/cat_photo1.png
```

Formatting text as YAML:

```yaml
key: value
- another_key: "another value"
```


## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |


## Tweetcards

{% twitter https://twitter.com/jakevdp/status/1204765621767901185?s=20 %}


## Footnotes



[^1]: This is the footnote.
