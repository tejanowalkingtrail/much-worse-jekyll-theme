---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "https://www.preservationaustin.org/uploads/Tejano_Trail_revised2013.pdf"
      author:  "www.preservationaustin.org"
      journal: "www.preservationaustin.org"
      note:    "revised2013."
      year:    "2013"
      url:     "https://www.preservationaustin.org/uploads/Tejano_Trail_revised2013.pdf"
      image:   "images/photo.jpg"


    - title:   "https://www.nps.gov/nts/index.htm"
      author:  "National Park Service"
      note:    "Website"
      year:    "Current"
      url:     "https://www.nps.gov/nts/index.htm"
      image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      media:
        - name: "IMDB"
          url:  "http://www.imdb.com/title/tt0133093/"

    - title:   "https://www.arcgis.com/home/index.html"
      author:  "ESRI"
      journal: "Transactions on Black Magic"
      note:    "(presented at Oz)"
      year:    "2014"
      url:     "https://www.arcgis.com/home/index.html"
      doi:     "http://dx.doi.org"
      image:   "https://images.duckduckgo.com/iu/?u=http%3A%2F%2Fimages.moviepostershop.com%2Fthe-matrix-movie-poster-1999-1020518087.jpg&f=1"
      media:
        - name: "IMDB"
          url:  "http://www.imdb.com/title/tt0133093/"


---

## Sources for Additional Research 

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
