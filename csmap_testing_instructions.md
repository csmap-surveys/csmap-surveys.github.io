# Testing Instructions
<html>
<head>
 <style> 
 	h1, h2, h3, h4, p, li { 
		line-height: 1.25;
		font-size:	20px;
		margin-top: 0.5em;
	}
	p,ol,li {
		margin-top: 0.5em;
		font-size: 14px ;
	}
	.blink-two {
        animation: blinker-two 1.5s linear infinite;
      }
    @keyframes blinker-two {
        100% {
          opacity: 0;
        }
      }
</style>
</head>
<body>
<p>These purpose of these tests is to ensure that the URL Historian functionality is as expected as well as help the developers make any necessary modifications pertaining to user experience, data collection and deletion as well as pause, activation and blacklisting functionalities</p>
<p>The data that will be collected during testing phase will be completely removed from our storage database both by your deletion activity as well as by CSMaP engineers. </p>
<p>Please use the chrome browser for the entirety of this test. The extension does not collect browse history from other browsers</p>
<p>The CSMaP team appreciates your support in testing the extension.</p>

<div>
	<h2> Overview of the tasks you will perform </h2>
		<ol>
			<li> Installing from Chrome Web Store and Activating the extension</li>
			<li> Sharing YouTube Page Content</li>
			<li> Navigate to specific set of URLs</li>
			<li> Navigate YouTube</li>
			<li> Pausing and Reactivating Data Collection</li>
            <li> Unpause the extension</li>
			<li> Deleting collected data</li>
			<li> Add Website to Blacklist</li>
		</ol>
</div>
<div>
	<h2>Installing from Chrome Web Store and Activating the Extension</h2>
	<ol>
		<li>Follow instructions below on how to install and activate the extension</li>
			<video width="320" height="240" controls>
	  		<source src="videos/uh_activate.mp4" type="video/mp4"></video>
		<li><a href="https://chrome.google.com/webstore/detail/url-historian/imdfbahhoamgbblienjdoeafphlngdim/related?hl=en" target="_blank" rel="noopener noreferrer">install</a> URL Historian extension </li>
	  	<li> Activate the extension using the user ID provided with your email</li>
	 </ol>
</div> 
<div>
	<h2>Sharing YouTube Page Content</h2>
	<ol>
		<li>Follow instructions below on how to allow sharing YouTube page content</li>
			<video width="320" height="240" controls>
	  		<source src="videos/uh_page_content.mp4" type="video/mp4"></video>
	 </ol>
</div> 
<div>
	<h2> Navigating to specific set of websites</h2>
	<p> Click the links below in order to visit the associated websites</p>
	<ol>
		<li><a href="https://www.google.com" target="_blank" rel="noopener noreferrer">www.google.com</a></li>
		<li><a href="https://www.nytimes.com/2020/08/21/movies/tenet-review-christopher-nolan.html" target="_blank" rel="noopener noreferrer">www.nytimes.com/2020/08/21/movies/tenet-review-christopher-nolan.html</a></li>
		<li><a href="https://www.cnn.com/style/article/birkenstocks-history-comfortable-shoes-sandals/index.html" target="_blank" rel="noopener noreferrer">www.cnn.com/style/article/birkenstocks-history-comfortable-shoes-sandals/index.html</a></li>
		<li><a href="https://www.nyu.edu" target="_blank" rel="noopener noreferrer">www.nyu.edu</a></li>
	</ol>
</div>
<div>
	<h2> Navigate YouTube</h2>
	<p> Click the link below to visit YouTube</p>
	<ol>
		<li>Click <a href="https://www.youtube.com" target="_blank" rel="noopener noreferrer">www.youtube.com</a></li>
		<li>Click on any YouTube video of your choice on your home page</li>
		<li>Click on 2 more YouTube video of your interest sequentially without watching the content</li>
		<li>Click <a href="https://www.youtube.com" target="_blank" rel="noopener noreferrer">www.youtube.com</a></li>
		<li>After 10 minutes, close both tabs running YouTube</li>
	</ol>
</div>

