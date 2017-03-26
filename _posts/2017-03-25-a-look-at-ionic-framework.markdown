---
title: A look at Ionic framework
date: 2017-03-25 23:04:00 -04:00
---

<article><div id="preblock"><div id="previewdiv"><p><a href="[https://mikelols.wordpress.com/2015/09/29/a-sprint-through-ionic-framework/](https://mikelols.wordpress.com/2015/09/29/a-sprint-through-ionic-framework/)" title="Permalink to A sprint through Ionic framework! – Mike Lols">Source</a></p>\
<h1 id="asprintthroughionicframework–mikelols">A sprint through Ionic framework! – Mike Lols</h1>\
<figure><img src="[https://mikelols.files.wordpress.com/2015/09/ionic-samples.png?w=300&h=118](https://mikelols.files.wordpress.com/2015/09/ionic-samples.png?w=300&h=118)" alt="ionic-samples" id="1" /><figcaption>ionic-samples</figcaption></figure>\
<p>Ionic sample apps</p>\
<p>VCS students were allotted 22 hours to learn a new skill that was some what related to development. 22 hours sounds like a pretty good amount of time but realistically, looking through the many options: socket, node, meteor, closure, jasmine, d3, react, backbone/knockout, etc etc etc , you see the picture. After looking at some options I settled on Ionic Mobile framework.</p>\
<p>Ionic is a mobile framework based on AngularJS, and with 9 actual code hours it was a good choice to dive into. Ionic can be built to use via the web, or you can easily compile android or ios versions.</p>\
<p>Starting an Ionic app:</p>\
<p>To start ionic you need to install:</p>\
<blockquote><p>First, install <a href="[http://nodejs.org/](http://nodejs.org/)">Node.js</a>. Then, install the latest Cordova and Ionic <a href="[https://npmjs.org/package/ionic](https://npmjs.org/package/ionic)">command-line tools</a>. Follow the <a href="[http://cordova.apache.org/docs/en/3.3.0/guide_platforms_android_index.md.html#Android%20Platform%20Guide](http://cordova.apache.org/docs/en/3.3.0/guide_platforms_android_index.md.html#Android%20Platform%20Guide)">Android</a> and <a href="[http://cordova.apache.org/docs/en/3.3.0/guide_platforms_ios_index.md.html#iOS%20Platform%20Guide](http://cordova.apache.org/docs/en/3.3.0/guide_platforms_ios_index.md.html#iOS%20Platform%20Guide)">iOS</a> platform guides to install required platform dependencies.</p></blockquote>\
<p>When developing I was using my Windows PC so I developed with an Android emulator using Android Studio. The emulator was awfully slow so I ended up switching to Genymotion which was much better.</p>\
<p><img src="[https://mikelols.files.wordpress.com/2015/09/lab.png?w=300&h=252](https://mikelols.files.wordpress.com/2015/09/lab.png?w=300&h=252)" alt="lab" id="6" />In the CMD.exe running ionic start myApp gets you started with a sample app followed up by a ionic serve –lab will run the app in your browser with real time updates. The “–lab” allows you to see what your app would run like on both Android and iOS.</p>\
<pre><code>&amp;lt;body ng-app=&quot;mustHaveCoffee&quot; &amp;gt;\
\&amp;amp;lt;ion-pane ng-controller=&quot;YelpController&quot;&amp;gt; &amp;lt;ion-header-bar class=&quot;bar-stable&quot; &amp;gt;\
\&amp;amp;lt;h1 class=&quot;title&quot; &amp;gt; &amp;lt;img src='https://mikelols.wordpress.com/img/coffee-bean-icon.png' /&amp;gt; &amp;lt;span &amp;gt;MustFindCoffee&amp;lt;/span &amp;gt; &amp;lt;/h1 &amp;gt; &amp;lt;/ion-header-bar &amp;gt; &amp;lt;ion-content &amp;gt;\
\&amp;lt;ion-refresher pulling-text=&quot;OW!..I'm working on it..&quot; on-refresh=&quot;doRefresh()&quot;&amp;gt; &amp;lt;/ion-refresher&amp;gt;\
\&amp;lt;ion-list &amp;gt; &amp;lt;ion-item ng-repeat=&quot;cafe in yelp.results&quot; class=&quot;item-thumbnail-left&quot; ng-click=&quot;openMap(cafe)&quot;&amp;gt;\
\&amp;lt;img ng-src=&quot;{{cafe.image_url}}&quot; &amp;gt;\
\&amp;amp;lt;h2 &amp;gt;{{cafe.name}}&amp;lt;/h2 &amp;gt;\
\&amp;lt;span &amp;gt; &amp;lt;i class=&quot;ion ion-ios-navigate&quot; &amp;gt;&amp;lt;/i &amp;gt; {{cafe.distance | number:&quot;0&quot;}}m&amp;lt;/span &amp;gt;\
\&amp;lt;i class=&quot;ion ion-ios-location&quot; &amp;gt;&amp;lt;/i &amp;gt; {{cafe.location.display_address | join: &quot;, &quot;}}\
\&amp;lt;i class=&quot;ion ion-ios-telephone&quot;&amp;gt;&amp;lt;/i&amp;gt; {{cafe.display_phone }}\
\&amp;lt;span &amp;gt; &amp;lt;i class=&quot;ion ion-star&quot; &amp;gt;&amp;lt;/i &amp;gt; {{cafe.rating}}&amp;lt;/span &amp;gt;\
\&amp;lt;span &amp;gt; &amp;lt;i class=&quot;ion ion-person&quot; &amp;gt;&amp;lt;/i &amp;gt; {{cafe.review_count}}&amp;lt;/span &amp;gt;\
\&amp;lt;ion-option-button class=&quot;button-positive&quot; ng-click=&quot;getDirections(cafe)&quot;&amp;gt; &amp;lt;i class=&quot;ion ion-map&quot;&amp;gt;&amp;lt;/i&amp;gt;&amp;amp;nbsp; map &amp;lt;/ion-option-button&amp;gt; &amp;lt;/ion-item &amp;gt; &amp;lt;/ion-list &amp;gt;\
\&amp;lt;!-- checks to see if it is at the end of the page if it is then it will get the next page --&amp;gt;\
\&amp;lt;ion-infinite-scroll ng-if=&quot;yelp.hasMore&quot; on-infinite=&quot;loadMore()&quot;&amp;gt; &amp;lt;/ion-infinite-scroll&amp;gt;\
\&amp;lt;/ion-content &amp;gt;\
\&amp;amp;lt;/ion-pane &amp;gt;&amp;lt;/body &amp;gt;</code></pre>\
<p><img src="[https://mikelols.files.wordpress.com/2015/09/ionic-refresher.png?w=134&h=300](https://mikelols.files.wordpress.com/2015/09/ionic-refresher.png?w=134&h=300)" alt="ionic-refresher" id="7" />When you work in Ionic, you essentially build an app in AngularJS as you normally would but when building the front end you use ionic’s syntax. Some quick examples include<br/>ion-refresher and ion-infinite scroll. When you pull your browser down on the phone, you can trigger a function that you would setup to return a promise. You would write something akin to:</p>\
<blockquote><p>$scope.yelp.refresh().then(function(){$scope.$broadcast(‘scroll.refreshComplete’);}</p></blockquote>\
<p>Broadcast tells Ionic that it can now stop the refreshing icon, or if for the case of using infinite scroll to load paginated data you would use $scope.$broadcast(‘scroll.infiniteScrollComplete’), which would load the data and end the refresh icon.</p>\
<p><img src="[https://mikelols.files.wordpress.com/2015/09/ionoption.jpg?w=196&h=300](https://mikelols.files.wordpress.com/2015/09/ionoption.jpg?w=196&h=300)" alt="IonOption" id="8" />Another rapid development feature of Ionic is using the ion-option directive. You can easily ad a ng-click() on a button inside of the ion-option and BAM you have a div you can slide over and click the button inside. You can put multiple buttons in it as well. Keep in mind if this is a list you can have the slide div and the button inside as clickable. These are just a couple of the many directives that Ionic has built in for rapid development.</p>\
<figure><img src="[https://mikelols.files.wordpress.com/2015/09/sidemenu.gif?w=217&h=300](https://mikelols.files.wordpress.com/2015/09/sidemenu.gif?w=217&h=300)" alt="sidemenu" id="9" /><figcaption>sidemenu</figcaption></figure>\
<p>Quick and easy menus!</p>\
<figure><img src="[https://mikelols.files.wordpress.com/2015/09/screen-shot-2015-09-28-at-3-16-41-am.png?w=300&h=247](https://mikelols.files.wordpress.com/2015/09/screen-shot-2015-09-28-at-3-16-41-am.png?w=300&h=247)" alt="Screen Shot 2015-09-28 at 3.16.41 AM" id="10" /><figcaption>Screen Shot 2015–09–28 at 3.16.41 AM</figcaption></figure>\
<p>Ion icons for your use, hundreds built in.</p>\
<p>One of the things you cannot do with HTML5 is access things like the camera. To access phone hardware you can inject ngCordova.</p>\
<blockquote><p>ngCordova comes with over 70 native Cordova plugins that you can easily add to your Angular Cordova apps. Choose the plugin you’d like to use from the menu, which will have information on which plugin you need to install and an example of how to use it in your Angular code.</p></blockquote>\
<figure><img src="[https://mikelols.files.wordpress.com/2015/09/screen-shot-2015-09-29-at-4-58-41-am.png?w=300&h=236](https://mikelols.files.wordpress.com/2015/09/screen-shot-2015-09-29-at-4-58-41-am.png?w=300&h=236)" alt="Screen Shot 2015-09-29 at 4.58.41 AM" id="11" /><figcaption>Screen Shot 2015–09–29 at 4.58.41 AM</figcaption></figure>\
<p>With directives and plugins you can easily build native full featured apps with the power of Angular.Hopefully this gives a quick insight into the power of Ionic once knowing Angular. I was impressed with Ionic and how quickly I could pick it up. Soon I’ll demo off one of first apps. Got an App idea? Lets build it!</p>\
<p>and always</p>\
<figure><img src="[https://mikelols.files.wordpress.com/2014/10/keep-calm-and-keep-coding-95.png?w=300&h=270](https://mikelols.files.wordpress.com/2014/10/keep-calm-and-keep-coding-95.png?w=300&h=270)" alt="keep-calm-and-keep-coding-95" id="12" /><figcaption>keep-calm-and-keep-coding–95</figcaption></figure>\
<h3 id="likethis:">Like this:</h3>\
<p>Like Loading…</p>\
<h3 id="related"><em>Related</em></h3></div></div></article><footer>