---
layout: default
---
<div class="container-fluid">
    <nav class="navbar navbar-expand navbar-light">
            <div class="navbar-brand"><img src="img/logo.svg" style="height: 100%; max-height: 40px; max-width: 20vw;" alt="ikovylyaev-logo"></div>
        
              <div class="collapse navbar-collapse" id="main-nav">
                <ul class="navbar-nav me-auto" style="position: absolute; right: 0px;;">
                  <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="{{site.url}}">ru</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" href="{{site.url}}/en">en</a>
                  </li>
                </ul>
              </div>
          </nav>
        <h1 class="display-2" style="text-align: right; margin-top: 20vh; font-weight: 200!important;">иван<br>ковыляев</h1>
        {% for post in site.posts limit: 1 %}
        {% if post.type == 'design' %}
            {% if post.link == 'null' %}
                <a href="#">
            {% else %}
                <a target="blank" href="{{post.link}}">
            {% endif %}
            <div class="header-image" style="background: url({{site.url}}/img/bg/{{post.img}}.webp); background-size: cover; background-position: center;">
            </div>
            <h2 class="display-4" style="margin-top: 20px;">{{ post.title-ru }}</h2>
            <p>
                {% if post.concept == 'concept' %}
                 <span style="margin-right: 50px;">концепт</span>
                {% endif %}
                <span>{{ post.categories-ru }}</span>
            </p>
        </a>
        {%endif%}
        {% endfor %}
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="display-4">обо мне</h2>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                <p>я - иван ковыляев. дизайнер-фрилансер родом из екатеринбурга, но живущий в санкт-петербурге. специализируюсь на графическом и ui/ux дизайне. </p>
                <a href="https://disk.yandex.ru/i/N0AnN-6GTr-ttQ" style='margin-right: 50px;'>презентация</a>
           
            </div>
        </div>
        <div class="row" style="margin-top: 10vh;">
            {% for post in site.posts limit: 4 offset: 1 %}
            {% if post.type == 'design' %}
            {% if post.link == 'null' %}
                <div class="col-md-6 col-sm-12">
            {% else %}
                <a href="{{post.link}}" target="blank" class="col-md-6 col-sm-12">
            {% endif %}
                <img src="{{site.url}}/img/bg/{{post.img}}.webp" style="width: 100%;" alt="{{post.title}}">
                <h2 style="margin-top: 20px;">{{ post.title-ru }}</h2>
                <p>
                {% if post.concept == 'concept' %}
                 <span style="margin-right: 50px;">концепт</span>
                {% endif %}
                <span>{{ post.categories-ru }}</span>
            </p>
            {% if post.link == 'null' %}
                </div>
            {% else %}
                </a>
            {% endif %}
            {%endif%}
            {% endfor %}
        </div>
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="display-4">инвентарь</h2>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                <a href="https://drive.google.com/drive/folders/18AbQ0FsPcc2yzV1IkBHfUVSqIdPR6z-S?usp=sharing" target="blank">карта санкт-петербургского метрополитена</a><br>
                <a href="https://drive.google.com/drive/folders/1F7pfxSSwSZ-sZ7Hl0UA8CyZafdK0g1N0?usp=sharing" target="blank">логотип санкт-петербургского метрополитена</a><br>
            </div>
        </div>
        <div class="row" style="margin-top: 10vh;">
            {% for post in site.posts offset: 5 limit: 4 %}
            {% if post.type == 'design' %}
            {% if post.link == 'null' %}
                <div class="col-md-6 col-sm-12">
            {% else %}
                <a href="{{post.link}}" target="blank" class="col-md-6 col-sm-12">
            {% endif %}
                <img src="{{site.url}}/img/bg/{{post.img}}.webp" style="width: 100%;" alt="{{post.title}}">
                <h2 style="margin-top: 20px;">{{ post.title-ru }}</h2>
                <p>
                {% if post.concept == 'concept' %}
                 <span style="margin-right: 50px;">концепт</span>
                {% endif %}
                <span>{{ post.categories-ru }}</span>
            </p>
            {% if post.link == 'null' %}
                </div>
            {% else %}
                </a>
            {% endif %}
            {%endif%}
            {% endfor %}
        </div>
        
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="display-4">тупичок эволюции</h2>
                <p>блог о дизайне и не только</p>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                {% for post in site.posts %}
                    {% if post.type == 'blog' %}
                        <a href="{{ post.url }}">{{ post.title }}</a><br>
                    {% endif %}
                {% endfor %}
            </div>
        </div>
        <div class="row" style="margin-top: 10vh;">
            {% for post in site.posts offset: 9 %}
            {% if post.type == 'design' %}
            {% if post.link == 'null' %}
                <div class="col-md-6 col-sm-12">
            {% else %}
                <a href="{{post.link}}" target="blank" class="col-md-6 col-sm-12">
            {% endif %}
                <img src="{{site.url}}/img/bg/{{post.img}}.webp" style="width: 100%;" alt="{{post.title}}">
                <h2 style="margin-top: 20px;">{{ post.title-ru }}</h2>
                <p>
                {% if post.concept == 'concept' %}
                 <span style="margin-right: 50px;">концепт</span>
                {% endif %}
                <span>{{ post.categories-ru }}</span>
            </p>
            {% if post.link == 'null' %}
                </div>
            {% else %}
                </a>
            {% endif %}
            {%endif%}
            {% endfor %}
        </div>
        
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="display-4">другие проекты</h2>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                <p><a href="http://video.ikovylyaev.com">фото и видео</a></p>
                <p><a href="http://nature.ikovylyaev.com">урал</a></p>
            </div>
        </div>
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="display-4">контакты</h2>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                <p><span style="opacity: 0.5; margin-right: 25px">mail</span><a href="mailto:hi@ikovylyaev.com">hi@ikovylyaev.com</a></p>
                <p><span style="opacity: 0.5; margin-right: 25px">behance</span><a href="https://behance.net/ikovylyaev">ikovylyaev</a></p>
                <p><span style="opacity: 0.5; margin-right: 25px">vk</span><a href="https://vk.com/ikovylyaev">ikovylyaev</a></p>
                <p><span style="opacity: 0.5; margin-right: 25px">instagram</span><a href="https://instagram.com/ikovylyaev">ikovylyaev</a></p>
                <p><span style="opacity: 0.5; margin-right: 25px">youtube</span><a href="https://www.youtube.com/channel/UCf9GOVc0qKKPB-Ee3LfH_uw">иван ковыляев</a></p>
            </div>
        </div>
        <div class="row" style="margin-top: 10vh;">
            <div class="col-sm-12 col-md-5">
                <h2 class="h1">правовая информация</h2>
            </div>
            <div class="col-sm-11 offset-sm-1 col-md-7 offset-md-0 mt-3">
                <p><a href="{{ site.url }}/privacy/" style="margin-right: 25px">политика конфиденциальности</a></p>
                <p><a href="{{ site.url }}/terms/" style="margin-right: 25px">правила использования</a></p>
                <p><a href="{{ site.url }}/domain/" style="margin-right: 25px">информация о домене</a></p>
            </div>
        </div>
    </div>
    
