---
title: "Background"
layout: splash
permalink: /background/
---
<style>
.flex-container {
    display: flex;
}
.flex-child {
    flex: 1;
    margin-right: 4px
}  
</style>
{% assign author = page.author | default: page.authors[0] | default: site.author %}
{% assign author = site.data.authors[author] | default: author %}
<br>

# Background

Aeon Sharp is the pseudonym of Nicholas Duque, audio engineer and vocalist based in central California.

My sound emerged from a unique path: As a teenager, I taught myself music theory and composition, scoring neo-classical chamber music that I began uploading to SoundCloud and BandCamp in 2010. A love for songs, video games and digital worlds led me to Vocaloid, with my personal projects over the following years often incorporating synthesized vocals alongside industrial synths, analog synths, and my own live vocals. Also a lover of experimentation, I enjoy playing with samples of things like dial-up modems, movie quotes, and other unique electronic sounds.

I would later go on to refine my skills formally, receiving a Bachelor’s degree in Music Technology in 2019. My training and subsequent professional experience included live sound and recording engineering, Operatic and choral vocals, and hands-on experience in scoring for animation, which easily melded with my natural curiosity and love for experimental forms of expression.

This all led to the development of my hybrid style; a proficiency in classical arrangements, industrial pop, and anywhere in between.

<div class="flex-container">
  <div class="flex-child">
    <h2>Explore my portfolio:</h2>
    <div class="author__urls-wrapper">
      <ul class="author__urls social-icons">
        {% if author.links %}
          {% for link in author.links %}
            {% if link.link_category contains 'portfolio' %}
              {% if link.label and link.url %}
                <li><a href="{{ link.url }}" rel="nofollow noopener noreferrer me"{% if link.url contains 'http' %} itemprop="sameAs"{% endif %}><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i><span class="label">{{ link.label }}</span></a></li>
              {% endif %}
            {% endif %}
          {% endfor %}
        {% endif %}
      </ul>
    </div>
  </div>

  <div class="flex-child">
    <h2>Connect on social media:</h2>
    <div class="author__urls-wrapper">
      <ul class="author__urls social-icons">
        {% if author.links %}
          {% for link in author.links %}
            {% if link.link_category contains 'social' %}
              {% if link.label and link.url %}
                <li><a href="{{ link.url }}" rel="nofollow noopener noreferrer me"{% if link.url contains 'http' %} itemprop="sameAs"{% endif %}><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i><span class="label">{{ link.label }}</span></a></li>
              {% endif %}
            {% endif %}
          {% endfor %}
        {% endif %}
      </ul>
    </div>
  </div>
  <div class="flex-child">
    <h2>Get in touch:</h2>
    <div class="author__urls-wrapper">
      <ul class="author__urls social-icons">
        <li><a href="mailto:{{ author.email }}" rel="nofollow noopener noreferrer me"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i><span class="label">Email</span></a></li>
      </ul>
    </div>
  </div>
</div>