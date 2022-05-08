---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
{% for post in site.posts %} {% assign currentdate = post.date | date: "%Y" %} {% if currentdate != date %}
# {{ currentdate }} 
{% assign date = currentdate %} {% endif %} 
## [{{post.title}}]({{ post.url | remove_first:'/'}})
[ ![]({{site.baseurl}}/assets/img/small/{{post.img}}) ]({{ post.url | remove_first:'/'}})
 {% endfor %}
<!-- {{ post.date | date: "%B" }} - {{post.title}} -->
