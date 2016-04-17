---
id: 490
title: For the last work
date: 2004-03-22T15:44:00+00:00
author: jane
layout: post
guid: http://www.janeandrichard.co.uk/2004/03/for_the_last_work
permalink: /2004/03/for_the_last_work/
---
For the last 2 work days I&#8217;ve been battling with DTS and Foxpro files. I&#8217;m importing data from some DBF files into SQL Server, and noticed that if the DTS package failed, the DBF files were remaining locked and so could not be deleted from the working area &#8211; but only when executed through VB, through SQL Server directly it was fine.

The inability to delete the files contaminated my next import (assuming it happened within a minute or two of the failed import). Finally, after a lot of searching around and a serious amount of head scratching, Gary found a useful tip which said that the problem happened less if you specified a sql query (i.e. select * from tablename) rather than just specifying the table in the Table/View field of the &#8220;Transform Data Task properties&#8221; within the DTS Package. And it works. Kind of. It hasn&#8217;t eliminated the problem entirely, but VB can now delete the files. If I try and delete them manually I still get the &#8220;Cannot delete FILENAME: It is being used by another person or program.&#8221; error.

Useful resources were [microsoft.public.sqlserver.dts](http://groups.google.com/groups?q=microsoft.public.sqlserver.dts&ie=UTF-8&oe=UTF-8&hl=en), [SQLDTS](http://www.sqldts.com) and [SQL Server Central](http://www.sqlservercentral.com/).