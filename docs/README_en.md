[Simplified Chinese](https://github.com/whitewatercn/rime_clinic/blob/master/README.md)  | [English](https://github.com/whitewatercn/rime_clinic/blob/master/docs/README_en.md) 

# Project Introduction

Rime Chinese-English Medical Dictionary. Contributions are welcome!

This project has been integrated into [rilinic Medical Input Method](https://github.com/whitewatercn/rilinic). You can directly use rilinic, an easy-to-use input method designed for medical practitioners.

# Chinese Dictionary (located in the `cn_dict` folder)

[Click here for detailed introduction](https://github.com/whitewatercn/rime_clinic/blob/master/docs/dict_info.md)

⚠️Note⚠️ Please mount the dictionaries one by one and then deploy. Mounting and deploying multiple large dictionaries at once can occupy a large amount of memory and cause the computer to freeze.

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%
flowchart LR
    TCM[Traditional Chinese Medicine] --> cn_tcm_origin["`cn_tcm_origin (too large, not recommended for direct use) Large TCM dictionary, including acupoints, Chinese herbs, prescriptions, etc., being split into smaller dictionaries`"]
    TCM[Traditional Chinese Medicine] --> cn_tcm_herb["`cn_tcm_herb (not available yet) Chinese herb dictionary, being split from cn_tcm_origin, recommended to use cn_tcm_dedulplicate`"]
    TCM[Traditional Chinese Medicine] --> cn_tcm_patent["`cn_tcm_patent (available) Chinese patent medicine dictionary`"]
    TCM[Traditional Chinese Medicine] --> cn_tcm_clinicia["`cn_tcm_clinician (available) TCM clinician dictionary`"]
    TCM[Traditional Chinese Medicine] --> cn_tcm_formula["`cn_tcm_formula (available) Prescription dictionary (now includes Shanghan Lun)`"]
    TCM[Traditional Chinese Medicine] --> cn_tcm_acupuncture["`cn_tcm_acupuncture (available) Acupuncture points dictionary`"]
    cn_tcm_origin --> cn_tcm_dedulplicate["`cn_tcm_dedulplicate (available) Words left after splitting into other dictionaries`"]
    cn_tcm_herb --> cn_tcm_dedulplicate

    WesternMedicine[Western Medicine] --> cn_clinic_origin["`cn_clinic_origin (too large, not recommended for direct use) Large clinical medicine dictionary, including pharmacology, anatomy, diseases, drug names, etc., being split into smaller dictionaries`"]
    WesternMedicine[Western Medicine] --> cn_pharmacology["`cn_pharmacology (available) Pharmacology dictionary`"]
    WesternMedicine[Western Medicine] --> cn_anatomy["`cn_anatomy (available) Anatomy dictionary`"]
    WesternMedicine[Western Medicine] --> cn_medicine_list_tiny["`cn_medicine_list_tiny (available) Western medicine dictionary, simplified from cn_medicine_list_origin, still retains some Chinese herbs and Chinese patent medicines`"]
    WesternMedicine[Western Medicine] --> cn_medicine_list_origin["`cn_medicine_list_origin (too large, not recommended for direct use) Large dictionary of Chinese and Western medicines, including Chinese herbs, Chinese patent medicines, Western medicines, and Western medicine preparations, being split into smaller dictionaries`"]
    cn_clinic_origin --> cn_clinic_dedulplicate["`cn_clinic_dedulplicate Words left after splitting into other dictionaries`"]
    cn_medicine_list_origin --> cn_medicine_list_dedulplicate["`cn_medicine_list_dedulplicate Words left after splitting into other dictionaries`"]        
```

# English Dictionary (located in the `en_dict` folder)

[Click here for detailed introduction](./docs/dict_info.md)

⚠️Note⚠️ Please mount the dictionaries one by one and then deploy. Mounting and deploying multiple large dictionaries at once can occupy a large amount of memory and cause the computer to freeze.

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%

flowchart LR
    General[General] --> en_google["`en_google (available) High-frequency general English vocabulary`"]
    WesternMedicine[Western Medicine] --> en_MAVL["`en_MAVL (recommended) High-frequency Western medicine vocabulary`"]
    WesternMedicine[Western Medicine] --> en_disease["`en_disease (available) English disease names`"]
    WesternMedicine[Western Medicine] --> en_anatomy["`en_anatomy (available) English anatomy`"]
    WesternMedicine[Western Medicine] --> en_medication["`en_medication (available) English medications`"]
    WesternMedicine[Western Medicine] --> en_medical_speciality["`en_medical_speciality (available) English medical specialties`"]
    WesternMedicine[Western Medicine] --> en_clinic_origin["`en_clinic_origin (too large, not recommended for direct use) Large English medical dictionary, including diseases, medications, etc., being split into smaller dictionaries`"]
    TCM[Traditional Chinese Medicine not available yet]

```

⚠️Note⚠️ Please mount the dictionaries one by one and then deploy. Mounting and deploying multiple large dictionaries at once can occupy a large amount of memory and cause the computer to freeze.

# Acknowledgements

- [Deep Blue Dictionary Converter](https://github.com/studyzy/imewlconverter): Many dictionaries in this repository were converted from Sogou and other dictionaries using this tool. For usage, see [How to use Deep Blue Dictionary Converter on Linux (example with Google Colab - based on Ubuntu)](https://forum.beginner.center/t/topic/719)
- [rime-ice](https://github.com/iDvel/rime-ice): The author of this project provided a lot of help related to Rime.
- [hallelujahIM (Hallelujah English Input Method)](https://github.com/dongyuwei/hallelujahIM): This project directly provided the source of the `google.dict.yaml` dictionary.
- [Rimetool](https://github.com/whitewatercn/rimetool): A multifunctional Rime tool developed by me to meet more needs.
- 

# Copyright

Dictionaries are collected from publicly available information on the internet. If there is any copyright infringement, please contact us for removal.

## Star History

![Star History Chart](https://api.star-history.com/svg?repos=whitewatercn/rime_clinic&type=Date)

![Alt](https://repobeats.axiom.co/api/embed/ddc3e1b371f832d3eee829ecaca1266b4bffbc11.svg "Repobeats analytics image")
