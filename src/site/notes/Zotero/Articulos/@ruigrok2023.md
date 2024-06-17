---
{"dg-publish":true,"permalink":"/zotero/articulos/ruigrok2023/","title":"Improved generalization of a plant-detection model for precision weed control","tags":["#zotero"]}
---


<span style="font-variant:small-caps; font-weight: bold;">Improved generalization of a plant-detection model for precision weed control</span>

---


> [!multi-column]
>
>> [!example|min-0]+ Autores
>> 
>> **FirstAuthor**:: [[Zotero/Autores/Ruigrok, Thijs\|Ruigrok, Thijs]]  
>> **Author**:: [[van Henten, Eldert\|van Henten, Eldert]]  
>> **Author**:: [[Kootstra, Gert\|Kootstra, Gert]]  
 >
>
>> [!info|wide-2]+
>>
>> - **Tipo de fuente**:: journalArticle
>> - **Referencia**:: Ruigrok T, Henten E van & Kootstra G (2023). Improved generalization of a plant-detection model for precision weed control. Computers and Electronics in Agriculture **204**, 107554.
>> - **Publicación**:: Computers and Electronics in Agriculture
>> - **DOI**:: 10.1016/j.compag.2022.107554
>> - **CiteKey**:: ruigrok2023
>> - **URL**:: https://www.sciencedirect.com/science/article/pii/S0168169922008626
>> - **Zotero Link:** 
>> - [Ruigrok et al_2023_Improved generalization of a plant-detection model for precision weed control.pdf](zotero://select/library/items/HVBXPJ9A)
>>
>> - **Ver en carpeta**: 
>> - [Ruigrok et al_2023_Improved generalization of a plant-detection model for precision weed control.pdf](file://J:\OneDrive\Articulos\Ruigrok%20et%20al_2023_Improved%20generalization%20of%20a%20plant-detection%20model%20for%20precision%20weed%20control.pdf)
>> - **tags**:: #gpt, #Basados, #MetodosEstudio



> [!abstract]+ 
>Lack of generalization in plant-detection models is one of the main challenges preventing the realization of autonomous weed-control systems. This paper investigates the effect of the train and test dataset distribution on the generalization error of a plant-detection model and uses incremental training to mitigate the said error. In this paper, we use the YOLOv3 object detector as plant-detection model. To train the model and test its generalization properties we used a broad dataset, consisting of 25 sub-datasets, sampled from multiple different geographic areas, soil types, cultivation conditions, containing variation in weeds, background vegetation, camera quality and variations in illumination. Using this dataset we evaluated the generalization error of a plant-detection model, assessed the effect of sampling training images from multiple arable fields on the generalization of our plant-detection model, we investigated the relation between the number of training images and the generalization of the plant-detection model and we applied incremental training to mitigate the generalization error of our plant-detection model on new arable fields. It was found that the average generalization error of our plant-detection model was 0.06 mAP. Increasing the number of sub-datasets for training, while keeping the total number of training images constant, increased the variation covered by the training set and improved the generalization of our plant-detection model. Adding more training images sampled from the same datasets increased the generalization further. However, this effect is limited and only holds when the new images cover new variation. Naively adding more images does not prepare the model for specific scenarios outside the training distribution. Using incremental training the model can be adapted to such scenarios and the generalization error can be mitigated. Depending on the discrepancy between the training set and the new field, finetuning on as little as 25 images can already mitigate the generalization error.


--- 

## Notes

@ruigrok2023

gpt:: Examina cómo la variabilidad en los datasets de entrenamiento afecta la generalización de los modelos de detección de plantas, utilizando incremental training para mejorar la precisión en nuevos campos agrícolas ([Ruigrok et al., 2023](zotero://select/library/items/ESBLX32R)).






---







