---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---
<div style="font-family: 'Source Sans Pro', sans-serif; background: url('/images/banner_no_text.png') no-repeat; background-size: cover; user-select: none;">
	<center>
		<h2 style="font-size: 70px" class="blackpar_title" ><img class="column" width="9%" src="/images/raising_hands.PNG"> MIRACL </h2>
		<h3 class="blackpar_title">Multilingual Information Retrieval Across a Continuum of Languages</h3>
	</center>
</div>
<br>
<h2 class="blackpar_title" id="overview">Overview</h2>
<p>
We propose a new competition: <b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"><img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL</b> (Multilingual Information Retrieval Across a Continuum of Languages), which focuses on evaluation of monolingual retrieval systems across a continuum of several diverse languages. These languages have diverse typology, origin, language families and external resource coverage (containing high- and low-resource languages, i.e. languages whose textual web presence and dataset availability is either high or low). 
Prior work and datasets have focused on retrieval in English, shadowing the progress of monolingual retrieval in other languages and multilingual retrieval in multiple languages. 
</p>
<br>
<h2 class="blackpar_title" id="description">Description</h2>
<p>
The goal of our competition is to better evaluate the progress of retrieval systems and help identify limitations across diverse language settings. 
<b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"><img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL</b> has two tracks: Known-Languages Retrieval and Surprise-Languages Retrieval. We require participants to submit the top-most relevant passages for both tasks. Each participant will be evaluated for retrieval performance measured in terms of accuracy and efficiency. 
To foster training of multilingual systems, we provide the <b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">project <img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL</b> dataset: a large balanced monolingual retrieval dataset containing human-annotated data for 18 languages, summing over 300k+ training pairs.
We provide a wide variety of different model architectures as baselines, such as BM25, mDPR, mColBERT and mMonoT5. We hope the competition encourages participants to collaborate and develop systems that are robust, efficient and able to retrieve
information quickly and effectively across a multitude of languages.
</p>
<br/>
<table>
  <tr>
    <th><b>Lang</b></th>
    <th><b>Queries</b></th>
    <th><b>Judgments</b></th>
    <th><b>Positive Relevance</b></th>
    <th><b>Avg of Positive Relevance per Query</b></th>
    <th><b>Collection Size</b></th>
  </tr>
  	<th>Arabic (ar)</th>
    <th>7K</th>
    <th>75K</th>
    <th>14K </th>
    <th>1.88 </th>
    <th>2M</th>
  </tr>
  <tr>
    <th>English (en)</th>
    <th>307  </th>
    <th>3K </th>
    <th>758</th>
    <th>2.47 </th>
    <th>32K</th>
  </tr>
  <tr>
    <th>Spanish (es)</th>
    <th>1K</th>
    <th>16K</th>
    <th>7K </th>
    <th>4.72 </th>
    <th>10M</th>
  </tr>
  <tr>
    <th>Farsi (fa)</th>
    <th>3K</th>
    <th>34K</th>
    <th>7K  </th>
    <th>2.09 </th>
    <th>2M</th>
  </tr>
  <tr>
    <th>Hindi (hi)</th>
    <th>2.2K</th>
    <th>22K</th>
    <th>4.4K  </th>
    <th>2.02 </th>
    <th>506K</th>
  </tr>
  <tr>
    <th>Indonesian (id)</th>
    <th>5K</th>
    <th>50K</th>
    <th>15K </th>
    <th>3.00 </th>
    <th>479K</th>
  </tr>
  <tr>
    <th>Japanese (ja)</th>
    <th>4K</th>
    <th>44K</th>
    <th>9K  </th>
    <th>2.05 </th>
    <th>6M</th>
  </tr>
  <tr>
    <th>Korean (ko)</th>
    <th>1K</th>
    <th>13K</th>
    <th>2K  </th>
    <th>1.99 </th>
    <th>1M</th>
  </tr>
  <tr>
    <th>Russian (ru)</th>
    <th>5K</th>
    <th>50K</th>
    <th>13K</th>
    <th>2.64</th>
    <th>9M</th>
  </tr>
  <tr>
    <th>Swahili (sw)</th>
    <th>1K</th>
    <th>12K</th>
    <th>2K</th>
    <th>1.77</th>
    <th>131K</th>
  </tr>
  <tr>
    <th>Telugu (te)</th>
    <th>667</th>
    <th>13K</th>
    <th>819</th>
    <th>1.23</th>
    <th>518K</th>
  </tr>
  <tr>
    <th>Thai (th)</th>
    <th>3K</th>
    <th>31K</th>
    <th>5K  </th>
    <th>1.75 </th>
    <th>542K</th>
  </tr>
  <tr>
    <th>Chinese (zh)</th>
    <th>2K</th>
    <th>26K</th>
    <th>6K  </th>
    <th>2.44 </th>
    <th>4M</th>
  </tr>
  <tr>
    <th>TBA (Suprise)</th>
    <th>1K</th>
    <th>12K</th>
    <th>2K  </th>
    <th>2.14 </th>
    <th>297K</th>
  </tr>
  <tr>
    <th>TBA (Suprise)</th>
    <th>90   </th>
    <th>891   </th>
    <th>169</th>
    <th>1.88 </th>
    <th>15M</th>
  </tr>
  <tr>
    <th>TBA (Suprise)</th>
    <th>2K</th>
    <th>19K</th>
    <th>4K  </th>
    <th>2.00 </th>
    <th>1M</th>
  </tr>
  <tr>
    <th>TBA (Suprise)</th>
    <th>138  </th>
    <th>1K </th>
    <th>447</th>
    <th>3.24 </th>
    <th>14K</th>
  </tr>
  <tr>
    <th>TBA (Suprise)</th>
    <th>407  </th>
    <th>4K </th>
    <th>466</th>
    <th>1.14 </th>
    <th>49K</th>
  </tr>
  <tr>
    <th>Total</th>
    <th>42K</th>
    <th>434K</th>
    <th>97K</th>
    <th>-</th>
    <th>105M</th>
  </tr>
</table>
<br/>
<br/>
<h2 class="blackpar_title" id="leaderboard">Competition and Leaderboard</h2>
<p>
We propose two tracks for our competition: <ol>
	<li> <a class="nav-link " aria-current="page" href="https://eval.ai/" target="_blank">Known-Languages Retrieval</a>This track involves retrieving the top 10 passages per query for every query that appears in the known-languages list. The participants are informed of the language they will be judged on and will be granted access to the Training and Development data for known languages. The Test data will not be shared with the public in order to avoid bias and overfitting.</li> 
	<li> <a class="nav-link " aria-current="page" href="https://eval.ai/" target="_blank">Surprise-Languages Retrieval</a>This track involves retrieving the top 10 passages for each query present in the surprise-language list. The participants will not be informed of the details of the language until two weeks before the submission deadline. The participants will not have access to any Training or Development data in order to maintain the secrecy of the surprise languages. This challenge aims to measure the robustness of a retriever model to generalize to unseen languages during training. The surprise languages will include both high-resource and low-resource languages.</li>
</ol>
</p>
<p>
For both tracks, participants are allowed to use any publicly available training data that does not contain the information from our development and test set. However, we expect to details on the nature of each training data.
For both tracks, the participants are evaluated on a combination of the model's average accuracy for all languages, model design complexity and retrieval latency.
</p>
<h2 class="blackpar_title" id="organizers">Organizers</h2>
<div class="row_perso">
	<p>
		{% include organizers.html %}
	</p>
</div>
