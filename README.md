# 自用 RIME 补充中文词库

爬取时间：2026年5月31日

词库内容：

`sogou_dicts` ：所有搜狗细胞词库<br />
`misc_dicts\zhwiki.dict.yaml` ：中文 Wiktionary 词库<br />
`misc_dicts\cjk_unihan_kmandarin.dict.yaml` ： Unicode 17.0 Unihan 单字生僻字词库

我个人的使用方式是添加到雾凇的词库配置部分：

```
---
name: rime_ice
version: "2026-01-26"
import_tables:
  - cn_dicts/8105     # 字表
  - cn_dicts/41448  # 大字表（按需启用）（启用时和 8105 同时启用并放在 8105 下面）
  - misc_dicts/cjk_unihan_kmandarin  # Unicode 17.0 Unihan
  - cn_dicts/base     # 基础词库
  - cn_dicts/ext      # 扩展词库
  - cn_dicts/tencent  # 腾讯词向量（大词库，部署时间较长）
  - moegirl			  # https://github.com/outloudvi/mw2fcitx
  - cn_dicts/others   # 一些杂项

  # 建议把扩展词库放到下面，有重复词条时，最上面的权重生效
  # - mydict1           # 挂载配置目录下的 mydict1.dict.yaml 词库文件
  # - cn_dicts/mydict2  # 挂载 cn_dicts 目录里的 mydict2.dict.yaml 词库文件
  - sogou_dicts/sogou_agriculture
  - sogou_dicts/sogou_art
  - sogou_dicts/sogou_cities
  - sogou_dicts/sogou_engineering
  - sogou_dicts/sogou_entertainment
  - sogou_dicts/sogou_games
  - sogou_dicts/sogou_humanities
  - sogou_dicts/sogou_life
  - sogou_dicts/sogou_medical
  - sogou_dicts/sogou_natural_science
  - sogou_dicts/sogou_social_science
  - sogou_dicts/sogou_sports
  - misc_dicts/zhwiki
...
```