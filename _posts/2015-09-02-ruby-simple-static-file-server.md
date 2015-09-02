---
layout: post
title: Ruby: A simple static file server in one line
---

This launches a new WEBrick::HTTPServer that listens to connections on port 3000, and serves documents from a 
'public' directory. 

{% highlight js %}
> ruby -rwebrick -e 'WEBrick::HTTPServer.new(:Port => 3000, :DocumentRoot => Dir.pwd + "/public").start'
{% endhighlight %}

