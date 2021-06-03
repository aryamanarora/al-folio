---
layout: page
title: Computational historical linguistics 
description: Using advances in CL/NLP to improve our study of the history of South Asian languages.
img:
importance: 2
---

The study of historical linguistics in South Asia has stagnated somewhat. For Indo-Aryan and Dravidian languages, our best large-scale comparative resources are pretty old: Ralph Lilley Turner's [*CDIAL*](https://dsal.uchicago.edu/dictionaries/soas/) for Indo-Aryan is from the 1960s, and Burrow and Emeneau's [Dravidian dictionary](https://dsal.uchicago.edu/dictionaries/burrow/) is from the 1980s.

Our big resources are missing out on a lot of developments. In terms of comparative work, there's a lot going on in Munda and some in Sino-Tibetan which has been fascinating. We also have much better descriptions of previously extremely isolated languages (including Dardic and Nuristani languages of the northwest, many Sino-Tibetan languages, the isolates of South Asia like Nihali and Burushaski, the Andamanese languages, etc.) but their data has not yet been utilised in a broadly comparative way. An illustrative example: [to get a big cross-family typological database of the region, researchers have had to use a century-old linguistic survey](https://spraakbanken.gu.se/blogg/index.php/2020/09/01/griersons-linguistic-survey-of-india-as-open-access-digital-data-resource-for-studying-languages-of-south-asia/).

We have had great computational advances in the past few decades that comparative/historical linguists of the region could really benefit from applying. An example is [Chundra Cathcart's probabilistic assessment of the Inner-Outer hypothesis of Indo-Aryan using lexical data](https://arxiv.org/pdf/1912.01957.pdf).

Basically, the main issues here are that:
1. We have way too much data to deal with and we need to organise it somehow.
2. A lot of computational advances (even those already applied in historical linguistics) are yet to be applied to South Asian languages.

So, I want to fill that gap. The hope is that not only will this benefit historical/archaeological/genetic study of South Asian linguistic development, but also that by collecting our data together we can work towards improving more broadly useful NLP for South Asian languages.

## Publications
<div class="publications mt-0">
{% bibliography -f papers -q @*[labels=historical]* %}
</div>