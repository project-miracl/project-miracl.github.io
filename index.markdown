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
        <h2 style="font-size: 70px" class="blackpar_title" > MIRACL 🌍🙌🌏 </h2>
        <h3 class="blackpar_title">Multilingual Information Retrieval Across a Continuum of Languages</h3>
    </center>
</div>
<br>
<h2 class="blackpar_title" id="overview">Overview</h2>
<p>
<b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"> MIRACL 🌍🙌🌏</b> (Multilingual Information Retrieval Across a Continuum of Languages) is an <a href="https://www.wsdm-conference.org/2023/program/wsdm-cup">WSDM 2023 Cup</a> challenge that focuses on search across 18 different languages, which collectively encompass over three billion native speakers around the world.
These languages have diverse typologies, originate from many different language families, and are associated with varying amounts of available resources &mdash; including what we typically characterize as high-resource as well as low-resource languages.
The focus of this challenge is <i>monolingual</i> retrieval, where the queries and the corpus are in the <i>same</i> language (e.g., Swahili queries searching for Swahili documents).
Our goal is to spur research that will improve retrieval models across a broad continuum of languages, and thus improve information access capabilities for diverse populations around the world, particularly those that have been traditionally underserved.
</p>
<p>
With the advent and dominance of deep learning and approaches based on neural networks (particularly transformer-based models) in information retrieval and beyond, the importance of large datasets as drivers of progress is well understood.
For retrieval models in English, the <a href="https://microsoft.github.io/msmarco/">MS MARCO datasets</a> have had a transformative impact in advancing the field.
To stimulate similar advances in multilingual retrieval, we have built the <b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"> MIRACL 🌍🙌🌏</b> dataset, comprising human-annotated passage-level relevance judgments on Wikipedia for 18 languages, totaling over 600k+ training pairs.
Along with the dataset, WSDM 2023 Cup provides a common evaluation methodology, a venue for a competition-style event with prizes, a leaderboard.
To get participants off the ground quickly our team will provide easy-to-reproduce baselines.
There will be two tracks in this challenge: "known languages" and "surprise languages".
In the first, we will provide data well in advance of the submission deadline.
In the second, the identity of the languages (along with data) will only be made available at the last moment.
The "surprise languages" task emphasizes the rapid development of language-specific capabilities.
</p>

<p>
Connect with us!
<ul>
<li>📬 <a href="https://forms.gle/aCbjRQ9CPeXViWcaA">Mailing list</a></li> 
<li> 💬 <a href="https://join.slack.com/t/slack-zlr3806/shared_invite/zt-1i2xm1602-kSoVt0MUNUSDln_VMoMHDg">Slack Workspace</a></li> 
<li> 📣 <a href="https://twitter.com/project_miracl?s=21&t=Qf9LrVerhhN1hsXs1gdWhw">Twitter</a></li> 
</ul>
</p>
<br>

<h2 class="blackpar_title" id="overview">News!</h2>

<ul>
  <li>September 20, 2022: Initial announcement.</li>
  <li>Oct 19, 2022: Release training and development set of known languages.</li>
</ul>
<br>
<h2 class="blackpar_title" id="data">Dataset Details</h2>
<p>
The topics and judgment in training and development set are now released, as well as the corpora.
Checkout our <a href="https://github.com/project-miracl/miracl">Github repository</a> and <a href="https://arxiv.org/abs/2210.09984">paper</a> for more details!
</p>

<p>
The corpus used in the evaluation is drawn from Wikipedia in different languages.
The <b style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px"> MIRACL 🌍🙌🌏</b> dataset is built from <a href="https://aclanthology.org/2021.mrl-1.12/">Mr. TyDi</a> as a starting point, which is in turn built on <a href="https://aclanthology.org/2020.tacl-1.30/">TyDi QA</a>.
The following table provides the number of topics (= queries), relevance judgment (= relevance labels) for each (language, split) combination, and the number of passages and Wikipedia articles in the corpora.
</p>
<table>
  {% assign st = site.data.stats %}
          {% for entry in st %}
              {% assign key = entry | first %}
              {% if st[key].bold %}
                <tr>
                  <th><b>{{ st[key].lang }}</b></th>
                  <th><b>{{ st[key].q_train }}</b></th>
                  <th><b>{{ st[key].j_train }}</b></th>
                  <th><b>{{ st[key].q_dev }}</b></th>
                  <th><b>{{ st[key].j_dev }}</b></th>
                  <th><b>{{ st[key].q_test_a}}</b></th>
                  <th><b>{{ st[key].j_test_a }}</b></th>
                  <th><b>{{ st[key].q_test_b }}</b></th>
                  <th><b>{{ st[key].j_test_b }}</b></th>
                  <th><b>{{ st[key].n_passage }}</b></th>
                  <th><b>{{ st[key].n_article }}</b></th>
                </tr>
              {% else %}
                <tr>
                  <th><b>{{ st[key].lang }}</b></th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].q_train }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].j_train }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].q_dev }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].j_dev }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].q_test_a }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].j_test_a }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].q_test_b }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].j_test_b }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].n_passage }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].n_article }}</th>
                </tr>
              {% endif %}
          {% endfor %}
</table>
<p><i>
	Descriptive statistics for 🌍🙌🌏 MIRACL. <b>Lang</b> denotes the language and ISO 639‑1 Code of the language; <b># Q</b> denotes the number of queries; <b># J</b> denotes the total number relevance judgments (including both positive and negative judgments); <b># Passages </b> denotes the number of passages in each language and <b> # Articles </b> denotes the number of Wikipedia articles in the same language.
</i></p>
<br/>
<h2 class="blackpar_title" id="leaderboard">Challenge and Leaderboard</h2>
<p>
Our challenge follows a standard retrieval setup: test queries will be released (at different points in time for the two tasks), and participants will submit top-<i>k</i> results for each of the queries.
These results will be primarily evaluated in terms of effectiveness (i.e., relevance of the responses).
We will build a leaderboard that tracks the effectiveness of submissions.
More details to follow!
</p>
<br>
<h3 class="blackpar_title" id="schedule">Schedule</h3>
<table>
  {% assign st = site.data.schedule %}
          {% for entry in st %}
              {% assign key = entry | first %}
              {% if st[key].bold %}
                <tr>
                  <th><b>{{ st[key].date }}</b></th>
                  <th><b>{{ st[key].event }}</b></th>
                </tr>
              {% else %}
                <tr>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].date }}</th>
                  <th style="font-family: 'Source Sans Pro', sans-serif; font-size: 18px">{{ st[key].event }}</th>
                </tr>
              {% endif %}
          {% endfor %}
</table>
<br/>
<h2 class="blackpar_title" id="organizers">Organizers</h2>
<div class="row_perso">
    <p>
        {% include organizers.html %}
    </p>
</div>
