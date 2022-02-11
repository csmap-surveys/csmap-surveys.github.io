# CSMaP URL Historian
Thank you for downloading the CSMaP URL Historian. Your data will support research on political knowledge, online behavior, and public opinion. The CSMaP URL Historian is a Chrome plug-in that allows you to share your data with the CSMaP research team. If at any time you wish to stop sharing your data, you can contact us at [nyu-smapp-engineers@nyu.edu](mailto:nyu-smapp-engineers@nyu.edu).

Participation in web browsing collection is voluntary. You can delete data for up to one week via the extension. To delete data farther back than one week, please contact [nyu-smapp-engineers@nyu.edu](mailto:nyu-smapp-engineers@nyu.edu).

For any questions regarding the use of the extension, the data we collect, or the research that your data will be used in, please contact [csmap-surveys@nyu.edu](mailto:csmap-surveys@nyu.edu). 

URL Historian is a Chrome extension that enables the collection of web browsing activities or website content in real-time. It collects browsing data for research purposes from research participants who opt-in to share their browsing history and page content when browsing Twitter, Facebook and Youtube. Page content information is collected if the research participant opt-in and the data collected is only for the social media site(s) opted for. 

The extension provides visualization feature that beautifully displays the participant's locally stored browsing history. The visual displays reflects browsing habits such as frequency of visits and word searches on search engines, visits times in a heatmap graph, and visit details in a tabulated format. Importantly, the visualization information presented remains in the user's local machine and is composed of the entirety browsing history. Therefore, websites visit before and during extension installation is used to generate the visualizations. Of the entire browsing history displayed, the extension only collects information the participant has opted to be collected.

Collected data is securely stored in Amazon Web Services(AWS) and only accessible to the CSMaP research team. The extension is available in the Chrome Web Store and accessible via invitation only.


## FAQ
1. [What if I install and forget to activate the extension?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#what-if-i-install-and-forget-to-activate-the-extension) 
2. [How do I pause and reactivate the extension?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#how-do-i-pause-and-reactivate-the-extension)
3. [Can I delete data collected from me?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#can-i-delete-data-collected-from-me)
4. [How can I prevent the extension from recording visits to websites that I wish to keep private?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#how-can-i-prevent-the-extension-from-recording-visits-to-websites-that-i-wish-to-keep-private)
5. [What should I do if I forget my login ID?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#what-should-i-do-if-i-forget-my-login-id)
6. [What do I do if the extension uninstalls itself and not because of failed attempts?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#what-do-i-do-if-the-extension-uninstalls-itself-and-not-because-of-failed-attempts)
7. [Who should I contact for further information?](https://github.com/csmap-surveys/csmap-surveys.github.io/blob/main/csmap_url_historian.md#who-should-i-contact-for-further-information)

<div>
	<h2>What if I install and forget to activate the extension?</h2>
	<p>The extension will send you a reminder 5 minutes after installing and every 30-minutes until you activate it.</p>
	<p align="center"><img src="images/alerts/inactive.jpg"></p>
</div>
<div>
	<h2>How do I pause and reactivate the extension?</h2>
	<ol>
		<li>Slide the toggle button to the left to pause, and to the right to reactivate the extension.</li>
		<p align ="center">
			<video width="320" height="240" controls>
  				<source src="videos/uh_pause.mp4" type="video/mp4">
			</video>
		</p>
		<li>The extension will send you reminders after you have paused the extension for 60 minutes. After the first reminder, it will send follow-ups in 4-hour intervals.</li>
	</ol>
</div>
<div>
 	<h2>Can I delete data collected from me?</h2>
	<p>Yes, we currently allow users to delete data within the past 7 days. (You can contact our research team at <a href="mailto:nyu-smapp-engineers@nyu.edu">nyu-smapp-engineers@nyu.edu</a> to request data deletion beyond the 7-day time frame.)</p>
	<p>You can also delete data collected within the specified date and time frame or date will be permanently deleted from our storage.</p>
	<center><h3> Delete by date and time</h3></center>
	<p align ="center">
		<video width="640" height="480" controls>
	  		<source src="videos/uh_delbytime.mp4" type="video/mp4">
		</video>
	</p>
</div>

To delete by date:
1. Click on _by Date_.
2. Select the _TimeZone_ you were are in ). You can also search for a time zone using keywords (e.g. Eastern, -04).
3. Select a _Date_.
4. Click on _Delete_. All your data collected on the selected date will be permanently deleted from our storage.

<div>
	<h2>How can I prevent the extension from recording visits to websites that I wish to keep private?</h2>
	<p>You can set up a list of web domains that you wish to keep private in <strong>Add Website to Blacklist</strong>
	<p align ="center">
		<video width="320" height="240" controls>
  			<source src="videos/uh_blacklist.mp4" type="video/mp4">
		</video>
	</p>
	<p>The URL will be added to the list of <strong>Websites currently Blacklisted</strong>. When you visit any of these sites, we will not record the URLs.</p> 
	<p>You can remove a blacklisted website from <strong>Websites currently Blacklisted</strong> by </p> 
	<p align="center">s
		<video width="300" height="240" controls>
	  		<source src="videos/uh_unblacklist.mp4" type="video/mp4">
		</video>
	</p>

</div>
<div>
	<h2>What should I do if I forget my login ID?</h2>
	<p>You can always find your User ID in your survey. You have 5 login attempts to activate the extension.</p>
	<p> With each failed attempt a notification message will popup.</p>
	<p align="center"><img src="images/alerts/failed_attempt.jpg"></p>
	<p>After 5 failed login attempts, the extension will auto uninstall, you should contact us at <a href="mailto:nyu-smapp-engineers@nyu.edu"> nyu-smapp-engineers@nyu.edu</a> for assistance.</p>
	<p align="center"><img src="images/alerts/final_failed_attempt.jpg"></p>
</div>
<div>
	<h2>What do I do if the extension uninstalls itself and not because of failed attempts?</h2>
	<p>This is meant to happen based on the study. A notification will popup informing you that the extension will auto uninstall. If you believe this happened due to an error, please contact  <a href="mailto:csmap-surveys@nyu.edu">csmap-surveys@nyu.edu</a></p>
	<p align="center"><img src="images/alerts/uninstall.jpg"></p>
</div>
<div>
	<h2> Who should I contact for further information?</h2>
	<ol>
		<li>For any questions on using the extension, requesting data deletion or other technical problems, please reach out to nyu-smapp-engineers@nyu.edu</li>
		<li>For any questions regarding the use of the extension, the data we collect, or the research projects that your data will be used in, please contact <a href="mailto:csmap-surveys@nyu.edu">csmap-surveys@nyu.edu</a> for assistance</li>
	</ol>
</div>