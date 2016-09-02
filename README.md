# TwitterStream-Program

1. Establish connection with Twitter's streaming API after obtaining consumer and secret keys, app registration, etc.

2. As you probably know, at present, Twitter lets you have a bounding box or a search but not both simultaneously. So choose      the search method and establish not one bounding box, but numerous bounding boxes that encompass the specific public health    jurisdiciton or area of interest.  It really helps to think of this as a calculus area problem (you know, where lim -> inf     in terms of rectangles...). 
   
3. Use these bounding boxes in a series of OR statements in the Java program, rather than in Twitter in order to determine
   whether the Lat/Lng of the tweet was in the target jurisdiction. 
   
4. If yes, then mark the tweet as important in your log file (then examine the log file, see if it's important, and if so,        tweet at the user who posted about 'food poisoning.'
   
5. If the Lat/Lng are turned off, then you can still look at the user's profile location as a proxy. Code these as 'possible' hits and
   look at these very carefully. In our case, we have ~125 cities in our area that are either completely within or jurisdiction, 
   or touch or cross our county's border. We opted to use an array to determine whether the name of our ~125 municipalities is contained 
   in the profile location string, and process accordingly.
   
6. We are epidemiologists, not coders. We have expertise in SAS/R. However, we were able to borrow code, adapt it, add to it, 
   and solve the problem. From beginning to end, this took three days -- knowing nothing about how to do this. Power of open source. 
  
7. In summary -- get your keys and load them in the java program. Put in your bounding box coordinates. Put in your file path. Put in 
   your search terms and you should be good to go. Tweet at us if you think we can help you and we will do what we can: @FoodSafeCookCo
   
