layout: post
title: BlocJams
thumbnail-path: "pictures/bloc_jams_logo.png"
short-description: BlocJams is a streaming music application where you can play all your favorite jams!


Summary

There are so many streaming music applications out there, but the aim of this particular streaming music project was to make it concise, responsive, and very user-friendly.

Explanation

I sought out to create this application with the end user in mind.  It was a Bloc project that I was taked with completing, but also represents my very first hands-on project with utilizing the Javascript language and jQuery library.

Problem

I think the biggest problem with current streaming music applications is that if they are user-friendly, they are normally very taxing on the end user's memory resources, and if they aren't user-friendly, well you're putting a burden on the user to figure out how to use something that doesn't need to be that complicated.

Solution

My solution to this problem was to leverage memory-friendly Javascript functions that didn't place a burden on the end user, while also keeping the application simple by leveraging jQuery methods to refer to elements in the app.

Results

The result is a user-friendly app that doesn't put such a burden on the user and also makes the experience seamless & familiar.  No sense in trying to reinvent the wheel when we can just make it more efficient.

Conclusion

It was easy to keep this project simple by focusing on limiting the lines of code necessary by introducing the jQuery library and also avoiding verbose Javascript.  What surprised me was how simple I could keep the app, but still have loads of unique functionality.  I learned that there are very often easier ways to do something complex, by writing a function one time, and then looking at the individual parts where an improvement or enhancement might be possible.  I plan on leveraging that ability to "look at the whole as simpler pieces" in future projects.



{:.center}
![]({{ site.baseurl }}/pictures/bloc_jams_bg.jpg)



{% highlight javascript %}
var onHover = function(event) {
        var songNumberCell = $(this).find('.song-item-number');
        var songNumber = parseInt(songNumberCell.attr('data-song-number'));

        if (songNumber !== currentlyPlayingSongNumber) {
            songNumberCell.html(playButtonTemplate);
        }
    };
{% endhighlight %}