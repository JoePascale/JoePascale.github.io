layout: post
title: BlocJams AngularJS
thumbnail-path: "pictures/bloc_jams_logo.png"
short-description: BlocJams AngularJS is a streaming music application where you can play all your favorite jams!


Summary

There are so many streaming music applications out there, but the aim of this particular streaming music project was to make it concise, responsive, and very user-friendly by leveraging AngularJS and improving upon the vanilla JS version.

Explanation

This project was intended to have very similar functionality to my previous Bloc Jams project, but rather leverage AngularJS and specific "states" so that I could make the end user experience even simpler.

Problem

The problem with a lot of streaming music apps is that they request a full page refresh from the server every time the user does something. Why reload a huge amount of assets and put a strain on the end user's memory when we really only need one or two bits of data?

Solution

My solution to this problem was to leverage AngularJS and create specific "states" of the application where we are only requesting some bits of data at a time.  This means the application is much more responsive, the end user doesn't have to have a huge amount of memory, and they also have less chance for errors resulting in huge packet requests.

Results

The result is the same user-friendly Bloc Jams app as before, but now the user gets faster experience that utilizes much less memory!

Conclusion

This was my first experience using AngularJS in a project and I have to say I still have a lot to learn, but I can definitely see how powerful the framework is.  My code is much more concise, it took me much less time to create functions, and I didn't have to keep rewriting very similar bits of code.  I definitely plan on sharpening my skills in Angular in the future!



{:.center}
![]({{ site.baseurl }}/pictures/bloc_jams_bg.jpg)



{% highlight javascript %}
(function() {
    function SongPlayer($rootScope, Fixtures) {
        var SongPlayer = {};

...
    angular
         .module('blocJams')
         .factory('SongPlayer', ['$rootScope', 'Fixtures', SongPlayer]);
 })();
{% endhighlight %}