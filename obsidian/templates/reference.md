---
title: "{{title}}"
authors: "{{authorString}}"
date: {{year}}
publisher: "{{containerTitle}}"
citekey: {{citekey}}
URL: "{{URL}}"
collection: ""
type: "{{entry.type}}"
tags: 
---
# {{title}}
{{pdfZoteroLink}}
> {{abstract}}

# Notes
![[{{pdfZoteroLink}}]]


----
{% for annotation in annotations %}
{% if annotation.annotatedText %}

> {{annotation.annotatedText}}
> {% endif %}
> {% if annotation.comment %}
> {{annotation.comment}}
{% endif %}
{% endfor %}


{% for annotation in annotations %}
{% if annotation.annotatedText %}
	{{annotation.annotatedText}}
	{% if annotation.color}
		{{annotation.colorCategory}} {{annotation.type | capitalize}}
	{% else %}
		{{annotation.type | capitalize }}
	{}