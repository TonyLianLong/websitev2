---
layout: default
title: "Long (Tony) Lian's Personal Website"
---

<main role="main" class="container-sm" style="max-width: 960px">
    <div class="row">
        <div class="col">
            <p class="h1 mt-5 page-title">
                <img class="profile-img-small d-md-none" src="{{ '/assets/profile.jpg' | relative_url }}" />
                <span style="clear: right">Long (Tony) Lian</span>
            </p>
            <p class="h4 section-title" style="clear: right">About</p>
            {% capture bio %}{% include bio.md %}{% endcapture %}
            <p>{{ bio | markdownify }}</p>
            <a href="mailto:longlian@berkeley.edu">Email</a> / <a href="{{ '/assets/cv.pdf' | relative_url }}">CV</a> / <a href="https://scholar.google.com/citations?user=eOLxyqUAAAAJ">Google Scholar</a> / 
                <a href="https://www.linkedin.com/in/longlian">LinkedIn</a> / <a href="https://github.com/TonyLianLong">Github</a>
        </div>
        <div class="col-auto d-none d-md-block">
            <img class="profile-img" src="{{ '/assets/profile.jpg' | relative_url }}" />
        </div>
    </div>
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Publications <span class="h6">(*: equal contribution)</span></p>
            <div class="container-fluid" style="padding: 0;">
                {% assign sorted_publications = site.publications | sort:"date" %}
                {% for publication in sorted_publications reversed %}
                <div class="row">
                    <div class="col">
                        <p class="h5 publication-title">{{ publication.title }}</p>
                        <span class="publication-authors">{{publication.authors | markdownify}}</span>
                        {% if publication.venue %}
                            <span class="publication-venue">{{publication.venue | markdownify}}</span>
                        {% endif %}
                        <p class="publication-excerpt"> {{publication.excerpt}} </p>
                        <!-- <p>{{ publication.content }}</p> -->
                        {% if publication.paper_url %}
                        <p class="publication-links"> <a href="{{publication.paper_url}}">Paper</a> 
                        {% if publication.video_url %}/ <a href="{{publication.video_url}}">Video</a>{% endif %} 
                        {% if publication.code_url %}/ <a href="{{publication.code_url}}">Code</a>{% endif %} 
                        </p>
                        {% endif %}
                    </div>
                    {% if publication.cover_image %}
                    <div class="col-4 d-none d-md-block align-self-center">
                        <img class="cover-image" src="{{'/assets/cover_images/' | append: publication.cover_image | relative_url }}" />
                    </div>
                    {% endif %}
                </div>
                {% endfor %}
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Academic Services</p>
            <p>
                Reviewer for CVPR 2022/ECCV 2022
            </p>
        </div>
    </div>
    <div class="row">
        <div class="col">
            <p class="h4 section-title">Side Projects</p>
            <p><a href="https://github.com/TonyLianLong/Rainbow">Rainbow</a>: An implementation of Rainbow algorithm with PARL reinforcement learning framework.</p>
            <p><a href="https://github.com/TonyLianLong/AnimeGAN.js">AnimeGAN.js</a>: An implementation of AnimeGAN with tf.js, which converts photos to anime style online.</p>
        </div>
    </div>
</main>

<footer class="footer">
    <div class="container-sm">
        <div class="row">
            <div class="col" style="text-align: center">
                <span class="text-muted">
                    Feel free to use the <a href="https://github.com/TonyLianLong/websitev2">source code</a> of this website. Referencing designs from <a href="https://github.com/HaozhiQi/haozhiqi.github.io/">Haozhi Qi</a> and <a href="https://github.com/jonbarron/website">Jon Barron</a>. The fonts are based on <a href="https://checkmyworking.com/cm-web-fonts/">this</a> project. Uses <a href="https://github.com/jekyll/jekyll">Jekyll</a> and <a href="https://getbootstrap.com/">Bootstrap</a>.
                </span>
            </div>
        </div>
    </div>
</footer>
