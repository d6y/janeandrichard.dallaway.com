---
id: 104
title: That looks about right
date: 2008-04-16T05:07:00+00:00
author: richard
layout: post
guid: http://www.janeandrichard.co.uk/2008/04/that_looks_about_right
permalink: /2008/04/that_looks_about_right/
---
Is it meme o&#8217;clock already? Well, if [you](http://happygiraffe.net/blog/articles/2008/04/13/that-looks-somewhat-iffy) really must know&#8230;

<pre><tt>
<a href="http://en.wikipedia.org/wiki/Toto_(dog)">toto</a>:~ richard$  history|awk '{a[$2]++} END{for(i in a){printf "%5d\t%s\n",a[i],i}}'|sort -rn|head
  130 cd
  110 ls
   50 ssh
   20 exit
   15 scp
   14 cp
   11 svn
   11 sudo
   11 openssl
   11 java
</tt></pre>

I&#8217;m surprised there&#8217;s not some `find`, `grep` and `mate` in there.