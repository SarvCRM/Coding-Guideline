# 1. Table Definition

All table names **MUST** be in `lower_case`.

All tables **MUST** use `InnoDB` as engine.

All tables **MUST** user `utf8` as charset.

All tables **MUST** user `utf8_unicode_ci` as collate.

~~~sql
-- --------------------------------------------------------
--
-- Table structure for table `tabel_name`
--
CREATE TABLE IF NOT EXISTS `tabel_name` (
	`id` CHAR(36) NOT NULL,
	`date_created` DATETIME DEFAULT NULL,
	`date_modified` DATETIME DEFAULT NULL,
	`created_by` VARCHAR(36) DEFAULT NULL,
	`modified_user_id` VARCHAR(36) DEFAULT NULL,
	`description` TEXT,
	`deleted` TINYINT(1) DEFAULT 0,
	`name` VARCHAR(50) NOT NULL,
	PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
~~~