<div>
	<h2>Pausing and Reactivating Data Collection</h2>
	<ol>
		<li>Pause and reactivate the activity of the plugin by toggling the purple switch as shown below</li>
		<video width="320" height="240" controls>
	  		<source src="videos/uh_pause.mp4" type="video/mp4">
	  	</video>
	  	<li>Pause the extension</li>
	</ol>
	<p style="font-size: 0.6rem; color: #686868" >After the plugin has been paused for 60 minutes, it will sends a reminder for you to reactivate it. Then every 4 hours until its reactivated</p>
	<p style="font-size: 0.6rem; color: #686868">While the extension is paused, it will not be sending your browsing data to our database.</p>
</div>

<div>
	<h1 class="blink-two" ><center><strong style="font-size: 30px; color: #FF0000">STOP!</strong></center></h1> 
	<p>Please wait <strong>12-24</strong> hours before proceeding to the next steps.</p> 
</div>

<div>
	<h2>Unpause the extension</h2>
	<p>Re-activate the extension as demonstrated in <strong style="color: #159957"> Pausing and Reactivating Data Collection</strong> above</p>
	<p>Visit a few more websites in the order below:</p>
	<ol>
		<li>Click <a href="https://www.washingtonpost.com/entertainment/music/qanda-with-yo-yo-ma-how-music-can-be-like-touch-during-these-socially-distant-times/2020/08/13/9725a22c-db07-11ea-8051-d5f887d73381_story.html" target="_blank" rel="noopener noreferrer">www.washingtonpost.com</a></li>
		<li>Click <a href="https://csmapnyu.org/" target="_blank" rel="noopener noreferrer">csmapnyu.org</a></li>
		<li>Click <a href="https://www.youtube.com/watch?v=-N5fEeD4Mnk" target="_blank" rel="noopener noreferrer">www.youtube.com</a></li>
	</ol>
</div>
<div>
	<h2>Deleting collected data</h2>
	<p> You can delete your individual data by clicking either the <strong><em>by Date</em></strong> or the <strong>by Time</strong> button in the <strong><em>Delete Browse History</em></strong> section.</p>
	<p><strong>by Time</strong>--deletes data collected for the selected hour range or single hour.</p>
	<p><strong>by Date</strong>--deletes all the data collected for the selected day. This is restricted to the past 7 days.</p>
	<ol>
		<!-- <li>Follow the instructions below on how to delete collected data <strong>by Time</strong></li>
		<video width="320" height="240" controls><source src="videos/uh_delbytime.mp4" type="video/mp4"></video> -->
		<li>Follow the instructions below on how to delete collected data <strong>by Date</strong></li>
		<video width="320" height="240" controls><source src="videos/uh_delbydate.mp4" type="video/mp4"></video>
		<li>Please use <strong>by Date</strong> and delete data collected yesterday from all social media and non-social media sources.</li>
	</ol>
</div>

<div>
	<h2>Add Website to Blacklist</h2>
	<p> <strong><em>Blacklisting</em></strong> creates a list of web domains which prevents those websites in the blacklist from been sent to our database.</p>
	<ol>
		<li>Follow the instructions below on how to <strong>Add Website to Blacklist</strong></li>
		<video width="320" height="240" controls><source src="videos/uh_blacklist.mp4" type="video/mp4"></video>
	  	<li>Please add <strong>www.cnn.com</strong> to the blacklist</li>
		<li>Visit <a href="https://www.cnn.com/travel/destinations/colorado" target="_blank" rel="noopener noreferrer">www.cnn.com/travel</a></li>
		<li>Remove <strong>www.cnn.com</strong> from the blacklist by clicking on the <strong style="color: #FF0000 ">x</strong> next to www.cnn.com</li>
		<li>Visit <a href="https://www.cnn.com/travel/destinations/colorado" target="_blank" rel="noopener noreferrer">www.cnn.com/travel</a></li>
	</ol>
</div>
<p>After this, you can remove the extension from the browser by right-clicking the icon and clicking “Remove from Chrome”.</p>
<p>We appreciate your help with the testing! Please email <a href="nyu-smapp-engineers@nyu.edu">nyu-smapp-engineers@nyu.edu</a> if you run into any problems with the plug in.</p>
</body>
</html>