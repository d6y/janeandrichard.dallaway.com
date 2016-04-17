---
id: 552
title: 'And another rant &#8230;'
date: 2003-09-10T16:42:00+00:00
author: jane
layout: post
guid: http://www.janeandrichard.co.uk/2003/09/and_another_rant_...
permalink: /2003/09/and_another_rant_.../
---
And another M$ rant&#8230; I&#8217;m using SQL Server, and I want to (programatically) change the next identity for a new record in a table. So, I use the [DBCC CheckIdent](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/tsqlref/ts_dbcc_5lv8.asp) command. If no records have ever been inserted into the table, then I use DBCC CheckIdent (_[tablename]_, RESEED,_[number I want the next record to have]_). However, if records have been inserted then I need to use DBCC CheckIdent (_[tablename]_, RESEED, _[number I want the next record to have]_ **+1**). What a load of pants!