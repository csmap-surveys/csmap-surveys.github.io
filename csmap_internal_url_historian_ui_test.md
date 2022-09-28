# Internal Testing Instructions
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
</style>
</head>
<body>
	<p>These purpose of these tests is to ensure that the URL Historian functionality is as expected as well as help the developers make any necessary modifications pertaining to user experience, data collection and deletion as well as pause, activation and blacklisting functionalities</p>
	<p>The data that will be collected during testing phase will be completely removed from our storage database both by your deletion activity as well as by CSMaP engineers. </p>
	<p>Please use the chrome browser for the entirety of this test. The extension does not collect browse history from other browsers</p>
	<div>
		<h2> Install </h2>
			<li> clone the extension <br> git clone -b authenticate git@github.com:SMAPPNYU/url_historian_chrome.git</li>
			<li> Load the extension to your chrome browser</li>
	</div>
	<div>
		<h2> Activate</h2>
		<ol>
			<li>use the survey id <strong>guest</strong> for both userID and surveyID</li>
			<li>use a userID that is less than 12 characters followed by surveyID <strong>guest</strong></li>
			<li>user userID that is more than 12 characters followed by surveyID<strong>guest</strong></li>
		<ol>
	</div>
	<div>
		<h2>Surf the web with the extension in thes modes</h2>
		<ol>
			<li>Active</li>
			<li>Paused </li>
			<li>Blackisted site</li>
		<ol>
	</div>
	<div>
		<h2> Delete either by</h2>
		<ol>
			<li>byTime </li>
			<li>byDate </li>
		<ol>
	</div>
	<div>
		<h2>Uninstall</h2>
		<p>Leave the extension to run for 4 hours. It will auto-install</p>
	</div>

</body>
</html>