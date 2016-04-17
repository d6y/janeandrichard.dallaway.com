---
id: 844
title: ASP Upload Components
date: 2002-05-03T13:37:00+00:00
author: jane
layout: post
guid: http://www.janeandrichard.co.uk/2002/05/asp_upload_components
permalink: /2002/05/asp_upload_components/
---
A bit of a geeky blog this one. Today I&#8217;ve been researching Upload components for ASP to use in the project I&#8217;m working on at the moment. Ideally I want one that does the following:

  * Uploads a file from the client&#8217;s file system, directly into the database
  * Can upload all types of files, not just images

I had a quick discussion on [BNM](http://brightonnewmedia.org/pipermail/bnmlist/2002-May/006819.html) about this, and also consulted [15 Seconds](http://www.15seconds.com/focus/Upload.htm).

I decided to try [ASPUpload](http://www.aspupload.com/) first, as this was recommended both by BNM and by an ex-colleague of mine. I got this working pretty quickly, but it doesn&#8217;t seem to be able to present me with the Mime Type (i.e. image/gif etc) and so isn&#8217;t very useful for handling different kinds of binary data. I know that I could code around this issue, but I&#8217;d rather it did it all for me really.

My next thought was to try [SA File Up](http://www.softartisans.com/softartisans/saf.html), a product I&#8217;ve used many times before. Unfortunately their evaluation copy expires on 1 May 2001, that&#8217;s 2 days ago &#8211; helpful.

Attempt 3 was [ABCUpload](http://www.websupergoo.com/abcupload-1.htm). On the plus side, this is a free product. This took a bit longer to get to work, as the help documents are not as comprehensive as ASPUpload. Hidden, on the [Object Reference page](http://www.websupergoo.com/helpupload/4-objectref/2-xfield/default.htm) I found the property I was looking for &#8211; MIMEType. Woohoo! But alas, it only seems to be able to work out the Mime Types for images so, PDFs etc are out of the question. And more annoying still, it won&#8217;t even upload the damn things. Bah!

Attempt number 4. The last of the BNM recommendations. [Dundas Upload](http://www.dundas.com/subFrame.asp?products/asp/upload/index.asp). Another free offering. The examples don&#8217;t seem to cover saving to a database, but a more thorough hunt through the [documentation](http://www.dundas.com/products/onlineDocs/FreeProds/Upload/Tutorial_3_ADO_Support_and_Saving_a_File_as_a_BLOB.htm) found it hidden away. This component has a ContentType property, and seems to insert pdfs, excel spreadsheets as well, so we might just have found our answer. Hurrah!