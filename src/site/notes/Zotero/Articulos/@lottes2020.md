---
{"dg-publish":true,"permalink":"/zotero/articulos/lottes2020/","title":"Robust joint stem detection and crop‐weed classification using image sequences for plant‐specific treatment in precision farming","tags":["#zotero"]}
---


<span style="font-variant:small-caps; font-weight: bold;">Robust joint stem detection and crop‐weed classification using image sequences for plant‐specific treatment in precision farming</span>

---


> [!multi-column]
>
>> [!example|min-0]+ Autores
>> 
>> **FirstAuthor**:: [[Zotero/Autores/Lottes, Philipp\|Lottes, Philipp]]  
>> **Author**:: [[Behley, Jens\|Behley, Jens]]  
>> **Author**:: [[Chebrolu, Nived\|Chebrolu, Nived]]  
>> **Author**:: [[Zotero/Autores/Milioto, Andres\|Milioto, Andres]]  
>> **Author**:: [[Stachniss, Cyrill\|Stachniss, Cyrill]]  
 >
>
>> [!info|wide-2]+
>>
>> - **Tipo de fuente**:: journalArticle
>> - **Referencia**:: Lottes P, Behley J, Chebrolu N, Milioto A & Stachniss C (2020). Robust joint stem detection and crop‐weed classification using image sequences for plant‐specific treatment in precision farming. Journal of Field Robotics **37**, 20–34.
>> - **Publicación**:: Journal of Field Robotics
>> - **DOI**:: 10.1002/rob.21901
>> - **CiteKey**:: lottes2020
>> - **URL**:: https://onlinelibrary.wiley.com/doi/10.1002/rob.21901
>> - **Zotero Link:** 
>> - [lottes2019jfr.pdf](zotero://select/library/items/3SW85SE8)
>>
>> - **Ver en carpeta**: 
>> - [lottes2019jfr.pdf](file://J:\OneDrive\Articulos\lottes2019jfr.pdf)
>> - **tags**:: #gpt, #Basados, #DeteccionAutomatica



> [!abstract]+ 
>Abstract
            Conventional farming still relies on large quantities of agrochemicals for weed management which have several negative side‐effects on the environment. Autonomous robots offer the potential to reduce the amount of chemicals applied, as robots can monitor and treat each plant in the field individually and thereby circumventing the uniform chemical treatment of the whole field. Such agricultural robots need the ability to identify individual crops and weeds in the field using sensor data and must additionally select effective treatment methods based on the type of weed. For example, certain types of weeds can only be effectively treated mechanically due to their resistance to herbicides, whereas other types can be treated trough selective spraying. In this article, we present a novel system that provides the necessary information for effective plant‐specific treatment. It estimates the stem location for weeds, which enables the robots to perform precise mechanical treatment, and at the same time provides the pixel‐accurate area covered by weeds for treatment through selective spraying. The major challenge in developing such a system is the large variability in the visual appearance that occurs in different fields. Thus, an effective classification system has to robustly handle substantial environmental changes including varying weed pressure, various weed types, different growth stages, changing visual appearance of the plants and the soil. Our approach uses an end‐to‐end trainable fully convolutional network that simultaneously estimates plant stem positions as well as the spatial extent of crop plants and weeds. It jointly learns how to detect the stems and the pixel‐wise semantic segmentation and incorporates spatial information by considering image sequences of local field strips. The jointly learned feature representation for both tasks furthermore exploits the crop arrangement information that is often present in crop fields. This information is considered even if it is only observable from the image sequences and not a single image. Such image sequences, as typically provided by robots navigating over the field along crop rows, enable our approach to robustly estimate the semantic segmentation and stem positions despite the large variations encountered in different fields. We implemented and thoroughly tested our approach on images from multiple farms in different countries. The experiments show that our system generalizes well to previously unseen fields under varying environmental conditions—a key capability to deploy such systems in the real world. Compared to state‐of‐the‐art approaches, our approach generalizes well to unseen fields and not only substantially improves the stem detection accuracy, that is, distinguishing crop and weed stems, but also improves the semantic segmentation performance.


--- 

## Notes

@lottes2020

gpt:: Se desarrolló un sistema robusto de detección conjunta de tallos y clasificación de cultivos-malezas utilizando secuencias de imágenes para tratamientos específicos de plantas en la agricultura de precisión. La metodología mostró alta precisión, mejorando el manejo específico de sitio ([Lottes et al., 2020](zotero://select/library/items/Z63DFPPC)).






---







