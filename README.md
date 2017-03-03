# db_table_report
数据库库表获取程序
1、创建库
create database system;
2、创建表

CREATE TABLE `db_table` (
  `id` int(255) NOT NULL AUTO_INCREMENT,
  `ip` varchar(20) NOT NULL,
  `type` varchar(20) DEFAULT NULL,
  `dbname` varchar(100) DEFAULT NULL,
  `table` varchar(50) DEFAULT NULL,
  `info` varchar(255) DEFAULT NULL,
  `checksum` varchar(255) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`),
  KEY `idx_db` (`dbname`),
  KEY `idx_table` (`table`),
  KEY `idx_ip_db` (`ip`,`dbname`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=63131 DEFAULT CHARSET=utf8 COMPRESSION='lz4';


3、授权根据情况自行授权即可
