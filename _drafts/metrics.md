---
layout: post
title: Metrics
lead: Capturing metrics in Java applications using Coda Hale's metrics framework. 
---

<ul>
<li>Mentioned at scaleconf</li>
<li>Maven dependencies</li>
<li>Singleton implementation</li>
<li>Injection implementation</li>
<li>Custom reporter</li>
</ul>

<h3>The importance of metrics</h3>

<h3>Github sample application</h3>
<!--
<div class="embed-responsive embed-responsive-16by9">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/czes-oa0yik" frameborder="0" allowfullscreen></iframe>
</div>
-->
<p>
{% highlight xml %}
<dependencies>
    <dependency>
        <groupId>io.dropwizard.metrics</groupId>
        <artifactId>metrics-core</artifactId>
        <version>3.1.0</version>
    </dependency>
</dependencies>
{% endhighlight %}
</p>
<p>
{% highlight java %}
System.out.println("metrics!");
{% endhighlight %}
</p>
