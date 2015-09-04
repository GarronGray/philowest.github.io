---
layout: post
title: Application metrics | Capturing metrics
lead: Metrics provide an accurate, unbiased view of the performance of an application, and can assist greatly with trouble-shooting and evaluation of the application under specific conditions. An example implementation using the Metrics framework is provided.  
glyph: glyphicon-stats
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

<canvas id="myChart" width="600" height="400"></canvas>

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


<script src="/assets/scripts/Chart.min.js"></script>
<script>
Chart.defaults.global = {
    animation: true,
    animationSteps: 60,
    animationEasing: "easeOutQuart",
    showScale: true,
    scaleOverride: false,
    scaleSteps: null,
    scaleStepWidth: null,
    scaleStartValue: null,
    scaleLineColor: "rgba(0,0,0,.1)",
    scaleLineWidth: 1,
    scaleShowLabels: true,
    scaleLabel: "<%=value%>",
    scaleIntegersOnly: true,
    scaleBeginAtZero: false,
    scaleFontFamily: "'Helvetica Neue', 'Helvetica', 'Arial', sans-serif",
    scaleFontSize: 12,
    scaleFontStyle: "normal",
    scaleFontColor: "#666",
    responsive: false,
    maintainAspectRatio: true,
    showTooltips: true,
    customTooltips: false,
    tooltipEvents: ["mousemove", "touchstart", "touchmove"],
    tooltipFillColor: "rgba(0,0,0,0.8)",
    tooltipFontFamily: "'Helvetica Neue', 'Helvetica', 'Arial', sans-serif",
    tooltipFontSize: 14,
    tooltipFontStyle: "normal",
    tooltipFontColor: "#fff",
    tooltipTitleFontFamily: "'Helvetica Neue', 'Helvetica', 'Arial', sans-serif",
    tooltipTitleFontSize: 14,
    tooltipTitleFontStyle: "bold",
    tooltipTitleFontColor: "#fff",
    tooltipYPadding: 6,
    tooltipXPadding: 6,
    tooltipCaretSize: 8,
    tooltipCornerRadius: 6,
    tooltipXOffset: 10,
    multiTooltipTemplate: "<%= value %>",
    onAnimationProgress: function(){},
    onAnimationComplete: function(){}
};
var data = {
    labels: ["0", "10", "20", "30", "40", "50", "60"],
    datasets: [
        {
            label: "My First dataset",
            fillColor: "rgba(220,220,220,0.2)",
            strokeColor: "rgba(220,220,220,1)",
            pointColor: "rgba(220,220,220,1)",
            pointStrokeColor: "#fff",
            pointHighlightFill: "#fff",
            pointHighlightStroke: "rgba(220,220,220,1)",
            data: [65, 59, 80, 81, 56, 55, 40]
        },
        {
            label: "My Second dataset",
            fillColor: "rgba(151,187,205,0.2)",
            strokeColor: "rgba(151,187,205,1)",
            pointColor: "rgba(151,187,205,1)",
            pointStrokeColor: "#fff",
            pointHighlightFill: "#fff",
            pointHighlightStroke: "rgba(151,187,205,1)",
            data: [32, 36, 30, 31, 27, 30, 29]
        }
    ]
};
var ctx = document.getElementById("myChart").getContext("2d");
var myChart = new Chart(ctx).Line(data, Chart.defaults.global);
</script>
