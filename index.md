---
layout: page
title: <img src="assets/img/big_logo.png">
description: >
  This is the landing and main page of <span class="enigma">EnIGMA</span>
hide_description: true
sitemap: false
---

<style type="text/css">
.no-zebra-table td{
    background-color: var(--gray-bg) !important;
}

/* Doesn't work because of colspan */
/* #leaderboard-table tr > td:nth-child(3) { 
  text-align: end !important; 
} */


tr.separator-row {
    border-bottom: 2px solid var(--border-color) !important;
}

td.top-align {
    vertical-align: top; 
}

.enigma {
  background: linear-gradient(to right, #ec412b, #ec008c); 
  -webkit-text-fill-color: transparent; 
  -webkit-background-clip: text; 
  font-weight: bold;
  font-style: italic;
}
</style>

## Enhanced Interactive Generative Model Agent for CTF Challenges 

Talor Abramovich[^1], Meet Udeshi[^2], Minghao Shao[^2], Kilian Lieret[^3], Haoran Xi[^2], Kimberly Milner[^2], Sofija
Jancheska[^2], John Yang[^4], Carlos E. Jimenez[^3], Farshad Khorrami[^2], Prashanth Krishnamurthy[^2], Brendan
Dolan-Gavitt[^2], Muhammad Shafique[^5], Karthik Narasimhan[^3], Ramesh Karri[^2], and Ofir Press[^3]
{:.lead}

[^1]: *Tel-Aviv University*
[^2]: *New York University*
[^3]: *Princeton Language and Intelligence, Princeton University*
[^4]: *Stanford University*
[^5]: *New York University Abu Dhabi*

Although language model (LM) agents are demonstrating growing potential in many domains, their success in cybersecurity has been limited due to simplistic design and the lack of fundamental features for this domain. We present <span class="enigma">EnIGMA</span>, a LM agent for autonomously solving Capture The Flag (CTF) challenges. <span class="enigma">EnIGMA</span> introduces new *Agent-Computer Interfaces* (ACIs) to  improve the success rate on CTF challenges. We establish the novel *Interactive Agent Tools* concept, which enables LM agents to run interactive command-line utilities essential for these challenges. Empirical analysis of <span class="enigma">EnIGMA</span> on over 350 CTF challenges from three different benchmarks indicates that providing a robust set of new tools with demonstration of their usage helps the LM solve complex problems and achieves state-of-the-art results on the [NYU CTF](https://arxiv.org/abs/2406.05590) and [Intercode-CTF](https://openreview.net/pdf?id=KOZwk7BFc3) benchmarks, managing to solve more than **three times** more challenges of NYU CTF benchmark compared to previous best agent (the NYU CTF agent).

### Results

<table class="no-zebra-table" id="leaderboard-table"><thead>
  <tr>
    <th>Benchmark</th>
    <th>Model</th>
    <th>% Solved</th>
    <th>Date</th>
    <th>Logs/Trajectories</th>
  </tr></thead>
<tbody>
  <tr>
    <td rowspan="4" class="top-align">NYU CTF</td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td><strong>13.5</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td>7.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>9.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr class="separator-row">
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>4.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="5" class="top-align">InterCode-CTF</td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td>67.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td><strong>72.0</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>69.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://openreview.net/pdf?id=KOZwk7BFc3">InterCode-CTF Agent</a></td>
    <td>40.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr class="separator-row">
    <td><a href="https://arxiv.org/abs/2403.13793">Google DeepMind Agent</a> w/ Gemini Ultra</td>
    <td>24.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td rowspan="4" class="top-align">HackTheBox</td>
    <td><span class="enigma">EnIGMA</span> w/ Claude 3.5 Sonnet</td>
    <td><strong>26.0</strong></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4 Turbo (1106)</td>
    <td>18.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><span class="enigma">EnIGMA</span> w/ GPT-4o</td>
    <td>16.0</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://arxiv.org/abs/2406.05590">NYU CTF agent</a> w/ GPT-4 Turbo</td>
    <td>20.0</td>
    <td></td>
    <td></td>
  </tr>
</tbody></table>


### How it Works

<video controls preload="none" poster="/assets/img/Enigma Figure1.png" autoplay muted>
    <source src="/assets/video/enigma_fig1_medium.mov" type="video/mp4">
</video>
<!-- ![figure1](/assets/img/<span class="enigma">EnIGMA</span>%20Figure1.png) -->

### Interactive Agent Tools In Action

<iframe width="560" height="315" src="https://www.youtube.com/embed/IJxqOsNFiCc?si=xtIxyCcriM9FJexK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Want to try it yourself and explore our new agent? We are completly *open-source*! 

You can try it out in the [SWE-agent repository](https://github.com/princeton-nlp/SWE-agent), refer to our [documentation](https://princeton-nlp.github.io/SWE-agent/) and read our [paper](/assets/paper.pdf).


### BibTeX

~~~BibTeX
@article{
  ...
}
~~~
