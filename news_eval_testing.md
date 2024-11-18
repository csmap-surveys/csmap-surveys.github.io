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
				font-size: 15px ;
			}
		</style>
	</head>
	<body>
		<p>These purpose of this test is to ensure that:</p>
		<ul>
		 	<li> Survey instructions are clear and concise.</li>
		 	<li> The <strong> News Evaluation </strong> plugin functionality is as expected.</li>
		</ul>
		<p>The test will help researchers and engineers refine study instructions and improve the quality of data captured using the plugin.</p>
		<p>All the data collected by the survey engine and the plugin will be deleted post analysis from our storage database. </p>
		<p>Please use the <strong>Google Chrome</strong> browser for the entirety of this test. The plugin does not collect web activity from other browsers</p>
		<div>
			<h2> Test overview </h2>
			<p>You will perform a task that incorporates survey questions that includes instructions on how to install the plugin and perform tasks that will be captured by the plugin.</p>
			<p> For this task you were emailed with a unique user ID which you will use for the survey and for registering the plugin.</p>
			<p> Follow the instructions below to perform the test:</p>
			<ol>
				<li><button id="copyButton" style="background-color: #59B2D1; color: black;">Copy Survey link</button></li>
				<li> Paste the Copied survey link URL into a Chrome Browser</li>
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
