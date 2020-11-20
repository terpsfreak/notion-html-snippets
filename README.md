# notion-html-snippets
Add html snippets to Notion: 
https://blog.shorouk.dev/2020/06/how-to-embed-any-number-of-html-widgets-snippets-into-notion-app-for-free/

Shorouk's Blog

How to embed any number of HTML widgets/snippets into Notion app for free
shorouk Abdelaziz	
Posted by
shorouk Abdelaziz
June 16, 2020
Notion
5 Min Read
embed Notion HTML widget

If you’re using Notion then you probably know that you can’t embed HTML widgets directly into it. I have done some research and I found 2 tools that let you do so.

    htmlsave which is great but only gives you one widget for free and you have to subscribe to add more
    The potion shop which is also great and has no limits on the number of widgets but adds an ad link to your widgets that just bugged me!

In this tutorial, I’ll show you how you can have as many HTML snippets in your Notion page or template as you want and without any extra ads.
step 1 : Making a GitHub repo

First of all, You’ll need a Github account if you don’t have one already then just create a new one.

https://blog.shorouk.dev/wp-content/uploads/2020/06/image-11.png

Once you have your account, go to your profile and click the plus button in the top right corner and choose “New repository”

Give your repository a meaningful name and click “Create repository”. You don’t need to change anything else.

https://blog.shorouk.dev/wp-content/uploads/2020/06/image-12.png

Step 2 : Creating your first widget

Now click on “creating a new file” to start adding your first widget / snippet.

I’m using weatherwedgit.io to get the HTML code for a nice looking weather widget. Customize your widget as you like and then copy the HTML code and paste it in the new file you’ve just created in Github. and name the page “index.html”

and then click “Commit changes” at the end of the page
Step 3 : Publishing your widget

In your repository page click “settings”

Go all the way down till you find “Github Pages”. and choose “master branch”

After that, click “choose a theme” and select anyone. it won’t matter.

You’ll notice now that your HTML file is published at the given link

If you copied everything right then you should see the widget when you click the link.
Step 4: Adding it to Notion and creating more widgets

Copy that link and embed it as a URL into your Notion page and Voila !

Now, let’s add another widget. The widget on the left is a custom made one that changes the greeting according to the time of day and shows the date. I’ll show you how you can add it. or, of course, you can use any other HTML snippet you want.

let’s go back to our repository and click “Create new file”

I’ll call this file “greetings.html”. whatever you wanna call it remember the name because we’re gonna use it later.

Copy and paste the following code into your newly created file

<html> 
<head>
    <title>Greeting Message</title> 
    <style>
#lbl {
    font-family: monospace;
    font-size: xx-large;
    color: #626262;
    padding: 5px;
    border: 1px solid #ececec;
    text-align: center;
    line-height: 1.5;
    height:85%


}
#date{
    font-size:large;
}
body{
    background-color: aliceblue;
}
    </style>
</head>
<body>
    <div id="lbl"></div>
</body>

<script>
    var weekday = new Array(7);
    weekday[0] = "Sunday";
    weekday[1] = "Monday";
    weekday[2] = "Tuesday";
    weekday[3] = "Wednesday";
    weekday[4] = "Thursday";
    weekday[5] = "Friday";
    weekday[6] = "Saturday";

    
    var today = new Date();
    var hrs = today.getHours();
    var dayOfWeek = weekday[today.getDay()];
    var date = dayOfWeek+" " + today.getDate() + "/" +(today.getMonth()+1) +'/'+today.getFullYear()  ;

    var greet;

    if (hrs < 12)
        greet = 'Good Morning  ';
    else if (hrs >= 12 && hrs <= 17)
        greet = 'Good Afternoon ';
    else if (hrs >= 17 && hrs <= 24)
        greet = 'Good Evening  ';

    document.getElementById('lbl').innerHTML =
        greet+=`<div id="date"> It's ${date}</div>`;
</script> 
</html>

you can personalize it more by adding your name for example. you can do so editing that line of code

  greet+=`<div id="date"> It's ${date}</div>`;

to be like this

  greet+= "Your name here " +`<div id="date"> It's ${date}</div>`;

After you’re done, click “Commit new file”.

Your new widget link will be “your repository url”/”your file name”. your repository URL is the one you used the first time. you can get it from the Settings under GitHub pages. Mine looks like this https://ally293.github.io/notion/greetings.html

Like you did with the first widget embed that link and you’re done!

Add as many snippets as you want. “Github pages” is totally free without any distracting links!”
Tags:
notion app
What’s your reaction?
Love48
Sad4
Happy6
Sleepy2
Angry3
Dead5
Previous Article Anki tutorial for beginners chanhing the card background	Anki Tutorials for Beginners I: Changing the Card Background
Next Article 20 Notion Covers to make your pages stand out	20 Notion Covers to make your pages stand out
19 Comments
View Comments
Recent Posts

    Creating Notion pages shortcuts in Android
    30 More Notion Covers for Beautiful Pages and Templates
    Using Notion templates as a Recipe Manager app
    Organize Your Home Movies with Plex to Make your Memories Shine
    7 Notion widgets to power up your pages

Archives

    September 2020
    August 2020
    July 2020
    June 2020
    May 2020

Categories

    Anki
    Notion
    Organizing

Tags
Anki
Anki addon
Anki tutorial
notion app
notion template
Organizing
styling anki
Get Notified For New Posts
You Might Also Enjoy
Add a shortcut to Notion page on Android home screen
Notion
Creating Notion pages shortcuts in Android
Posted by shorouk Abdelaziz
shorouk Abdelaziz
September 26, 2020
READ MORE
notion pages covers
Notion
30 More Notion Covers for Beautiful Pages and Templates
Posted by shorouk Abdelaziz
shorouk Abdelaziz
August 21, 2020
READ MORE
a screenshot of a Notion recipe template
Notion
Using Notion templates as a Recipe Manager app
Posted by shorouk Abdelaziz
shorouk Abdelaziz
July 14, 2020
READ MORE
Load More
Shorouk's Blog

    Home
    About me
    Contact me
    Anki
    Notion
    Buy Me a Coffee
    Privacy Policy

© Copyright Shorouk Abdelaziz 2020
