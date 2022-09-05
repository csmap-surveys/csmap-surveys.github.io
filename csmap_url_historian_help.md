# URL Historian
<html>
<head>
 <style> 
 	h1, h2, h3, h4, p, li { 
		line-height: 1.30;
		font-size:	20px;
		margin-top: 0.5em;
	}
	p,ol,li {
		margin-top: 0.5em;
		font-size: 14px ;
	}
</style>
</head>
<body>
<div>
<!-- <h1>CSMaP URL Historian</h1> -->
<p>
Thank you for downloading CSMaP URL Historian. URL Historian is a Chrome extension that collects browsing data from research participants who agree to share their browsing history and page content when browsing Twitter, Facebook and YouTube. All the data collected is securely stored in Amazon Web Services (AWS) and only accessible by CSMaP researchers. 

This page will help you information on how to use the extension effectively as well as address issues that you may encounter while using it</p>

<div>
	<h2>FREQUENTLY ASKED QUESTIONS</h2>
	<ul>
		<li><a href="#survey">What should I do if i forget my Survey ID?</a></li>
		<li><a href="#forget">What if I install and forget to activate the extension?</a></li>
		<li><a href="#pause">How do I pause and resume data collection?</a></li>
		<li><a href="#html">How do i share page content from Twitter, Facebook or YouTube?</a></li>
		<li><a href="#delete">How do i delete data already collected from me?</a></li>
			<ol><a href="#byTime">How to delete by date and time?</a></ol>
			<ol><a href="#byDate">How to delete by time</a></ol>
		<li>How can I prevent the extension from recording visits to websites that I wish to keep private?</li>
		<li><a href="#unblacklist">How can I remove a website from the blacklist?</a></li>
		<li><a href="#uninstall">What do I do if the extension uninstalls itself and not because of failed activation attempt?</a></li>
		<li><a href="#assistance">Who should I contact for further information?</a></li>
	</ul>

 </div>

<div id="survey">
	<h2 id="survey">What should I do if I forget my Survey ID?</h2>
	<p>Your Survey ID information is provided together with your user ID through either an email sent to you or through a link to install and activate the extension. If you receive an email please refer to it for both your user ID and surver ID. Otherwise please contact <a href="mailto:nyu-smapp-engineers@nyu.edu"> nyu-smapp-engineers@nyu.edu</a> for assistance. Please provide your study provider information as a reference</p>
	<p> You have 3 login attempts to activate the extension using your survey ID. With each failed attempt a prompt window will appear for you to input a valid study id.</p>
	<p>After 3 failed attempts the extension will auto uninstall from your browser.You should contact us at <a href="mailto:nyu-smapp-engineers@nyu.edu"> nyu-smapp-engineers@nyu.edu</a> for assistance.</p>
	<p align="center"><img src="images/alerts/final_failed_attempt.jpg"></p>
</div>
<div>
	<h2 id="forget">What if I install and forget to activate the extension?</h2>
	<p>The extension will send you a reminder 5 minutes after installing and every 30-minutes until you activate it.</p>
	<p align="center"><img src="images/alerts/inactive.jpg"></p>
</div>
	<!-- PAUSING AND REACTIVATING -->
<div>
	<h2 id="pause">How do I pause and resume data collection?</h2>
	<p>Using the button on the top right side of the extension window allows you to pause and resume data collection at any time. When the toggle is in “Active” state, the extension is collecting data </p>
	<ol>
		<li>Slide the toggle button to the left to pause data collection, and to the right to resume data collection.</li>
		<p align ="center">
			<iframe width="560" height="315" src="https://www.youtube.com/embed/Z9z7SfkZp0Q"></iframe>
		</p>
		<li>The extension will send you reminders after you have paused the extension for 60 minutes. After the first reminder, it will send follow-up reminders in 4-hour intervals.</li>
	</ol>
</div>
<!-- SHARING SOCIAL MEDIA CONTENT -->
<div>
	<h2 id="html">How to share Page Content from Twitter, Facebook or YouTube</h2>
	<ol>
		<li>Follow instructions below on how to allow sharing page content</li>
			<video width="320" height="240" controls>
	  		<source src="videos/uh_page_content.mp4" type="video/mp4"></video>
	 </ol>
</div> 
<div>
 	<h2 id="delete">How do i delete data already collected from me?</h2>
	<p> You can permanently delete data collected from you in the last 10 days within the extension either by specific date or specific date and time from our storage</p>
	<center><h2 id="byTime"> How to delete by date and time</h2></center>
	<p align ="center">
		<video width="600" height="400" controls>
	  		<source src="videos/uh_delbytime.mp4" type="video/mp4">
		</video>
	</p>
	<center><h2 id="byDate"> How to delete by date</h2></center>
	<p align ="center">
		<video width="320" height="240" controls>
	  		<source src="videos/uh_delbydate.mp4" type="video/mp4">
		</video>
	</p>
	<p> To delete data older than 10 days, send an email to  <a href="mailto:nyu-smapp-engineers@nyu.edu">nyu-smapp-engineers@nyu.edu.</a>. You must reference the user ID that you used to activate the extenson in your email and include the date(s) or date(s) and time(s) that you wish data to be deleted </p>
</div>
<!-- BlackList -->

<div>
	<h2 id="blacklist">How can I prevent the extension from recording visits to websites that I wish to keep private?</h2>
	<p>You can enter website domains that you wish to keep private using the <Strong>Blacklist</Strong> feature in the extension</p> 
	<p>Simply enter any URL in the format www.domain.com in <strong>Add Website to Blacklist</strong> field. Data from that domain will not be collected while you visiting it. </p>
	<p align ="center">
		<video width="320" height="240" controls>
  			<source src="videos/uh_blacklist.mp4" type="video/mp4">
		</video>
	</p>
	<p>You will see all domains you have blocked in the <strong>Websites Currenly Blacklisted</strong> field</p>
</div>
<!-- Unblacklist -->
<div> 
	<h2 id="unblacklist">How can I remove a website from the blacklist?</h2>
	<p>You can remove <strong>a blacklisted website from Websites currently blacklisted</strong> by </p> 
	<p>Simply click the <strong>X</strong> on the right of the website domain you wish to unblacklist</p>
	<p align="center">
		<video width="300" height="240" controls>
	  		<source src="videos/uh_unblacklist.mp4" type="video/mp4">
		</video>
	</p>
</div>
<div>
	<h2 id="uninstall">What do I do if the extension uninstalls itself and not because of failed activation attempt?</h2>
	<p>This is meant to happen based on the study. A notification will popup informing you that the extension will auto uninstall. If you believe this happened due to an error, please contact <a href="mailto:csmap-surveys@nyu.edu">csmap-surveys@nyu.edu</a></p>
	<p align="center"><img src="images/alerts/uninstall.jpg"></p>
</div>
<div>
	<h2 id="assistance"> Who should I contact for further information?</h2>
	<ol>
		<li>For any questions on using the extension, requesting data deletion or other technical problems, please reach out to <a href="mailto:nyu-smapp-engineers@nyu.edu"> nyu-smapp-engineers@nyu.edu</a></li>
		<li>For any questions regarding the use of the extension, the data we collect, or the research projects that your data will be used in, please contact <a href="mailto:csmap@nyu.edu">csmap-surveys@nyu.edu</a> for assistance</li>
	</ol>
</div>
</body>
</html>