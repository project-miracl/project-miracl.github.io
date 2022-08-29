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
<h3 class="blackpar_title" id="description">Description</h3>
<p>
The goal of our competition is to better evaluate the progress of retrieval systems and help identify limitations across diverse language settings. 
<b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"><img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL</b> has two tracks: Known-Languages Retrieval and Surprise-Languages Retrieval. We require participants to submit the top-most relevant passages for both tasks. Each participant will be evaluated for retrieval performance measured in terms of accuracy and efficiency. 
To foster training of multilingual systems, we provide the <b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">project <img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL</b> dataset: a large balanced monolingual retrieval dataset containing human-annotated data for 18 languages, summing over 300k+ training pairs.
We provide a wide variety of different model architectures as baselines, such as BM25, mDPR, mColBERT and mMonoT5. We hope the competition encourages participants to collaborate and develop systems that are robust, efficient and able to retrieve
information quickly and effectively across a multitude of languages.
</p>
<br/>
<h3 class="blackpar_title" id="data">Data details</h3>
<table>
  {% assign st = site.data.stats %}
          {% for entry in st %}
              {% assign key = entry | first %}
              {% if st[key].bold %}
                <tr>
                  <th><b>{{ st[key].lang }}</b></th>
                  <th><b>{{ st[key].q }}</b></th>
                  <th><b>{{ st[key].j }}</b></th>
                  <th><b>{{ st[key].pr }}</b></th>
                  <th><b>{{ st[key].avg }}</b></th>
                  <th><b>{{ st[key].size }}</b></th>
                </tr>
              {% else %}
                <tr>
                  <th><b>{{ st[key].lang }}</b></th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].q }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].j }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].pr }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].avg }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].size }}</th>
                </tr>
              {% endif %}
          {% endfor %}
</table>
<p><i>
	Descriptive statistics for <img class="column" width="2.5%" src="/images/raising_hands.PNG"> MIRACL. <b>Lang</b> denotes the language and ISO 639‑1 Code of the language; <b>Queries</b> denotes the number of queries; <b>Judgments</b> denotes the total number relevance judgments; <b>Positive Relevance</b> denotes the total number of positive relevance among <b>Judgments</b>, whereas <b>Avg Positive Relevance</b> is the average number of positive relevance per query; <b>Collection Size</b> denotes the number of passages in each language.
</i></p>
<br/>
<h3 class="blackpar_title" id="leaderboard">Competition and Leaderboard</h3>
<p>
We propose two tracks for our competition: <ol>
    <li> <a class="nav-link " aria-current="page" href="https://eval.ai/" target="_blank">Known-Languages Retrieval</a>This track involves retrieving the top 10 passages per query for every query that appears in the known-languages list. The participants are informed of the language they will be judged on and will be granted access to the Training and Development data for known languages. The Test data will not be shared with the public in order to avoid bias and overfitting.</li> 
    <li> <a class="nav-link " aria-current="page" href="https://eval.ai/" target="_blank">Surprise-Languages Retrieval</a>This track involves retrieving the top 10 passages for each query present in the surprise-language list. The participants will not be informed of the details of the language until two weeks before the submission deadline. The participants will not have access to any Training or Development data in order to maintain the secrecy of the surprise languages. This challenge aims to measure the robustness of a retriever model to generalize to unseen languages during training. The surprise languages will include both high-resource and low-resource languages.</li>
</ol>
</p>
<p>
For both tracks, participants are allowed to use any publicly available training data that does not contain the information from our development and test set. However, we expect to details on the nature of each training data.
</p>
<br>
<h3 class="blackpar_title" id="evaluation">Evaluation</h3>
<p>
We evaluate the models presented in the competition based on a combination of average retrieval accuracy across the test datasets for all languages and efficiency measured using model-size (i.e. complexity) and retrieval latency, similar to DynaBench (Kiela et al., 2021), where we provide an importance weight and finally provide a cumulative score. The validation set will be released so that the participants could reasonably evaluate their systems, but the overall test set will be kept confidential.
</p>
<p>
<b>Effectiveness Evaluation:</b>
We ask the participants to provide us a TREC runfile containing the top-k judgements. We will evaluate top k=10 retrieved passages for each query, consistent with prior competitions such as TREC-DL (Craswell et al., 2020) or NeuCLIR (https://neuclir.github.io/). Once the competition ends, we would run an automatic evaluation for the submitted TREC runfiles in the backend on our server on the hidden test queries and evaluate each participants model performance using nDCG@10 and rank-biased precision (RBP).
</p>
<p>
<b>Efficiency Evaluation:</b> Participants would be required to open-source their final model implementations on HuggingFace hub (https://huggingface.co/), a popular open-source platform for publicly hosting models. From the submitted model URL and brief report, we would estimate model complexity and index size. At inference, for a fair comparison of retrieval latency, each participant team would be required to provide easy and intuitive APIs to help us benchmark latencies using exact and exhaustive search similar to BEIR (Thakur et al., 2021). 
</p>
<p>
We can precisely estimate how fast or slow a system is at inference is in comparison to our baselines.
</p>
<h2 class="blackpar_title" id="organizers">Organizers</h2>
<div class="row_perso">
    <p>
        {% include organizers.html %}
    </p>
</div>
