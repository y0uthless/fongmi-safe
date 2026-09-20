完整直播配置
============

共52个频道：CCTV 1-17及5+、11个省级卫视、3个金华地区频道、
7个港台频道，以及美国、加拿大、西班牙、日本和墨西哥频道。

未加入CNN：未找到可审计且公开开放的稳定直播地址。
未加入澳门台，也未加入兵团、康巴、山东教育和延边卫视。

线路来源：
- 国内主体：Guovin/iptv-api固定快照
  57ac0b5ce3998470bd9e39e4925b1c3a88302a87
- 海外主体：iptv-org/iptv固定快照
  d26a66b0e0cfbecf5d4aef50e52a886c1ceb159b

安全边界：本包只有静态M3U和JSON模板，不包含Spider、JAR、JS、
PHP解析器、Cookie或账号Token。部分频道使用HTTP；港台、日本、ABC
等频道可能受地区限制，制作时未能从当前网络确认播放。

部署：把live-complete.m3u上传到仓库live/目录；提交后用完整40位
commit SHA替换JSON模板里的REPLACE_WITH_COMMIT_SHA，然后再次提交。
