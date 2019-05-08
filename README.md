# iOS-gittest

https://github.com/googlesamples

TabHost
FragmentTabHost
Fragment
ViewPager

# 数据库
```
CREATE TABLE `push_device` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `tag` varchar(255) DEFAULT NULL,
  `alias` varchar(32) DEFAULT NULL,
  `device_id` varchar(64) DEFAULT NULL,
  `device_token` varchar(64) DEFAULT NULL,
  `platform` smallint(5) DEFAULT NULL,
  `push_source` smallint(5) DEFAULT NULL,
  `package_name` varchar(64) DEFAULT NULL,
  `app_version` varchar(32) DEFAULT NULL,
  `lang` varchar(16) DEFAULT NULL,
  `channel` varchar(32) DEFAULT NULL,
  `old_alias_list` text,
  `extras` text,
  `created_at` int(11) DEFAULT '0',
  `updated_at` int(11) DEFAULT '0',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;
```
