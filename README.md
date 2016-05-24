# Mobile Ecommerce Social Media #

## Main Goals : ##
Identify the BUZZ/prominent device currently in market.
  * Providing market sentiment about device on its detail page would help customer in making better choices
  * Provide Social Live feed about device on its detail page. Which gives current market reviews about devices/plans
  * Live Heat Maps of devices based on OS(iphone vs android), New Phones(iphone6 vs S5)

Link Social Networks with existing customer profile.
  * Extract social profile of customer and tag it with existing ATT profile.
  * Helpful in auto-populating form fields while creating new customer account.
  * Can provide targeted ads based on Social conversations.

Create a social circle of customers including friends from his social networks
  * Suggest New device/Plan based on his friends current device/plan
  * Moving friends comment/review about devices/plans on top
  * Provides opportunity to know about device from friends

Creating Live feed of twitter/facebook using apis instead of using their Website.
  * We may end-up promoting competitors on att website. Since twitter allows sponsored tweets in between.


### Extra: ###
  * Search Engine
  * Ranking Search Results
  * Clustering Search Engine Results
  * Organize Data

### Social Login: ###
Ability to make User login using their Social Networks.
<br>
<b>Demo :</b> <a href='http://socioapi.appspot.com/'>http://socioapi.appspot.com/</a>


<h3>Link Social Profile :</h3>
In case of ATG we can extend user profile to include facebook/twitter handle<br>
<br>
<br>
<h3>optin/optout :</h3>
provide user an opportunity to optout at any instance<br>
<br>
<h3>Identify Person on Social Networks :</h3>
This would be helpful in knowing customer problem more effectively using his tweet/post.<br>
<br>
<h3>Prominent device currently in market :</h3>
We can use combination of Radian6 and clarabridge to show prominent devices in top of the chart.<br>
<br>
<h3>Social Circle :</h3>
We can create a circle of friends for current user using his fb/twitter friends, who have account with us and this could be helpful in decision making.<br>
<br>
<h3>Realtime Feedback about Product :</h3>
We can include Social timeline a side of device to be purchased. This timeline would show all the posts/tweets with current device hashtag.<br>
<br>
<a href='https://code.google.com/p/mobile-social/logo'>https://code.google.com/p/mobile-social/logo</a>



<h3>Search Engine :</h3>
Search with query should result matched data.<br>
<br>
<b>Demo :</b> <a href='http://socioapi.appspot.com/search'>http://socioapi.appspot.com/search</a>
<br><br>
<a href='https://code.google.com/p/social-networks-gateway-googleapp-engine/source/browse/src/com/prashanth/searchengine/preprocess/PreProcesser.py'>PreProcess Steps</a>
<br>
<br>
Further planning to add ability of query expansion using WordNet<br>
<br>example : loan<br>
<br>noun.  	advance - accommodation - borrowing - debt - loaning<br>
<br>verb.  	lend - borrow<br>
<br>
<br>
<h3>Ranking Search Results :</h3>
<ul><li>Using Cosine Similarity to get the distance between query and data<br>
</li><li>Planning to Conect current scenario with Page Rank Algorithm (used in google). I had implemented a version of Page Rank in Scala, need to work on python implementation  <a href='https://code.google.com/p/page-rank-scala/source/browse/src/com/prashanth/graph/PageRank.scala'>link</a></li></ul>

<h3>Clustering Search Engine Results :</h3>
<b>Problem :</b> Manager wants some data about how many people are facing problem with insurance.. with Relational db running a query on un-organized data  wont be good idea.<br>
<br>
<b>Solution :</b> I wrote a Search Engine Few years back with an ability to cluster the Search results and query extension. Please find a flow of pictures in below link, they would make it clear about this.<br>
<br>
<a href='https://code.google.com/p/search-engine-perl/'>Project Details</a>  <a href='https://search-engine-perl.googlecode.com/files/Search_Engine.pdf'>PPT</a>  <a href='https://search-engine-perl.googlecode.com/files/Clustering_Search_Results.pdf'>PDF</a>
<br>

Above approach is based on single linkage clustering, instead planning to make use  combination of single and complete linkage clustering.<br>
<i>use previous work on<br>
<ul><li>gene sequence clustering</i> <a href='https://page-rank-scala.googlecode.com/files/Clustering_of_sequences_using_Esprit_and_CD-HIT.pdf'>link</a> (BOW MODEL)<br>
</li><li><i>Clustering Documents Using Wikipedia Minor</i> <a href='https://page-rank-scala.googlecode.com/files/clustering_documents_using_wikipedia.pdf'>link</a> (Semantic Analysis Using Wikipedia Miner)  <i>cat and bag -> 20% , cat and dog -> 75%</i></li></ul>



<h3>Organize Data :</h3>


<blockquote>This can be done n number of ways.. my intention is to split the content into two types for now.Do the post made on facebook/twitter/.. depicts positive or negative about the company. This is a kind of process automation, where we extract all the negative feedback and process it to further level.</blockquote>

<b>Problem :</b> User needs to read all the posts and organize manually as positive or negative posts and process it to other people who take the required steps.<br>
<br>
<b>Solution :</b><br> 1) I did some work few years back on polarity Detection. I made it public in <a href='http://prashanthmadi.blogspot.com/2010/11/nlp-project.html'>Blog</a>
<br>
2) Using NLTK Package to get sentiment of input data<br>
<a href='http://text-processing.com/demo/sentiment/'>link</a>
