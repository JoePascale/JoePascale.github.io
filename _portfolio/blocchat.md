layout: post
title: Bloc Chat
thumbnail-path: "pictures/beethoven.jpg"
short-description: Bloc Chat is an online chat room application that allows you to connect with all your friends!


Summary

I used AngularJS to make this chat room application simple, easy to use, and have a clean-looking UI.

Explanation

This project was created because chat rooms should be as simple and user-friendly as possible.

Problem

The problem with a lot of chat apps is that they request a full page refresh from the server every time the user does something. No need to reload assets when a user really only needs to see the most recent rooms & messages.

Solution

My solution to this problem was to leverage AngularJS and create specific "states" of the application where we are only requesting some bits of data at a time, depending on what room you are in.  This means the application is much more responsive, the end user doesn't have to have a huge amount of memory, and they also have less chance for errors resulting in huge packet requests.

Results

The result is the user sees less but gets more, with regards to user-experience, and doesn't need the latest greatest hardware & memory to get that experience.

Conclusion

This was my second AngularJS project.  I learned a lot about how to query a backend database and only show what is needed (i.e. messages tied to only the room you are in).  I plan on using Firebase and AngularJs a lot more in the future to expand upon this knowledge.



{:.center}
![]({{ site.baseurl }}/pictures/beethoven.jpg)



{% highlight javascript %}
Message.getByRoomId = function(roomId) {
      // Filter the messages by their room ID.
      ref.orderByChild('roomId').equalTo(roomId).on('value', function(snapshot) {
          return snapshot.val();
      });
    };
{% endhighlight %}