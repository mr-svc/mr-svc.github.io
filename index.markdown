<!-- # MR-SVS: Singing Voice Synthesis with Multi-Reference Encoder -->

## Authors

<li>Shoutong Wang (Zhejiang University) </li>
<li>Jinglin Liu (Zhejiang University) </li>
<li>Yi Ren (Zhejiang University) </li>
<li>Zhen Wang (State Key Laboratory of Media Convergence Production Technology and Systems) </li>
<li>Changliang Xu (State Key Laboratory of Media Convergence Production Technology and Systems) </li>
<li>Zhou Zhao (Zhejiang University) </li>

## Abstract

  Multi-speaker singing voice synthesis is to generate the singing voice sung by different speakers. To generalize to new speakers, previous zero-shot singing adaptation methods obtain the timbre of the target speaker with a fixed-size embedding from single reference audio. However, they face several challenges: 1) the fixed-size speaker embedding is not powerful enough to capture full details of the target timbre; 2) single reference audio does not contain sufficient timbre information of the target speaker; 3) the pitch inconsistency between different speakers also leads to a degradation in the generated voice. In this paper, we propose a new model called MR-SVS to tackle these problems. Specifically, we employ both a multi-reference encoder and a fixed-size encoder to encode the timbre of the target speaker from multiple reference audios. The Multi-reference encoder can capture more details and variations of the target timbre. Besides, we propose a well-designed pitch shift method to address the pitch inconsistency problem. Experiments indicate that our method outperforms the baseline method both in naturalness and similarity.

## Synthesis Results


Speaker 1 reference: {% include embed-audio.html src="/wavs/ref1.wav" %}


<table><thead>
<tr>
<th style="text-align: center">GT mel + Vocoder</th>
<th style="text-align: center">MR-SVS</th>
<th style="text-align: center">Baseline</th>
<th style="text-align: center">Multi-ref-only</th>
<th style="text-align: center">Single-head</th>
</tr></thead><tbody>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk1-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk1-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk1-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk1-373_3.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk1-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk1-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk1-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk1-506_25.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk1-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk1-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk1-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk1-1083_2.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk1-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk1-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk1-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk1-1182_2.wav" %}
</tr>
</tbody></table>


Speaker 2 reference: {% include embed-audio.html src="/wavs/ref2.wav" %}

<table><thead>
<tr>
<th style="text-align: center">GT mel + Vocoder</th>
<th style="text-align: center">MR-SVS</th>
<th style="text-align: center">Baseline</th>
<th style="text-align: center">Multi-ref-only</th>
<th style="text-align: center">Single-head</th>
</tr></thead><tbody>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk2-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk2-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk2-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk2-373_3.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk2-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk2-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk2-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk2-506_25.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk2-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk2-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk2-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk2-1083_2.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/proposed-model-spk2-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/baseline-spk2-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/mul-ref-only-spk2-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/single-head-spk2-1182_2.wav" %}
</tr>
</tbody></table>


## Conversion w/o Pitch Shift


<table><thead>
<tr>
<th style="text-align: center">GT mel + Vocoder</th>
<th style="text-align: center">Speaker 1</th>
<th style="text-align: center">Speaker 2</th>
</tr></thead><tbody>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk1-373_3.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk2-373_3.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk1-506_25.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk2-506_25.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk1-1083_2.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk2-1083_2.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/gt-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk1-1182_2.wav" %}
{% include embed-audio-cell.html src="/wavs/without-spk2-1182_2.wav" %}
</tr>
</tbody></table>


## Controlled Singing Voice Synthesis


<table><thead>
<tr>
<th style="text-align: center">Low Pitch</th>
<th style="text-align: center">Normal</th>
<th style="text-align: center">High Pitch</th>
</tr></thead><tbody>
<tr>
{% include embed-audio-cell.html src="/wavs/low-373_0.wav" %}
{% include embed-audio-cell.html src="/wavs/normal-373_0.wav" %}
{% include embed-audio-cell.html src="/wavs/high-373_0.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/low-373_8.wav" %}
{% include embed-audio-cell.html src="/wavs/normal-373_8.wav" %}
{% include embed-audio-cell.html src="/wavs/high-373_8.wav" %}
</tr>
<tr>
{% include embed-audio-cell.html src="/wavs/low-373_14.wav" %}
{% include embed-audio-cell.html src="/wavs/normal-373_14.wav" %}
{% include embed-audio-cell.html src="/wavs/high-373_14.wav" %}
</tr>
</tbody></table>
