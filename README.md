

[简体中文](https://github.com/whitewatercn/rime_clinic/blob/master/README.md)  | [English](https://github.com/whitewatercn/rime_clinic/blob/master/docs/README_en.md) 

# 项目介绍

rime医学输入法，集成中英医学词库，开箱即用。欢迎补充修改提意见！

原始配置和词库基于[白霜拼音](https://github.com/iDvel/rime-ice)的 [d441930](https://github.com/gaboolic/rime-frost/commit/d441930f657d797979797220eee3c45430dc20f6) commit。

医学词库位于`clinic_dicts`文件夹中

# 常见问题

- 如何使用rime医学输入法？参考雾凇拼音的[使用说明](https://github.com/iDvel/rime-ice?tab=readme-ov-file#%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85)
- 如何从其他rime输入方案迁移数据到本方案？参考白霜拼音的[这个issue](https://github.com/gaboolic/rime-frost/issues/106)
- 输出的内容旁边的*星号、⚡闪电、𑄗无限是什么意思？[详见这里](https://github.com/gaboolic/rime-frost/issues/12)





# 中文词库（位于 `clinic_dicts/cn_dict`文件夹）

[详细介绍点此查看](./docs/dict_info.md)

⚠️注意⚠️挂载词库时请逐个挂载后部署，一次挂载多个大词库后部署可占用大量内存导致电脑卡死
简略介绍

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%
flowchart LR
    中医[中医] --> cn_tcm_origin["`cn_tcm_origin （太大，不建议直接用）中医大词库，包括穴位、中药、方剂等，正在拆分成小词库`"]
    中医[中医] --> cn_tcm_herb["`cn_tcm_herb cn_tcm_herb （暂不可用）中药词库，正在从cn_tcm_origin拆分，建议使用cn_tcm_dedulplicate`"]
    中医[中医] --> cn_tcm_patent["`cn_tcm_patent （可用）中成药词库`"]
    中医[中医] --> cn_tcm_clinicia["`cn_tcm_clinician （可用）中医临床家词库`"]
    中医[中医] --> cn_tcm_formula["`cn_tcm_formula （可用）方剂词库（现已集合伤寒论）`"]
    中医[中医] --> cn_tcm_acupuncture["`cn_tcm_acupuncture （可用）针灸穴位词库`"]
    cn_tcm_origin --> cn_tcm_dedulplicate["`cn_tcm_dedulplicate （可用）拆分到其他词库后剩下的词`"]
    cn_tcm_herb --> cn_tcm_dedulplicate

    西医[西医] --> cn_clinic_origin["`cn_clinic_origin （太大，不建议直接用）临床医学大词库，包括药理、解剖、疾病、药物名等，正在拆分成小词库，太大了，不建议直接用`"]
    西医[西医] --> cn_pharmacology["`cn_pharmacology （可用）药理学词库`"]
    西医[西医] --> cn_anatomy["`cn_anatomy （可用）解剖词库`"]
    西医[西医] --> cn_medicine_list_tiny["`cn_medicine_list_tiny （可用）西药词库，基于cn_medicine_list_origin精简，还不够精简，仍保留部分中药及中成药`"]
    西医[西医] --> cn_medicine_list_origin["`cn_medicine_list_origin （太大，不建议直接用）中西医药物大词库，包括中药，中成药、西药、西药制剂，正在拆分成小词库`"]
    cn_clinic_origin --> cn_clinic_dedulpicate["`cn_clinic_dedulpicate 拆分到其他词库后剩下的词`"]
    cn_medicine_list_origin --> cn_medicine_list_dedulplicate["`cn_medicine_list_dedulplicate 拆分到其他词库后剩下的词`"]        
```

# 英文词库（位于 `clinic_dicts/en_dict`文件夹）

[详细介绍点此查看](./docs/dict_info.md)

⚠️注意⚠️挂载词库时请逐个挂载后部署，一次挂载多个大词库后部署可占用大量内存导致电脑卡死

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%

flowchart LR
    通用[通用] --> en_google["`en_google （可用）高频通用英文词汇`"]
    西医[西医] --> en_MAVL["`en_MAVL （推荐使用）高频西医词汇`"]
    西医[西医] --> en_disease["`en_disease （可用）英文疾病名`"]
    西医[西医] --> en_anatomy["`en_anatomy （可用）英文解剖`"]
    西医[西医] --> en_medication["`en_medication （可用）英文药物`"]
    西医[西医] --> en_medical_speciality["`en_medical_speciality （可用）英文医学专业`"]
    西医[西医] --> en_clinic_origin["`en_clinic_origin （太大，不建议直接用）英文医学大词库，包括疾病、药物等，正在拆分成小词库`"]
    西医[西医] --> en_respiratory["`en_respiratory 英文呼吸科词库`"]
    中医[中医暂无]

```

⚠️注意⚠️挂载词库时请逐个挂载后部署，一次挂载多个大词库后部署可占用大量内存导致电脑卡死

# 感谢

- [深蓝词库转换](https://github.com/studyzy/imewlconverter)：本仓库的很多词库由搜狗等词库使用该工具转换而来，使用方法见[如何在Linux上使用深蓝词库转换（以Google colab为例——基于Ubuntu）](https://forum.beginner.center/t/topic/719)
- [rime-ice](https://github.com/iDvel/rime-ice)：该项目作者提供了rime相关的很多帮助
- [rime-frost](https://github.com/gaboolic/rime-frost)：该项目基于rime-ice进行了很多词库优化
- [hallelujahIM(哈利路亚英文输入法)](https://github.com/dongyuwei/hallelujahIM) ：该项目直接提供了 `google.dict.yaml`词库来源
- [rimetool](https://github.com/whitewatercn/rimetool)：为了满足更多需求，本人开发的多功能rime工具
- [RIME-LMDG](https://github.com/amzxyz/RIME-LMDG)：基于32GB超大规模语料的RIME中文语法模型与词库构建

# 版权

词库收集自互联网公开信息，如侵犯版权请联系删除

## Star History


![Star History Chart](https://api.star-history.com/svg?repos=whitewatercn/rime_clinic&type=Date)

![Alt](https://repobeats.axiom.co/api/embed/ddc3e1b371f832d3eee829ecaca1266b4bffbc11.svg "Repobeats analytics image")
