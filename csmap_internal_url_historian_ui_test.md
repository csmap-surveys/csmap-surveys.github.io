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
	<p>Please use the chrome browser for the entirety of this test. The extension does not collect browse history from other browsers<br>
		This tests are not exhaustive and you are welcome to add several others that may be encountered in the field
	</p>
	<div>
		<h3> Install </h3>
		 <ol>
			<li> clone the extension:<br>
				<strong>git clone -b authenticate git@github.com:SMAPPNYU/url_historian_chrome.git</strong>
			</li>
			<li> Load the extension to your chrome browser</li>
		</ol>
	</div>
	<div>
		<h3>Uninstall</h3>
		<p>Leave the extension to run for two days. It should uninstall with a message</p>
	</div>
	<div>
		<h3> User ID test</h3>
		<ol>
			<li>Input userID as an email</li>
			<li>Input userID as a wrong email format <strong>name@yahoocom</strong> </li>
			<li>Incorporate one or more email characters <strong>(@, com, .)</strong> in your userID </li>
		</ol>
		<p> The userID is automatically truncated if its more than 30 characters and will be valid. The prompt to put surveyID</p>
	</div>
	<div>
		<h3> Survey ID TEST </h3>
		<ol>
			<li>With valid userID use <strong>guest</strong> as surveyID</li>
			<li>make wrong entry for surveyID <strong>guest</strong> eg (guets, guset, ...) three times</li>
			<li>make wrong entry for surveyID <strong>guest</strong> eg guets, guset, ... once or twice then correctly </li>
		</ol>
	</div>
	<div>
		<h3>Correctly activate the app and surf the web with the extension in these modes</h3>
		<ol>
			<li>Active</li>
			<li>Paused </li>
			<li>With Blackisted sites</li>
		</ol>
	</div>
	<div>
		<h1 class="blink-two" ><center><strong style="font-size: 30px; color: #FF0000">STOP!</strong></center></h1> 
		<p>Please wait <strong>12-24</strong> hours before proceeding to the next steps.</p> 
	</div>
	<div>
		<h3> Deleting</h3>
		<ol>
			<li>delete previous day data byDate </li>
			<li>delete the current day byTime </li>
		</ol>
	</div>
</body>
</html>