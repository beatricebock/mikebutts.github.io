---
layout: default
title: Codelegy Blog
---
{% include JB/setup %}


{% for post in site.posts %}
		 {{post.title}}
		 


<div class="row">
    <div class="col-md-8 blog-column">
        <div class="view overlay hm-blue-slight z-depth-2">
            <a><img src="https://mdbootstrap.com/images/slides/slide%20(13).jpg" class="img-responsive">
                <div class="mask waves-effect waves-light "></div>
            </a>
        </div>

        <div class="card-panel bl-panel text-center hoverable">
            <a href=""><h3 class="black-text">{{post.title}} <i class="material-icons">chevron_right</i></h3></a>
            <h5>Written by <a href="#">{{post.author}}</a> | {{ post.date | date: "%m/%d/%Y" }}</h5>
            <!--Social Counter-->
            <div class="hidden-xs">
                <a class="btn-sm-full fb-bg rectangle waves-effect waves-light"><i class="fa fa-facebook"> </i> <span>Facebook</span> </a><span class="badge social-counter"></span>
                <a class="btn-sm-full tw-bg rectangle waves-effect waves-light"><i class="fa fa-twitter"> </i> <span>Twitter</span></a><span class="badge social-counter"></span>
                <a class="btn-sm-full gplus-bg rectangle waves-effect waves-light"><i class="fa fa-google-plus"> </i> <span>Google +</span></a><span class="badge social-counter"></span>
                <a class="btn-sm-full comm-bg rectangle waves-effect waves-light"><i class="fa fa-comments"> </i> <span>Comments</span></a><span class="badge social-counter"></span>
            </div>
            <!--/.Social Counter-->
            <!--Social Counters for mobile-->
            <div class="visible-xs">
                <span class="counter-wrapper">
                <a class="btn-sm fb-bg rectangle waves-effect waves-light">
                <i class="fa fa-facebook"> </i>
                </a>
                <span class="badge social-counter">5</span>
                </span>

                <span class="counter-wrapper">
                <a class="btn-sm tw-bg rectangle waves-effect waves-light">
                <i class="fa fa-twitter"> </i>
                </a>
                <span class="badge social-counter">5</span>
                </span>

                <span class="counter-wrapper">
                <a class="btn-sm gplus-bg rectangle waves-effect waves-light">
                <i class="fa fa-google-plus"> </i>
                </a>
                <span class="badge social-counter">5</span>
                </span>
                <span class="counter-wrapper">
                <a class="btn-sm comm-bg rectangle waves-effect waves-light">
                <i class="fa fa-comments"> </i>
                </a>
                <span class="badge social-counter">5</span>
                </span>
            </div>
            <!--/.Social Counters for mobile-->
            <hr>
            <p class="text-left">{{Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni, perspiciatis, fugit! Deleniti, voluptatem, officia! Error, voluptate eaque ex, aperiam quo tempora, veritatis aspernatur voluptatum nesciunt a distinctio provident numquam quisquam. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio, incidunt odio saepe! Voluptate fugiat nihil debitis, excepturi soluta cumque aut harum quibusdam ratione quod, quia, vel, consectetur autem! Rem, corrupti!}}</p>
        </div>
    </div>
</div>
<!--/.Post row-->
{% endfor %}