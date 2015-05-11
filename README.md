*Dollar Universe Check Exchanger Files*
=============


This script is to detect old objects in the queue.
http://github.com/Automic-Community/Dollar-Universe-Check-Exchanger-Files

<!-- List of attached files -->
Contents of Solution Package:

						
								*Dollar_Universe-Exchanger_Check.zip
								
						


Documenation and Instructions
---

<div class="ipsType_textblock ipsPad_half description_content"><span><strong class="bbc">Description</strong></span><br />&nbsp;<br />In Dollar Universe, the Exchanger is is charge of:
<ul class="bbc">
<li>For Dollar Universe 5 and 6: send job of cross-node sessions from 1 node to another</li>
<li>For Dollar Universe 5: distribute objects from 1 node to another</li>
</ul>
<span><strong class="bbc">Problem</strong></span>: if there is a communication issue, the objects to send are stored in a queue and this queue can fill up and make Dollar Universe fail when there are too many objects. Any object should not stay more than 1 day in the queue.<br />&nbsp;<br /><span><strong class="bbc">Solution</strong></span>: the goal of this script is to detect old objects in the queue.<br />&nbsp;<br />&nbsp;<br /><strong class="bbc"><span>Implementation</span></strong><br />&nbsp;<br />This script should be:
<ul class="bbc">
<li>Included in a CL_INT script</li>
<li>Executed regularly on all Dollar Universe (at least once per week)</li>
</ul>
<span><strong class="bbc">Result</strong></span>: this script will not fix the issue, it will only abort if there are old records detected.<br />&nbsp;<br /><span class="bbc_underline">Example</span>:<br />&nbsp;<br />Run with no error found:<br />
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="typ">Dollar</span><span class="pln"> </span><span class="typ">Universe</span><span class="pln"> </span><span class="lit">5</span><span class="pln"> environment loaded

</span><span class="typ">Checking</span><span class="pln"> old entries </span><span class="kwd">in</span><span class="pln"> the echanger files</span><span class="pun">...</span><span class="pln">

&nbsp; </span><span class="typ">Success</span><span class="pun">:</span><span class="pln"> </span><span class="typ">No</span><span class="pln"> old entry found</span></pre>
Run with error found:<br /><br />
<pre class="prettyprint lang-auto linenums:0 prettyprinted"><span class="typ">Dollar</span><span class="pln"> </span><span class="typ">Universe</span><span class="pln"> </span><span class="lit">5</span><span class="pln"> environment loaded

</span><span class="typ">Checking</span><span class="pln"> old entries </span><span class="kwd">in</span><span class="pln"> the echanger files</span><span class="pun">...</span><span class="pln">
&nbsp; ERROR</span><span class="pun">:</span><span class="pln"> </span><span class="lit">133</span><span class="pln"> old lines found </span><span class="kwd">in</span><span class="pln"> u_fecd file
&nbsp; ERROR</span><span class="pun">:</span><span class="pln"> </span><span class="lit">132</span><span class="pln"> old lines found </span><span class="kwd">in</span><span class="pln"> u_fecl file

&nbsp; </span><span class="typ">Advice</span><span class="pun">:</span><span class="pln"> </span><span class="typ">Check</span><span class="pln"> the </span><span class="typ">Distribution</span><span class="pln"> </span><span class="typ">Exchange</span><span class="pln"> </span><span class="kwd">and</span><span class="pln"> </span><span class="typ">Job</span><span class="pln"> </span><span class="typ">Exchange</span></pre>
&nbsp;<br /><span><strong class="bbc">Note / Actions</strong></span><br />&nbsp;<br />Once if the script detects an old record you have to:
<ul class="bbc">
<li>(DU 5 &amp; 6) Node log: check the node lod and check if there are communication issues with other nodes</li>
<li>(DU 5) Distribution Exchange/Job Exchange: check the record in distribution exchange and clean the old records from there.</li>
</ul>
<p class="bbc_indent" style="margin-left: 40px;"><span><img class="bbc_img" src="http://www.orsypforum.com/uploads/gallery/album_15/gallery_299_15_5099.png" alt="Posted Image" /></span></p>
</div>

Copyright and License
---

Solutions, Templates, Actions and other content available on the Automic Marketplace subject to the Automic [Developers Distribution License] (http://automic.com/developers-distribution-license) as well as the Automic Community [Terms of Service] (http://automic.com/community-terms-of-service).
Automic does not support, maintain or warrant any content submitted by the Automic Community.



Questions or Need Help? 
---
Any questions or comments? Converse with your fellow Users in the [Automic Community] (https://community.automic.com).