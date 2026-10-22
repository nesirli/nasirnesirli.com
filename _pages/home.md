---
permalink: /
excerpt: "Clinical bioinformatics: benchmarked genomics pipelines and clinical-style reports."
---

I build **clinical genomics pipelines**, from raw sequencing reads to benchmarked variant calls and finished clinical reports. I also do machine learning on genomic and microbial data.

Before bioinformatics I spent over a decade in clinical laboratories, first as a clinical microbiologist and then as a laboratory manager across 26 regional sites, so I know how lab data is made and where it goes wrong. Every pipeline I build is checked against public truth sets (GIAB, SEQC2) and produces a clinical-style PDF report, the way a diagnostic lab would expect.

**Open to clinical bioinformatics roles in Ankara**: clinical genetics, molecular pathology and public-health microbiology.
{: .notice--primary}

## What I'm building

- **Clinical genomics:** a germline WGS pipeline from FASTQ to ACMG-classified variants, benchmarked on seven GIAB genomes and producing a clinical-style report.
- **Microbial genomics:** predicting erythromycin resistance in *S. aureus*, comparing a fine-tuned DNA language model (DNABERT-2) with XGBoost.

[See the portfolio]({{ '/portfolio/' | relative_url }}){: .btn .btn--primary} [About me]({{ '/about/' | relative_url }}){: .btn .btn--inverse}

## Writing

{% assign recent = site.posts | slice: 0, 3 %}
{% if recent.size > 0 %}
{% for post in recent %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>{{ post.date | date: "%B %-d, %Y" }}</small>
{% endfor %}

[All posts]({{ '/blog/' | relative_url }})
{% else %}
I write about bioinformatics, clinical genomics and machine learning. Posts are coming soon.
{% endif %}
