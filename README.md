# 项目介绍

rime中英医学词库 欢迎补充！

# 中文词库

⚠️注意⚠️挂载词库时请逐个挂载后部署，一次挂载多个大词库后部署可占用大量内存导致电脑卡死

| 文件名                          | 主要内容                                                     | 词条数量（非及时更新 | 推荐等级 |
| ------------------------------- | ------------------------------------------------------------ | -------------------- | -------- |
| cn_tcm.dict.yaml                | 中医医学词汇 [https://pinyin.sogou.com/dict/detail/index/2739](https://pinyin.sogou.com/dict/detail/index/2739) |                      |          |
| cn_clinic.dict.yaml             | 中文医学词汇，如病名 [https://pinyin.sogou.com/dict/detail/index/15125](https://pinyin.sogou.com/dict/detail/index/15125) |                      |          |
| cn_tcm_clinician.dict.yaml      | 中医临床家姓名录，如张仲景，胡希恕                           |                      |          |
| cn_acupuncture.dict.yaml        | 穴位词库 [https://pinyin.sogou.com/dict/detail/index/75844](https://pinyin.sogou.com/dict/detail/index/75844) |                      |          |
| cn_tcm_medicine.dict.yaml       | 中药词库                                                     |                      |          |
| cn_medicine_list.dict.yaml      | 中文药品库，如次黄嘌呤鸟嘌呤转磷酸核糖基酶 [https://pinyin.sogou.com/dict/detail/index/20666](https://pinyin.sogou.com/dict/detail/index/20666) |                      |          |
| cn_anatomy                      | 中文解剖词库 [https://pinyin.sogou.com/dict/detail/index/79098](https://pinyin.sogou.com/dict/detail/index/79098) |                      |          |
| cn_medicine_list.dict_tiny.yaml | 基于`cn_medicine_list.dict.yaml`简化版本，仅保留药名，删除制剂名<br />如`阿奇霉素`保留，`阿奇霉素颗粒、阿奇霉素分散片、阿奇霉素胶囊`等制剂名删除 |                      |          |

# 英文词库

⚠️注意⚠️挂载词库时请逐个挂载后部署，一次挂载多个大词库后部署可占用大量内存导致电脑卡死

| 文件名                          | 简介                                                         | 词条数量（非及时更新 | 推荐等级 |
| ------------------------------- | ------------------------------------------------------------ | -------------------- | -------- |
| en_MAVL.dict.yaml               | The Medical Academic Vocabulary List (MAVL) 医学学术词汇表（MAVL）是Lei Lei &Liu Dilin在对270万词医学学术英语语料库和350万词医学英语教材语料库的研究基础上于2015年开发的。 MAVL在两个语料库中的覆盖率分别为19.44%和20.18%。[^1]<br>[来源](https://www.eapfoundation.com/vocab/academic/other/mavl/) | 1.5k+                | 5        |
| en_disease.dict.yaml            | 英文疾病名<br>[来源](https://github.com/CodeSante/medical-wordlist) |                      |          |
| en_anatomy.dict.yaml            | 英文解剖 <br>基于公开课本[Anatomy and Physiology by OpenStax](https://openstax.org/books/anatomy-and-physiology/pages/index) <br>[开源声明](https://openstax.org/books/anatomy-and-physiology/pages/preface) |                      |          |
| en_medication.dict.yaml         | 英文药物<br>[来源](https://github.com/CodeSante/medical-wordlist) |                      |          |
| en_medical_speciality.dict.yaml | 英文医学专业 - <br>[来源](https://github.com/CodeSante/medical-wordlist) |                      |          |
| google.dict.yaml                | Google's 1/3 million most frequent English words. - <br>[来源](http://norvig.com/ngrams/count_1w.txt) |                      |          |
| en_clinic.dict.yaml             | 英文医学词典，虽然经过清洗仍然很大，直接挂载会宕机<br>来源 [英汉汉英医学辞典](https://mdict.org/post/%E8%8B%B1%E6%B1%89%E6%B1%89%E8%8B%B1%E5%8C%BB%E5%AD%A6%E8%BE%9E%E5%85%B8/) | 44w+                 |          |
|                                 |                                                              |                      |          |

# 感谢

- [深蓝词库转换](https://github.com/studyzy/imewlconverter)：本仓库的很多词库由搜狗等词库使用该工具转换而来，使用方法见[如何在Linux上使用深蓝词库转换（以Google colab为例——基于Ubuntu）](https://forum.beginner.center/t/topic/719)

- [rime-ice](https://github.com/iDvel/rime-ice)：该项目作者提供了rime相关的很多帮助

- [hallelujahIM(哈利路亚英文输入法)](https://github.com/dongyuwei/hallelujahIM) ：该项目直接提供了`google.dict.yaml`词库来源
- [Rimetool](https://github.com/whitewatercn/rimetool)：为了满足更多需求，本人开发的多功能rime工具

- 

# 版权

词库收集自互联网公开信息，如侵犯版权请联系删除

## Star History

![Alt](https://repobeats.axiom.co/api/embed/ddc3e1b371f832d3eee829ecaca1266b4bffbc11.svg "Repobeats analytics image")

# 参考文献
[^1]: Lei, L., Liu, D. (2016) 'A new medical academic word list: A corpus-based study with enhanced methodology', _Journal of English for Academic Purposes_, Vol 22, p.42-53.