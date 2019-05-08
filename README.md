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

```
CREATE TABLE `push_task` (
  `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `task_id` varchar(64) DEFAULT NULL COMMENT '标题和内容的md5值，用来判断相同内容',
  `msg_id` varchar(64) DEFAULT NULL COMMENT '推送平台返回的值',
  `lang` varchar(16) DEFAULT NULL COMMENT '语言，中文和英文',
  `tag` varchar(255) DEFAULT NULL COMMENT '用于第三方推送平台设置tag',
  `platform` smallint(5) DEFAULT '0' COMMENT '推送平台，0：all，1：iOS，2：Android',
  `push_source` smallint(5) DEFAULT '0' COMMENT '推送源：极光，友盟等',
  `status` smallint(5) DEFAULT '0' COMMENT '推送状态，0待发送，1：处理中，2：处理成功，3：处理失败，4取消任务',
  `type` smallint(5) DEFAULT '0' COMMENT '自定义类型',
  `uid` int(11) DEFAULT '0' COMMENT '推送人ID，可以没有',
  `title` varchar(255) DEFAULT NULL COMMENT '推送标题',
  `content` varchar(255) DEFAULT NULL COMMENT '推送内容',
  `device_token` text NOT NULL COMMENT '设备token，第三方推送平台使用',
  `plan_at` int(11) DEFAULT '0' COMMENT '计划推送时间',
  `channel` varchar(255) DEFAULT NULL COMMENT '渠道，用来分组，可以没有',
  `app_version` varchar(32) DEFAULT NULL COMMENT '应用版本',
  `package_name` varchar(32) NOT NULL DEFAULT '' COMMENT '推送应用包名',
  `extra_data` text COMMENT '额外信息',
  `created_at` int(11) DEFAULT '0' COMMENT '创建时间',
  `updated_at` int(11) DEFAULT '0' COMMENT '更新时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;
```
