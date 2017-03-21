---
title: Codelegy Blog
layout: default
---

{% include JB/setup %}


<!--
{% for post in site.posts %}
		 {{post.title}}
		 

{% endfor %}
-->

<main>
        <!--Main layout-->
        <div class="container">
            <div class="row">

                <!--Main column-->
                <div class="col-lg-8">
                    {% for post in site.posts %}
                    <!--Post-->
                    <div class="post-wrapper">
                        <!--Post data-->
                        <h1 class="h1-responsive">{{post.title}} <small class="text-muted">{{post.tagline}}</small></h1>
                        <h5>Written by <a href="">{{post.author}}</a>, {{post.date | date_to_long_string }}</h5>

                        <br>

                        <!--Featured image -->
                        <div class="view overlay hm-white-light z-depth-1-half">
                            <img src="{{post.main_img}}" class="img-fluid img-responsive main-image" alt="{{post.img_main_alt}}" ma>
                            <div class="mask">
                            </div>
                        </div>

                        <br>

                        <!--Post excerpt-->
                        <p>{{post.excerpt}}</p>

                        <!--"Read more" button-->
                        <a class="btn btn-info waves-effect waves-light" href="{{ site.baseurl }}{{ post.url }}">Read more</a>
                    </div>
                    <!--/.Post-->
                    {% endfor %}
                    <hr>    
                    <hr>

                    <!--Pagination-->
                    <nav>
                        <ul class="pagination flex-center pg-dark">
                            <!--Arrow left-->
                            <li class="page-item">
                                <a class="page-link waves-effect waves-effect" aria-label="Previous">
                                    <span aria-hidden="true">«</span>
                                    <span class="sr-only">Previous</span>
                                </a>
                            </li>

                            <!--Numbers-->
                            <li class="page-item active"><a class="page-link waves-effect waves-effect">1</a></li>
                            <li class="page-item"><a class="page-link waves-effect waves-effect">2</a></li>
                            <li class="page-item"><a class="page-link waves-effect waves-effect">3</a></li>
                            <li class="page-item"><a class="page-link waves-effect waves-effect">4</a></li>
                            <li class="page-item"><a class="page-link waves-effect waves-effect">5</a></li>

                            <!--Arrow right-->
                            <li class="page-item">
                                <a class="page-link waves-effect waves-effect" aria-label="Next">
                                    <span aria-hidden="true">»</span>
                                    <span class="sr-only">Next</span>
                                </a>
                            </li>
                        </ul>
                    </nav>
                    <!--/.Pagination-->

                </div>
 {% assign categories_list = site.categories %}  
                <!--Sidebar-->
                <div class="col-lg-4">

                    <div class="widget-wrapper">
                        <h4>Categories:</h4>
                        <br>
                        <div class="list-group">
                           {% for category in categories_list %} 
                            <a href="#" class="list-group-item" href="{{ BASE_PATH }}{{ site.JB.categories_path }}#{{ category[0] }}-ref">{{ category[0] | join: "/" }}</a>
                            {% endfor %} 
                        </div>
                    </div>
                    <div>
                    	<a class="twitter-timeline" href="https://twitter.com/codelegy">Tweets by codelegy</a> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
                    </div>
<!--

  <div class="widget-wrapper">
    <h4>Subscription form:</h4>
    <br>
    <div class="card">
       <div class="card-block">
           <p><strong>Subscribe to our newsletter</strong></p>
           <p>Once a week we will send you a summary of the most useful news</p>
           <div class="subscribe-form ml-block-success" style="display:none">
               <div class="form-section">
                  <h4>Newsletter</h4>
                  <p>Thank you! You have successfully subscribed to our newsletter.</p>
              </div>
          </div>
          <form class="ml-block-form" action="//app.mailerlite.com/webforms/submit/l2x1a1" data-id="344185" data-code="l2x1a1" method="POST" target="_blank">
           <div class="md-form">
               <i class="fa fa-user prefix"></i>
               <input type="text" name="fields[name]" class="form-control" placeholder="Name" value="" autocomplete="name" x-autocompletetype="name" spellcheck="false" autocapitalize="off" autocorrect="off" id="form1">
               <label for="form1">Your name</label>
           </div>
           <div class="md-form">
               <i class="fa fa-envelope prefix"></i>
               <input type="email" name="fields[email]" class="form-control" placeholder="Email*" value="" autocomplete="email" x-autocompletetype="email" spellcheck="false" autocapitalize="off" autocorrect="off" id="form2">
               <label for="form2">Your email</label>
           </div>
           <button class="btn btn-info waves-effect waves-light">Submit</button>
           <button disabled="disabled" style="display: none;" type="button" class="loading">
               <img src="//static.mailerlite.com/images/rolling.gif" width="20" height="20" style="width: 20px; height: 20px;">
           </button>
          </form>
       </div>
   </div>
</div>
<script>
  function ml_webform_success_4516083() {
     var $ = ml_jQuery || jQuery;

     $('.ml-subscribe-form-4516083 .ml-block-success').show();
     $('.ml-subscribe-form-4516083 .ml-block-form').hide();
 };
</script>
<script type="text/javascript" src="//static.mailerlite.com/js/w/webforms.min.js?v98f07ba3d85ef7eb5404a058e826ec34"></script>
                 
-->

                </div>
                <!--/.Sidebar-->
            </div>
        <!--/.Main layout--></div>
        

    </main>
	
	
	
	