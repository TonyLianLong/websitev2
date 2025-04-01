---
layout: default
title: "Long (Tony) Lian's Personal Website"
---

<div class="row">
    <div class="col-md-8">
        <h1 class="page-title">
            <img class="profile-img-small d-md-none" src="{{ '/assets/profile.jpg' | relative_url }}" alt="Long (Tony) Lian" />
            Long (Tony) Lian
        </h1>
        <div class="social-links">
            <a href="mailto:longlian@berkeley.edu" title="Email"><i class="fas fa-envelope"></i></a>
            <a href="https://scholar.google.com/citations?user=eOLxyqUAAAAJ" title="Google Scholar"><i class="fas fa-graduation-cap"></i></a>
            <a href="https://twitter.com/LongTonyLian" title="Twitter"><i class="fab fa-twitter"></i></a>
            <a href="https://www.linkedin.com/in/longlian" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="https://github.com/TonyLianLong" title="GitHub"><i class="fab fa-github"></i></a>
        </div>
        <section id="about" class="mt-4">
            <!-- <h2 class="section-title">About</h2> -->
            {% capture bio %}{% include bio.md %}{% endcapture %}
            <div class="bio-content">
                {{ bio | markdownify }}
            </div>
        </section>
    </div>
    <div class="col-md-4">
        <img class="profile-img d-none d-md-block" src="{{ '/assets/profile.jpg' | relative_url }}" alt="Long (Tony) Lian" />
    </div>
</div>

<section id="publications" class="mt-5">
    <h2 class="section-title">Publications <span class="h6">(*: equal contribution)</span></h2>
    <div class="publications-list">
        {% assign sorted_publications = site.publications | sort:"date" %}
        {% for publication in sorted_publications reversed %}
        <div class="publication-item mb-4">
            <div class="row">
                <div class="col-md-7">
                    <h3 class="publication-title">{{ publication.title }}</h3>
                    <div class="publication-authors">{{publication.authors | markdownify}}</div>
                    {% if publication.venue %}
                        <div class="publication-venue">{{publication.venue | markdownify}}</div>
                    {% endif %}
                    <div class="publication-excerpt" style="display: none">{{publication.excerpt | markdownify}}</div>
                    {% if publication.paper_url %}
                    <div class="publication-links">
                        <a href="{{publication.paper_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-file-alt"></i> Paper</a>
                        {% if publication.blog_url %}<a href="{{publication.blog_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-blog"></i> Blog</a>{% endif %}
                        {% if publication.project_page_url %}<a href="{{publication.project_page_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-project-diagram"></i> Project</a>{% endif %}
                        {% if publication.demo_url %}<a href="{{publication.demo_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-play-circle"></i> Demo</a>{% endif %}
                        {% if publication.video_url %}<a href="{{publication.video_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-video"></i> Video</a>{% endif %}
                        {% if publication.demo_video_url %}<a href="{{publication.demo_video_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-film"></i> Demo Video</a>{% endif %}
                        {% if publication.code_url %}<a href="{{publication.code_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-code"></i> Code</a>{% endif %}
                        {% if publication.poster %}<a href="{{'/assets/posters/' | append: publication.poster | relative_url }}" class="btn btn-outline-primary btn-sm"><i class="fas fa-file-image"></i> Poster</a>{% endif %}
                        {% if publication.bibtex_url %}<a href="{{publication.bibtex_url}}" class="btn btn-outline-primary btn-sm"><i class="fas fa-quote-right"></i> BibTex</a>{% endif %}
                        {% if publication.excerpt %}<a href="#" class="btn btn-outline-primary btn-sm tldr_btn"><i class="fas fa-info-circle"></i> TL;DR</a>{% endif %}
                    </div>
                    {% endif %}
                </div>
                {% if publication.cover_image %}
                <div class="col-md-5 d-none d-md-block">
                    <img class="cover-image" src="{{'/assets/cover_images/' | append: publication.cover_image | relative_url }}" alt="{{ publication.title }}" />
                </div>
                {% endif %}
            </div>
        </div>
        {% endfor %}
    </div>
</section>

<section id="services" class="mt-5">
    <h2 class="section-title">Academic Services</h2>
    <div class="services-content">
        <p>Reviewer for CVPR/ECCV/ICCV/ICLR/ICML/NeurIPS/AAAI</p>
    </div>
</section>

<section id="projects" class="mt-5">
    <h2 class="section-title">Side Projects</h2>
    <div class="projects-list">
        <div class="project-item mb-4">
            <h3 class="project-title">Stable Diffusion XL Demo WebUI</h3>
            <p>A gradio-based WebUI that allows playing around with <a href="https://arxiv.org/abs/2307.01952">SDXL</a> locally and on Colab for free.</p>
            <div class="publication-links">
                <a href="https://github.com/TonyLianLong/stable-diffusion-xl-demo" class="btn btn-outline-primary btn-sm"><i class="fas fa-code"></i> Code</a>
                <a target="_blank" href="https://colab.research.google.com/github/TonyLianLong/stable-diffusion-xl-demo/blob/main/Stable_Diffusion_XL_Demo.ipynb" class="btn btn-outline-primary btn-sm"><i class="fas fa-play-circle"></i> Demo</a>
            </div>
        </div>
        <div class="project-item mb-4">
            <h3 class="project-title">AnimeGAN.js</h3>
            <p>An implementation of AnimeGAN, which converts photos to anime style online, with <a href="https://github.com/tensorflow/tfjs">tf.js</a>.</p>
            <div class="publication-links">
                <a href="https://github.com/TonyLianLong/AnimeGAN.js" class="btn btn-outline-primary btn-sm"><i class="fas fa-code"></i> Code</a>
                <a target="_blank" href="https://animegan.js.org/" class="btn btn-outline-primary btn-sm"><i class="fas fa-play-circle"></i> Demo</a>
            </div>
        </div>
        <div class="project-item mb-4">
            <h3 class="project-title">Rainbow</h3>
            <p>An implementation of Rainbow algorithm with <a href="https://github.com/PaddlePaddle/PARL">PARL</a> reinforcement learning framework.</p>
            <div class="publication-links">
                <a href="https://github.com/TonyLianLong/Rainbow" class="btn btn-outline-primary btn-sm"><i class="fas fa-code"></i> Code</a>
            </div>
        </div>
    </div>
</section>
