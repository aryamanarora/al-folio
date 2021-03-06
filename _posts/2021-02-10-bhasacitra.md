---
title: Bhāṣācitra
layout: post
categories: [mapping]
---

<p>Recently, I’ve been working on mapping the languages of South Asia by organising the scholarly work that has been done on individual varieties—this means sociolinguistic surveys, grammatical descriptions of standardised dialects, and any other fieldwork-based study of language. At first the goal was to organise the works that I read and reference in a way that is (1) useful to others, and (2) easy to browse through, but I came to realise that it can be useful beyond that, for more general-purpose language mapping. By plotting the locations of individual studies and dividing the map into zones around each point through some sort of <abbr data-title="So far, I’ve only tried a geographic version of the Voronoi algorithm because it is easy to implement in D3.js with the d3-geo-voronoi library.">nearest-neighbour interpolation</abbr> we can create language regions, which approximate the geographical spread of languages. The result of this is <strong><a href="https://aryamanarora.github.io/bhasacitra/">Bhāṣācitra</a>.</strong></p>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/assets/img/bhasacitra.png">
    </div>
</div>
<div class="caption">
    A view of Bhāṣācitra.
</div>

<p>You can hover to see zones and click on dots to see sublocations and references. The colour scheme is automatically generated (string to hex hashing function) so it’s a little wonky. On the tech side, this was all done through some JSON files and D3.js—I do not have the money to host a webapp for the foreseeable future and I don’t actually like coding web stuff! The data collection that went into the map was not a solitary effort: Adam Farris, Samopriya Basu, and Gopalakrishnan Ramamurthy provided a lot of the sources for Insular IA, Dardic and Pahari, and Dravidian (respectively). Some highlights:</p>

- Shina is the most studied Dardic language. Seems there is a lot of dialectal variation that makes it suitable for linguistic analysis, and there are plenty of speakers to access in both India and Pakistan.
- Sindhi and Lahnda are relatively understudied. The whole frontier region of Southern Pakistan is certainly not uninteresting, but there’s not much work being done there. This is surprising, given the sub-nationalist movements that have been so important to Pakistan’s history in that region—we’d expect linguistic work to occur there as these languages assert their unique identities.
- The Hindi region is understudied too! Cannot find sources for Chattisgarhi, Bagheli, etc. at least in English. Same for many of the Pahari lects. This is probably due to the political assertion of Hindi as the only language of the Indo-Aryan heartland, which really stifles linguistic work.

<p>The obvious issue in this approach is that linguistic work is not being done at a sufficiently fine level in South Asia to make really small zones/a very fine-grained distribution of points. (That’s not to say the there is any lack of linguistic work being done in South Asia—one of the things I’ve realised in mapping all these references is that there is plenty of work, it’s just hidden away in unpublished theses that we can only now access through <em>Shodhganga,</em> and papers in obscure non-digitised journals.)</p>

<p>The kind of data this map ideally would be built on can only really be collected in expansive dialect surveys, which are rare in South Asia. The only recent examples that come to mind are the SIL sociolinguistic surveys, which have only focused on a <abbr data-title="Northern Pakistan, some portions of the Himalayan regions, some parts of the midlands (Bhil dialects, Bundeli).">few regions of South Asia</abbr>, and the <a href="https://sdml.ac.in/">Survey of the Dialects of the Marathi Language</a>.</p>

<p>Still, it’s a useful gathering of sources that I don’t think has been done for this important linguistic zone. One of the uses may be mapping areal features: <a href="https://aryamanarora.github.io/bhasacitra/voronoi.html">here’s a prototype</a> looking at some phonological features: the presence of contrastive breathy-voicing and historical post-nasal voicing. Other things that may be interesting to map:</p>

- Writing systems
- Syntactic features, e.g. alignment systems, the use of numeral classifiers, branching
- Lexical-semantic features, e.g. case marking
- Lexicons, e.g. etymological sources for Swadesh list words or other glottochronological data

<p>There has been similar work on other regions, like Henrik Liljegren’s work on mapping and analysing the areal features and <abbr data-title="Language Contact and Relatedness in the Hindukush Region: https://hindukush.ling.su.se/">typology of Hindukush-Karakoram region languages</abbr> and Erik Anonby and Mortaza Taheri-Ardali’s <em><a href="http://iranatlas.net/index.html">Atlas of the Languages of Iran</a></em> mapping language distributions at the village level.</p>

<p>One of the data integrations I have thought of is extracting data from an etymological dictionary (like Turner’s <em>Comparative Dictionary of the Indo-Aryan Languages</em>), and, at least for phonological features, mapping out the likelihoods of individual sound changes or even a regex-based querying system for sound change. The initial extraction of data from CDIAL wasn’t so hard (it’s already digitised), but now I’m stuck on finding or making a good alignment algorithm, especially to cover things like metathesis. The usual dynamic-programming edit-distance algorithms can’t handle that very well; plus, we need to make decisions about how to measure phoneme distance (e.g. what are the distances between /pʰ p b/? /pʰ~p/ = /p~b/ or not?). I’m sure there’s work on this, but I’m totally new to it so these are just some musings. Another approach that comes to mind is something neural, sort of like the LSTM encoder-decoder in <a href="https://www.aclweb.org/anthology/2020.conll-1.50.pdf">Cathcart and Rama (2020)</a>, but for alignment instead of prediction. One idea is to train contextual phoneme embeddings, and then run something like <a href="https://arxiv.org/abs/2004.08728">Sabet et al. (2020)</a>’s Simalign algorithm. Maybe pretrain on manual alignments of tricky cases first.</p>

<p>Anyways, there’s plenty of neat stuff to be done in this system. It’s a fun side project for now (apparently, I like making datasets), maybe will result in something publishable in a more formal format someday.</p>