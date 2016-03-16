
### What is this file?
##### _Guide to use the old facebook graph search and some Javascript code to generate Graph Search queries_
# Super very important note: _This_ **IS NOT** _a hack tool, graph search results respect content privacy you will_ **NEVER** _see anything you can't normally see_

#### Example query on my own profile to explain

#####https://www.facebook.com/search/100005052378257/stories-by

That query is formed from 4 parts

First the facebook url

Then /search/ to tell facebook that you are using the search
On mobile sites of facebook e.g mbasic.facebook.com/ & m.facebook.com/  you can use /graphsearch/ alternatively

Then my own facebook user id which is easily found on my profile link "https://www.facebook.com/profile.php?id=100005052378257" my facebook user id is the number after "id=" and if there is other GET variables till the "&"
To know the facebook user id of someone with a username there is so much ways the easiest is to use an online tool to know it for example http://findmyfbid.com/

the fourth part of the search query is /stories-by/ which is the graph search operator for posts I made
Other possible parameters are after the second example

Second example query
https://www.facebook.com/search/100005052378257/stories-liked/2016/mar/16/date-3/stories/intersect
*The first three parts are the same as the first example
*The fourth part is /stories-liked/ which is the graph search operator for posts I liked

The fifth part is /2016/mar/16/date-3/ which is today's date "16 march 2016" written in the format of "/Year/First Three letter of month/Day/date-3/" followed by /date-3/ to tell facebook that you want content from that specific day 
Alternatively you can use /date-2/ format which is "/Year/First Three letter of month/date-2/" to find content from that specific month in which case the search url would be https://www.facebook.com/search/100005052378257/stories-liked/2016/mar/date-2/stories/intersect
Also you can use /date/ format which is "/Year/date/" to find content from that specific year in which case the search url would be https://www.facebook.com/search/100005052378257/stories-liked/2016/date/stories/intersect

The sixth part is /stories/ which means you are searching posts

The seventh part is /intersect which is used with multiple different parameters

Another example you should easily understand on your own
https://www.facebook.com/search/100005052378257/photos-liked/2016/mar/date-2/photos/intersect

#### some useful links

http://researchclinic.net/graph.html

For other customised Graph searches see Graph.tips and http://www.intel-sw.com/blog/facebook-search/
The ultimate facebook sourcing tutorial
[part 1] (http://thebalazs.com/2013/08/11/the_facebook_sourcing_tutorial_part1/)
[part 2] (http://thebalazs.com/2014/12/30/the-facebook-sourcing-tutorial-part-2/)

Useful Graph operators
Action 	Operator
Liked 	/likers
Pages named 	/str/keywords separated by %20/pages-named/
Places 	/residents/past (or present)
/users-birth-place
/employer-location/ever-past (or present)
/place-visited
/places (e.g.bars)
/places-in
Friends 	/friends
People by name 	/str/keywords separated by %20/user-named
/males (or females)
Marriage 	/spouses/females (or males)
Groups 	/groups or /groups-privacy (for private groups)
Employment 	/job-liker-union
/employers
/employees/past (or present)
/employer-location/ever-past
Photos & Videos 	/photos-of
/photos-by
/photos-in (photos taken in a place)
/photos-tagged
/photos-commented
/photos-liked
/videos-of etc.
Posts 	/stories-commented
/stories-topic
/stories-by
/stories-tagged
/stories-liked
Religion/Politics 	/users-religious-view
/users-political-view
Sexuality 	/users-interested/males (or females or both)
Combined search 	/intersect (at the end of the address) 


use the following as templates to create queries
Important Notes:
1-It isn't important to read the whole document
2-Javascript could be used for autogeneration of date specific searches
3-javascript code must be put in a bookmark or run from browser console
4-replace "USERID" with the user id of your choice
Tip: use the replace all in your text editor

Keywords to use for finding associated code
Tip: use Ctrl + F for easily traversing them

JavaScript Queries:
Key1= Posts liked Year
Key2= Posts liked Month
Key3= Posts liked Day
Key4= Posts commented Month
Key5= Photos liked Year
Key6= Photos liked Month
Key7= Photos liked Day
Key8= Photos commented Month
Key9= Posts liked Yesterday
Note: Key9 is somewhat complicated but I use it though

Just URLs
Key10= Female Friends
Key11= Male Friends
Key12= Photos liked by two users at the same time
Key13= Posts liked by two users at the same time
Key14= Specific Page posts liked (use Page ID)
Key15= Specific Page photos liked(use Page ID)
Note: Previous four you can add date to refine search
Key16= See Two users friendship
Note: Key16 you can use facebook username instead of USERID


==================================================================

Key1
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
 return 'https://www.facebook.com/search/USERID/stories-liked/'+y+'/date/stories/intersect';

} window.open(url(), "_self");
``` 

==================================================================



Key2
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}

 return 'https://www.facebook.com/search/USERID/stories-liked/'+y+'/'+mon+'/date-2/stories/intersect';

} window.open(url(), "_self");
``` 


==================================================================



Key3
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}
   
 var d = date.getDate();
 if(d < 10){d = '0' + d;}

 return 'https://www.facebook.com/search/USERID/stories-liked/'+y+'/'+mon+'/'+d+'/date-3/stories/intersect';

} window.open(url(), "_self");
``` 

==================================================================

Key4
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}

 return 'https://www.facebook.com/search/USERID/stories-commented/'+y+'/'+mon+'/date-2/stories/intersect';

} window.open(url(), "_self");
``` 

