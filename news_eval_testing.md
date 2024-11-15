---
title: News Evaluation Testing
layout: perplexity
---
<html>
	<head>
	 	<style> 
		 	h1, h2, h3, h4, p, li { 
				line-height: 1.25;
				font-size:	20px;
				margin-top: 0.5em;
			}
			p,ol,li,video {
				margin-top: 0.5em;
				font-size: 14px ;
			}
		</style>
	</head>
	<body>
		<p>These purpose of these test is to ensure that survey instructions that will be provided to survey participants are clear and the functionality of the  <strong>News Evaluation</strong> plugin is as expected. 
		<p>The test you will perform will help the researcher and the plugin developers to make any necessary modifications pertaining to clear instructions to study participants and ensure the capture of high quality data for research </p>
		<p>The data that will be collected both in the survey and plugin portion will be completely removed from our storage database by CSMaP engineers. </p>
		<p>Please use the <strong>Google Chrome</strong> browser for the entirety of this test. The extension does not collect web activity from other browsers</p>
		<div>
			<h2> Test overview </h2>
			<p>You will perform a task that incorporates survey questions that included instruction on how to install a plugin and perform web activity that will be captured.
			<p> For this task you were emailed with a uniqued userID which you will use for the survey and for registering the plugin 
			<p> Follow the instructions below to perform the test</p>
			<ol>
				<li><button id="copyButton" style="background-color: #59B2D1; color: black;">Copy Survey link</button></li>
				<li> Paste the Copied Survey Link URL into a Chrome Browser</li>
				<li> Take the survey</li>
			 </ol>
		</div>
    	<script>
        	const urlDisplay = document.getElementById('urlDisplay');
        	const copyButton = document.getElementById('copyButton');
        	const url = 'https://nyu.qualtrics.com/jfe/form/SV_diCWiMmVyDtvhSC';

        	copyButton.addEventListener('click', () => {
            	navigator.clipboard.writeText(url).then(() => {
                copyButton.textContent = 'Copied!';
                	setTimeout(() => {
                    copyButton.textContent = 'Copy Survey link';
                	}, 2000);
            	}).catch(err => {
                	console.error('Failed to copy: ', err);
            	});
        	});
    	</script>
    	<p>We appreciate your support in testing the extension.</p>
	</body>
</html>
