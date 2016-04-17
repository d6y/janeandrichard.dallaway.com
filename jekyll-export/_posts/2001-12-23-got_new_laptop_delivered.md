---
id: 905
title: got new laptop delivered
date: 2001-12-23T11:52:00+00:00
author: jane
layout: post
guid: http://www.janeandrichard.co.uk/2001/12/got_new_laptop_delivered
permalink: /2001/12/got_new_laptop_delivered/
---
I got a new laptop delivered on Thursday, and mostly installation has gone very smoothly (took Windows ME off and put 2000 on instead). One issue did arise however, and that was to do with the error message &#8220;Can&#8217;t open ACPI ATK0100 kernel mode driver&#8221;. Reinstalling the supplied drivers from the CD didn&#8217;t help either (altho it might have done if I had known then what I know now). We looked on google for suggestions, and found a [site](http://notebook.asus.com/m1drivers.asp) which had lots of new drivers for the Asus notebooks. I downloaded one of them, and then started the &#8220;Reinstall driver&#8221; process again. Each time, it still decided that the oem6.inf file in the Winnt\inf folder was newer than the one I told it to look at. In the end, the only way to get this to work properly was to rename the file to be oem6.inf.bak. This time, it looked at the location I told it too, and the driver was installed correctly. Hurrah! During the driver installation it recreated this oem6.inf file so there was no need to rename the .bak version.