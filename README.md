<p style="text-align:justify;margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">You are asked to write a small API to support the user interface of a train ticket machine.</span></span></span></span></p>

<p style="text-align:justify;margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">You will not be creating any actual User Interface but instead, you should model the problem space and implement a search feature to help the user find train stations by name in order to buy a ticket.</span></span></span></span></p>

<p style="text-align:justify;margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">These machines have a <u>direct but unreliable connection</u> to the central system and use a touchscreen display which works as follows.</span></span></span></span></p>

<p style="text-align:justify;margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">As the user types each character of the station&rsquo;s name on the touchscreen, the display should:</span></span></span></span></p>

<ol>
	<li style="text-align:justify;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Update to show all valid choices for the next character </span></span></span></span></li>
	<li style="text-align:justify;margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">List of possible matching stations.</span></span></span></span></li>
</ol>

<p style="margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">The illustration below shows what is needed when &lsquo;D A R T&rsquo; has been entered.</span></span></span></span></p>

<p style="margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><img alt="" height="215" src="https://hrcdn.net/s3_pub/istreet-assets/8iQfdpc6oGNHQseIxSQCWQ/Screenshot%202020-05-05%20at%2017.05.28.png" width="497" /></span></span></span></span></p>

<p style="margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">This URI simulates the central system response:&nbsp;</span></span></span></span><a href="https://raw.githubusercontent.com/abax-as/coding-challenge/master/station_codes.json">https://raw.githubusercontent.com/abax-as/coding-challenge/master/station_codes.json</a></p>

<h2 style="margin-top:13px;"><span style="font-size:13pt;"><span style="line-height:115%;"><span style="font-family:Cambria,serif;"><span style="color:#4f81bd;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Requirements:</span></span></span></span></span></h2>

<ol>
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Typing a search string will return: </span></span></span></span>

	<ol style="list-style-type:lower-alpha;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">All stations that start with the search string.</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">All valid next characters for each matched station.</span></span></span></span></span></li>
	</ol>
	</li>
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Space is a valid character when returning a list of next characters.</span></span></span></span></span></li>
	<li style="margin-bottom:13px;"><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">The service response will be used for the machine UI and for the routing and pricing purposes.</span></span></span></span></span></li>
</ol>

<h2 style="margin-top:13px;"><span style="font-size:13pt;"><span style="line-height:115%;"><span style="font-family:Cambria,serif;"><span style="color:#4f81bd;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Operational requirements:</span></span></span></span></span></h2>

<ol>
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Runtime speed is very important, loading time is not.</span></span></span></span></span></li>
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Make no assumptions about the data source in real life.</span></span></span></span></span></li>
</ol>

<h2 style="margin-top:13px;"><span style="font-size:13pt;"><span style="line-height:115%;"><span style="font-family:Cambria,serif;"><span style="color:#4f81bd;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Expected Scenarios:</span></span></span></span></span></h2>

<p>&nbsp;</p>

<ul>
	<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Given </span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">a list of stations &lsquo;DARTFORD&rsquo;, &lsquo;DARTON&rsquo;, &lsquo;TOWER HILL&rsquo;, &lsquo;DERBY&rsquo;</span></span></span></span></span></span></span>

	<ul style="list-style-type:circle;">
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">When</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> input &lsquo;DART&rsquo;</span></span></span></span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Then</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> should return:</span></span></span></span></span></span></span>
		<ol>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">The characters of &lsquo;F&rsquo;, &lsquo;O&rsquo;</span></span></span></span></span></span></span></li>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">The stations &lsquo;DARTFORD&rsquo;, &lsquo;DARTON&rsquo;.</span></span></span></span></span></span></span></li>
		</ol>
		</li>
	</ul>
	</li>
</ul>

<p style="margin-left:144px;">&nbsp;</p>

