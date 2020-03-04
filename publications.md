---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "Jing Xu†, Han Zhang†, Jinfang Zheng, Philippe Dovoedo, Yanbin Yin"
    title: "eCAMI: simultaneous classification and motif identification for enzyme annotation"
    month: "December"
    year: "2019"
    booktitle: "Bioinformatics"
    code: "https://github.com/zhanglabNKU/eCAMI"
    url: "https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btz908/5651014"

  - author: "Xin Su†, Jing Xu†, Yanbin Yin, Xiongwen Quan, Han Zhang"
    title: "Antimicrobial Peptide Identification Using Multi-scale Convolutional Network"
    month: "December"
    year: "2019"
    booktitle: "BMC Bioinformatics"
    code: "https://github.com/zhanglabNKU/APIN"
    url: "https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-019-3327-y"

  - author: "Xia Guo, Xue Jiang, Jing Xu, Xiongwen Quan, Min Wu, Han Zhang"
    title: "Ensemble Consensus-Guided Unsupervised Feature Selection to Identify Huntington's Disease-Associated Genes"
    month: "July"
    year: "2018"
    booktitle: "Genes"
    url: "https://www.mdpi.com/2073-4425/9/7/350"


---

## Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).
    {% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}.<br>
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}{% if pub.code %}[Code]({{pub.code}}).
    {% endif %}
{% endunless %}
{% endfor %}