==================================================================

Key5
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();

 return 'https://www.facebook.com/search/USERID/photos-liked/'+y+'/date/photos/intersect';

} window.open(url(), "_self");
``` 


==================================================================


Key6
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}
 return 'https://www.facebook.com/search/USERID/photos-liked/'+y+'/'+mon+'/date-2/photos/intersect';

} window.open(url(), "_self");
``` 




==================================================================



Key7
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}
   
 var d = date.getDate();
 if(d < 10){d = '0' + d;}

 return 'https://www.facebook.com/search/USERID/photos-liked/'+y+'/'+mon+'/'+d+'/date-3/photos/intersect';

} window.open(url(), "_self");
``` 

==================================================================

Key8
 ```js
 javascript:function url() {
 var date = new Date();
var y = date.getFullYear();
var m = date.getMonth();

var mon;
switch(m) {
    case 0:
        mon = "jan";
        break;
    case 1:
        mon = "feb";
        break;
    case 2:
        mon = "mar";
        break;
    case 3:
        mon = "apr";
        break;
    case 4:
        mon = "may";
        break;
    case 5:
        mon = "jun";
        break;
    case 6:
        mon = "jul";
        break;
    case 7:
        mon = "aug";
        break;
    case 8:
        mon = "sep";
        break;
    case 9:
        mon = "oct";
        break;
    case 10:
        mon = "nov";
        break;
    case 11:
        mon = "dec";
        break;
    default:
        mon = "jan";
}
 return 'https://www.facebook.com/search/USERID/photos-commented/'+y+'/'+mon+'/date-2/photos/intersect';

} window.open(url(), "_self");
``` 

==================================================================

Key9

 ```js
 javascript:function url() { var date = new Date();var y = date.getFullYear();var m = date.getMonth(); var mon; var yd; var d = date.getDate(); if (d==1) { switch(m) { case 0: yd = 31; mon = "dec"; break; case 1: yd = 31; mon = "jan"; break; case 2: if(y % 4 == 0) { yd = 29;} else { yd = 28;} mon = "feb"; break; case 3: yd = 31; mon = "mar"; break; case 4: yd = 30; mon = "apr"; break; case 5: yd = 30; mon = "jun"; break; case 7: yd = 31; mon = "jul"; break; case 8: yd = 31; mon = "aug"; break; case 9: yd = 30; mon = "sep"; break; case 10: yd = 31; mon = "oct"; break; case 11: yd = 30; mon = "nov"; break; default: yd = 31; mon = "dec";} } else { switch(m) { case 0: mon = "jan"; break; case 1: mon = "feb"; break; case 2: mon = "mar"; break; case 3: mon = "apr"; break; case 4: mon = "may"; break; case 5: mon = "jun"; break; case 6: mon = "jul"; break; case 7: mon = "aug"; break; case 8: mon = "sep"; break; case 9: mon = "oct"; break; case 10: mon = "nov"; break; case 11: mon = "dec"; break; default: mon = "jan"; }yd = d-1; }; return 'https://www.facebook.com/search/USERID/stories-liked/'+y+'/'+mon+'/'+yd+'/date-3/stories/intersect';} window.open(url(), "_self");
 ``` 

==================================================================
Key10
https://www.facebook.com/search/USERID/friends/females/intersect
==================================================================
Key11
https://www.facebook.com/search/USERID/friends/males/intersect
==================================================================
Key12
https://www.facebook.com/search/USERID/photos-liked/USERID/photos-liked/intersect
==================================================================
Key13
https://www.facebook.com/search/USERID/stories-liked/USERID/stories-liked/intersect
==================================================================
Key14
https://www.facebook.com/search/USERID/stories-liked/PAGEID/stories/intersect
==================================================================
Key15
https://www.facebook.com/search/USERID/photos-liked/PAGEID/photos/intersect
==================================================================
Key16
https://www.facebook.com/friendship/USERID/USERID/