<ul>
	<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Given </span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">a list of stations&nbsp; &lsquo;LIVERPOOL&rsquo;, &lsquo;LIVERPOOL LIME STREET&rsquo;, &lsquo;PADDINGTON&rsquo;</span></span></span></span></span></span></span>

	<ul style="list-style-type:circle;">
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">When</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> input &lsquo;LIVERPOOL&rsquo; </span></span></span></span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Then</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> should return:</span></span></span></span></span></span></span>
		<ol>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">The characters of &lsquo; &lsquo;</span></span></span></span></span></span></span></li>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">The stations &lsquo;LIVERPOOL&rsquo;, &lsquo;LIVERPOOL LIME STREET&rsquo;</span></span></span></span></span></span></span></li>
		</ol>
		</li>
	</ul>
	</li>
</ul>

<p style="margin-left:144px;">&nbsp;</p>

<ul>
	<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Given</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> a list of stations &lsquo;EUSTON&rsquo;, &lsquo;LONDON BRIDGE&rsquo;, &lsquo;VICTORIA&rsquo; </span></span></span></span></span></span></span>

	<ul style="list-style-type:circle;">
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">When</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> input &lsquo;KINGS CROSS&rsquo;</span></span></span></span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">Then</span></span></span></b><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;"> should return: </span></span></span></span></span></span></span>
		<ol>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">no next characters </span></span></span></span></span></span></span></li>
			<li><span style="font-size:11pt;"><span style="line-height:normal;"><span><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-size:10.0pt;"><span style="font-family:&quot;Cascadia Code&quot;;"><span style="color:black;">no stations</span></span></span></span></span></span></span></li>
		</ol>
		</li>
	</ul>
	</li>
</ul>

<h1 style="margin-top:32px;"><span style="font-size:14pt;"><span style="line-height:115%;"><span style="font-family:Cambria,serif;"><span style="color:#365f91;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Evaluation Guidelines:</span></span></span></span></span></h1>

<p>&nbsp;</p>

<ol>
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Understanding and interpretation of the domain</span></b></span></span></span>

	<ul style="list-style-type:disc;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Context</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Boundaries</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Ubiquitous Language</span></span></span></span></li>
	</ul>
	</li>
</ol>

<p style="margin-left:96px;">&nbsp;</p>

<ol start="2">
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Delivery quality</span></b></span></span></span>

	<ul style="list-style-type:disc;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Complete solution meeting all requirements</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">No typographical errors</span></span></span></span></li>
	</ul>
	</li>
</ol>

<p style="margin-left:96px;">&nbsp;</p>

<ol start="3">
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Code readability</span></b></span></span></span>

	<ul style="list-style-type:disc;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Classes, functions, methods and fields naming</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Consistent code formatting</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Adequate documentation</span></span></span></span></li>
	</ul>
	</li>
</ol>

<p style="margin-left:96px;">&nbsp;</p>

<ol start="4">
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Code quality</span></b></span></span></span>

	<ul style="list-style-type:disc;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Coding against tests</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Code coverage &amp; complexity</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Correct usage of data structures and techniques</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Solution dependencies and their correct usage</span></span></span></span></li>
	</ul>
	</li>
</ol>

<p style="margin-left:96px;">&nbsp;</p>

<ol start="5">
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Solution quality</span></b></span></span></span>

	<ul style="list-style-type:disc;">
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Structure and organization</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Separation of concerns</span></span></span></span></li>
	</ul>
	</li>
</ol>

<p style="margin-left:96px;">&nbsp;</p>

<ol start="6">
	<li><span style="font-size:11pt;"><span style="line-height:115%;"><span style="font-family:Calibri,sans-serif;"><b><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Bonus Points</span></b></span></span></span>

	<ul>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Patterns &amp; Practises</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Production readiness</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Choice of communications protocol</span></span></span></span></li>
		<li><span style="font-size:11pt;"><span style="line-height:normal;"><span style="font-family:Calibri,sans-serif;"><span lang="EN-GB" style="font-family:&quot;Cascadia Code&quot;;">Docker</span></span></span></span><span style="display: none;">&nbsp;</span></li>
	</ul>
	</li>
</ol>
