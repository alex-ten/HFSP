## Template .md for analysis entry

---
title:
category:
doctype:
entrynum:
---

## Template for figure

{% include caption.html 
    obj='figure' 
    num=page.entrynum 
    label='caption content' %}
[![alt]({{site.baseurl}}/img_compressed/file.name)]({{site.baseurl}}/img/file.name)