---
layout: page
title: nachrichten
permalink: /nachrichten/
ref: blog
lang: de
---

<div class="page-content">
    <div class="wrapper">
         <div id="pagecontent" class="main-sec">
              <div class="blog">
                 <ul class="post-list">
                   {% assign posts=site.posts | where:"lang", page.lang %}
                      {% for post in posts %}
                        <li>
			  <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
                          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>               
                       </li>
                     {% endfor %}
                </ul>
                <p class="rss-subscribe">suivre le <a href="{{ '/futter.xml' | prepend: site.baseurl }}">Futter RSS</a></p>
            </div>
        </div>
    </div>
 </div>
