---
{"dg-publish":true,"permalink":"/00-templates/template-literatura/","title":{"{ title }":null},"tags":["zotero"]}
---


<span style="font-variant:small-caps; font-weight: bold;">{{title}}</span>

---


> [!multi-column]
>
>> [!example|min-0]+ Autores
>> 
{% for type, creators in creators | groupby("creatorType") -%}
{%- for creator in creators -%}
>> **{{"First" if loop.first}}{{type | capitalize}}**::
{%- if creator.name %} [[{{creator.name}}\|{{creator.name}}]]  
{%- else %} [[{{creator.lastName}}, {{creator.firstName}}\|{{creator.lastName}}, {{creator.firstName}}]]  
{%- endif %}  
{% endfor %} >
{%- endfor %}
>
>> [!info|wide-2]+
>>
>> - **Tipo de fuente**:: {{itemType}}
>> - **Referencia**:: {{bibliography}} {%- if publicationTitle %}
>> - **Publicación**:: {{publicationTitle}} {%- endif %} {%- if publisher %} 
>> -  **Publisher**:: {{publisher}} {%- endif %} {%- if DOI %}
>> - **DOI**:: {{DOI}} {%- endif %} {%- if ISBN %}
>> - **ISBN**:: {{ISBN}} {%- endif %}
>> - **CiteKey**:: {{citekey}}
{%- if url %}
{%- if extra %}
>> - **Descripción corta**:: {{extra}}{%- endif %}
{%- if shortTitle %}
>> - **Nombre corto**:: {{shortTitle}} {%- endif %}
>> - **URL**:: {{url}}{%- endif %}
>> - **Zotero Link:** 
>> - {{pdfZoteroLink}}
>> {%- for attachment in attachments | filterby("path", "endswith", ".pdf") %}
>> - **Ver en carpeta**: 
>> - [{{attachment.title}}](file://{{attachment.path | replace(" ", "%20")}})  {%- endfor -%}
{%- if hashTags %}
>> - **tags**:: {{hashTags}} 
{%- endif %}

{% if abstractNote %}

> [!abstract]+ 
>{{abstractNote}}
{% endif %}



{%- if relation %}

## Relacionados

**Related**:: {% for relation in relations | selectattr("date", "title") %} [[@{{relation.citekey}}\|@{{relation.citekey}}]]{% if not loop.last %}, {% endif%} {% endfor %}

{%- endif %}

---


{%- if markdownNotes %} 

## Notes

@{{citekey}}

{{markdownNotes}}

{%- endif %}



{% persist "notes" %}
{% endpersist %}

---

{% persist "annotations" %}
{% set newAnnotations = annotations | filterby("date", "dateafter", lastImportDate) %}
{% if newAnnotations.length > 0 %}

## Importado: {{importDate | format("YYYY-MM-DD h:mm a")}}
{% for a in newAnnotations %}
{% if a.color == "#ffd400" %}
> [!amarillo]  
> 🟨 **Amarillo**:: {% if a.annotatedText %} {{a.annotatedText}} {% endif %} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}})) {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}} {% endif %}
 {% elif a.color == "#2ea8e5" %}
> [!azul]  
> 🟦 **Azul**:: {% if a.annotatedText %} {{a.annotatedText}} {% endif %} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}})) {% if a.comment %} 
> 📝**Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %} 
 {% elif a.color == "#a28ae5" %}
> [!morado]  
> 🟪 **Morado**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}})) {% endif %} {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
 {% elif a.color == "#ff6666" %}
> [!rojo]  
> 🟥 **Rojo**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}})) {% endif %} {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
 {% elif a.color == "#5fb236" %}
> [!verde]  
> 🟩 **Verde**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}}))  {% endif %} {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
 {% elif a.color == "#e56eee" %}
> [!rosa]  
> 🔢 **Rosa**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}}))  {% endif %} {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
 {% elif a.color == "#f19837" %}
> [!naranja]  
> 🟧 **Naranja**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}}))  {% endif %} {% if a.comment %}
>  📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
 {% elif a.color == "#aaaaaa" %}
> [!gris]  
> ⬛️ **Gris**:: {% if a.annotatedText %} {{a.annotatedText}} ([{{a.page}}](zotero://open-pdf/library/items/{{a.attachment.itemKey}}?page={{a.page}}&annotation={{a.id}}))  {% endif %} {% if a.comment %} 
> 📝 **Comentario**: {{a.comment}} {% endif %} {% if a.imageRelativePath %}
> ![[{{a.imageRelativePath}}\|{{a.imageRelativePath}}]]{% endif %}
> {% if a.hashTags %} {{a.hashTags}}  {% endif %}
> {% endif %} 
> 
{% endfor %}
{% endif %}
{% endpersist %}