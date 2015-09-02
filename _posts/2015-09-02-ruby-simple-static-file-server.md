---
layout: post
title: A simple static file server in Ruby
---

I use <a href="https://www.nitrous.io">Nitrous.io</a> for development and frequently 
need to launch a server to test Javascript code.  Here's the Ruby command I use to launch a 
WEBrick::HTTPServer (This listens to connections on port 3000 and serves documents from the 
'public' directory).

{% highlight js %}
> ruby -rwebrick -e'WEBrick::HTTPServer.new(:Port => 3000, :DocumentRoot => Dir.pwd + "/public").start'
{% endhighlight %}
