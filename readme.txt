要是用jdk1.8版本
记住导入javaLib中的那些包
img为程序使用到的图片，GUIUtil指定的位置


建表建库的语句

create database hutubill;
 
use  hutubill;
  
CREATE TABLE config (
  id int AUTO_INCREMENT,
  key_ varchar(255) ,
  value varchar(255) ,
  PRIMARY KEY (id)
)  DEFAULT CHARSET=utf8;
  
CREATE TABLE category (
  id int AUTO_INCREMENT,
  name varchar(255) ,
  PRIMARY KEY (id)
)  DEFAULT CHARSET=utf8;
  
CREATE TABLE record (
  id int AUTO_INCREMENT,
  spend int,
  cid int,
  comment varchar(255) ,
  date Date,
  PRIMARY KEY (id),
  CONSTRAINT `fk_record_category` FOREIGN KEY (`cid`) REFERENCES `category` (`id`)
)  DEFAULT CHARSET=utf8;