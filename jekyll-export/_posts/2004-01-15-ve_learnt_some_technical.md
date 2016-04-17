---
id: 507
title: ve learnt some technical
date: 2004-01-15T16:29:00+00:00
author: jane
layout: post
guid: http://www.janeandrichard.co.uk/2004/01/ve_learnt_some_technical
permalink: /2004/01/ve_learnt_some_technical/
---
I&#8217;ve learnt some technical stuff today which makes the installation of our product a lot easier:

  1. you can tell [MSDE](http://www.microsoft.com/sql/msde/default.asp) to use mixed authentication mode by adding SECURITYMODE=SQL into the setup.ini file or as a parameter
  2. you can start the SQL Server and SQL Agent services using &#8220;net start MSSqlServer&#8221; and &#8220;net start SqlServerAgent&#8221; 
  3. you can make a batch file call an external program and wait until its finished before doing the next thing by using &#8220;Start /w appname&#8221; (/w means wait)