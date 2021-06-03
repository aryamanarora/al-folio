---
layout: page
title: future
permalink: /future/
description: Things to do eventually.
nav: true
---

<style>
.note {
    margin-left: 2rem!important;
    font-size: 80%;
    font-weight: 400;
}
</style>

This is a list of cool and interesting questions in computational linguistics and/or just linguistics that I don't think have been addressed (enough) in the past research. I'll probably work on some of these at some point.

### Things I need to learn
- Literally anything substantial about statistics and calculus for ML
- PyTorch
- Deep learning
- Probabilistic machine learning. <a href="https://arxiv.org/abs/1809.10756">Van de Meent et al. (2018)</a>, <a href="https://pyro.ai/">Pyro</a>.
- BERT, transformers, and attention. <a href="https://arxiv.org/abs/1706.03762">Vaswani et al. (2017)</a>
- At least the basics about some grammar frameworks: LFG, dependency grammars, Minimalism, HPSG.
- Optimality Theory

<h3>South Asian language documentation</h3>
<ul>
    <li>How can we assess where we are so far and what languages need to be studied? There's so much research work that it's hard to make sense of it all.
        <div class="note">✅ <a href="https://aryamanarora.github.io/bhasacitra/">Bhāṣācitra</a> is a start.</div>
    </li>
    <li>Find speakers of and study as many undocumented languages of the region as possible. Unsure if I will have time for this after university.
        <div class="note">✅ <a href="https://aryamanarora.github.io/kholosi/">Kholosi</a> is a start. Follow up with Rajaswa Patil on documenting Gujjari.</div>
    </li>
    <li>How can computational methods help? Check out Wav2Vec for dealing with speech, and more generally learn about low-resource NLP.</li>
</ul>
<h3>South Asian historical linguistics</h3>
<ul>
    <li>The <a href="http://www.aa.tufs.ac.jp/sarva/">SARVA project</a> is dead. Revive it and make it better (make a database that is usable, not a text file, and look towards computational identification of cognates, alignment of phonemes, strata detection, and so on).
        <div class="note">✅ Created <a href="http://jambu-clld.herokuapp.com/">Jambu</a> for the CDIAL. See how to incorporate <a href="http://kolichala.com/DEDR/">Suresh Kolichala's DEDR</a>. Write a paper at some point (computational venue and linguistic venue?) and go get more etymologised word lists from documentary linguists.</div>
    </li>
    <li>We need a massive diachronic database for all the literary languages of South Asia. How can we figure out anything with high confidence if we haven't seen all the data?</li>
    <li><strong>What is the linguistic history of Sanskrit?</strong> What kinds of language contact (particularly with now lost substrata languages) influenced its development? Can we computationally model this sort of language change?
        <div class="note">See <a href="https://crossasia-journals.ub.uni-heidelberg.de/index.php/ejvs/article/download/828/806">Witzel (1999)</a> on a comprehensive overview of substrata in Vedic Sanskrit. It seems <a href="http://www.ideals.illinois.edu/bitstream/handle/2142/26495/SLS1975v52_hock.pdf?sequence=2">Hock (1975)</a> proposed the idea. Modern research seems stagnant.</div>
    </li>
    <li>Do the language isolates of South Asia actually provide substrate loans into modern IA/Dravidian/Munda languages or have they been too isolated to do so?
        <div class="note">Not sure of the literature much here, but I think the signs point to "yes" for Burushaski, "maybe" for Nihali, and more murky for the others.</div>
    </li>
    <li>Can substrate vocabulary be automatically identified with phonotactic LMs? Is the time depth too great (presumably, substrate loans are assimilated more readily than adstrate loans)?
        <div class="note">We know that NIA languages have a lot of unidentified borrowings (e.g. Masica's work on Hindi agricultural vocab) so it would be nice for computational tools, like phonotactic language models, to be able to help here.</div>
        <div class="note">✅ Working on a paper with Chundra Cathcart. Need to actually learn probabilistic ML stuff. This is only a start at tackling the issue.</div>
    </li>
    <li>How much of the substrate vocabulary of IA is actually Munda or Dravidian, and how much is contributed by a language X ("Nishadic" or it may be multiple unrelated languages) to all three?</li>
    <li>We need to do a systematic study of toponyms, extending on Southworth (2005)'s work on Maharastra, towards the goal of finding clear substrate languages. This is how e.g. Gaulish has been reconstructed.</li>
    <li>Can we model sound change computationally when taking into account the ramifications of continuous language contact? Broadly, can we reconcile the issues with the tree model for South Asian language history using computational approaches?
        <div class="note">The work here is being done by Chundra Cathcart and Taraka Rama, mainly by the former. Cathcart mentioned in emails about a probabilistic ML model architecture for this problem but it does not seem to converge well. Can we take a deep learning approach? Check out <a href="https://arxiv.org/pdf/1908.02477.pdf">Meloni et al. (2019)</a> for Romance reconstruction.</div>
    </li>
</ul>
<h3>Phonology</h3>
<ul>
    <li>Do the perplexities calculated by a phonotactic LM (which I guess is a generative phonology model; it doesn't learn restrictions like the MaxEnt model) correlate with OT weighted violations?
        <div class="note"><a href="https://scholarworks.umass.edu/cgi/viewcontent.cgi?article=1132&context=scil">Nelson and Mayer (2020)</a> is one of the papers that came up with this model.</div>
    </li>
    <li>Can we model multilingual schwa deletion across Indo-Aryan with a phonotactic LM? What kinds of linguistic generalisations can we even extract from that kind of model?</li>
    <li>Can other architectures model phonotactics better than unidirectional RNNs? Especially curious about bidirectional models. IDK how attention works, should probably read that, but may be useful here too.</li>
</ul>
<h3>Syntax</h3>
<ul>
    <li>What the heck are compound verbs doing in South Asian languages?
        <div class="note">Read Benjamin Slade's papers and scour his bibliography.</div></li>
</ul>
<h3>Case and adpositions</h3>
<ul>
    <li>SNACS for Hindi-Urdu and eventually other South Asian languages. Can we learn cool linguistic stuff from it? Train a classifier on Hindi data (use several architectures), try to do transfer learning for other languages.
        <div class="note">✅ <a href="http://0.0.0.0:8000/papers/snacs_hindi_guidelines.pdf">Arora, Venkateswaran, and Schneider (2021)</a> for guidelines. Classifier paper for EMNLP 2021.</div>
    </li>
    <li>What do language models learn about case? Like, do they learn the [+definite] context for the Hindi accusative? Would be a neat linguistic investigation.</li>
    <li>Is models learning this kind of stuff useful for upstream tasks?</li>
</ul>