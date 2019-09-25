# UUID construction

The UUID for the actorOccupation have been calculated using the hashes of the md5 value of the cell's content. To avoid repetitions the value has been calculated using a chain. 

+ grpActorOccupation_Term_EN_singular_male_or_generic_UUID has been calculated using the hash of the value in grpActorOccupation_Term_EN_singular_male_or_generic
+ grpActorOccupation_Term_EN_plural_male_or_generic_UUID has been calculated using the hash of the value in grpActorOccupation_Term_EN_singular_male_or_generic_UUID
+ grpActorOccupation_Term_EN_singular_female_UUID has been calculated using the hash of the value in grpActorOccupation_Term_EN_plural_male_or_generic_UUID
+ grpActorOccupation_Term_EN_plural_female_UUID has been calculated using the hash of the value in grpActorOccupation_Term_EN_singular_female_UUID
+ grpActorOccupation_Term_DE_singular_male_UUID has been calculated using the hash of the value of the combination of entries (without space between them. e.g. schauspieler2CF4DA9C-69DF-46DA-89CC-CE96BCA21716) in grpActorOccupation_Term_DE_singular_male + grpActorOccupation_UUID
+ grpActorOccupation_Term_DE_plural_male_UUID  has been calculated using the hash of the value of the combination of entries (without space between them) in grpActorOccupation_Term_DE_plural_male + grpActorOccupation_Term_EN_singular_male_or_generic_UUID
+ grpActorOccupation_Term_DE_singular_female_UUID has been calculated using the hash of the value of the combination of entries (without space between them) in grpActorOccupation_Term_DE_singular_female + grpActorOccupation_UUID + grpActorOccupation_Term_EN_singular_male_or_generic_UUID
+ grpActorOccupation_Term_DE_plural_female_UUID has been calculated using the hash of the value of the combination of entries (without space between them) in grpActorOccupation_Term_DE_plural_female + grpActorOccupation_Term_EN_singular_male_or_generic_UUID + grpActorOccupation_UUID .

The mixed combination was the chosen method to keep the UUID defined by the entry hash, but avoid repetitions (some terms in the form singular and plural are the same). 

The UUID was constructed using the formula:

```python
import uuid
return str(uuid.uuid3(uuid.NAMESPACE_DNS, value.encode('utf-8')))
```

where value is the encoded value in the original cell in UTF-8


## URI structure

+ More or not more conformant with translation?
+ Can we import something else in the translation tools?

https://resources.swissartresearch.net/terminology/concept/300238469/de/form/5ff742f1-d58b-4500-bcf5-f98cbbcdc769

https://resources.swissartresearch.net/vocab/occupation/33881D50-4FE3-437B-A32C-7A21D7F81D98/de/form/d2478d3f-ac3c-3421-b8bd-7ae17e1df43a
