---
layout: post
title: Ruby: A simple static file server in one line
---
This launches a new WEBrick::HTTPServer that listens to connections on port 3000, and serves documents from a 
'public' directory. 

{% highlight js %}
> ruby -rwebrick -e 'WEBrick::HTTPServer.new(:Port => 3000, :DocumentRoot => Dir.pwd + "/public").start'
{% endhighlight %}

Or as a Ruby script server.rb:

{% highlight js %}
require 'webrick'
root = Dir.pwd + '/public'
server = WEBrick::HTTPServer.new :Port => 3000, :DocumentRoot => root
trap 'INT' do server.shutdown end
server.start
{% endhighlight %}

