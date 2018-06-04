## Magento 從入門到放棄

### 下載 -> 萬事起頭難
* Composer install
* 官方安裝包

### 安裝
* command
```sh
bin/magento setup:install 
--db-host=localhost 
--db-name=silmore2 
--db-user=root  
--db-password=abcd1234 
--base-url=http://grayson.magento.cc 
--backend-frontname=admin
--admin-firstname=admin
--admin-lastname=admin
--admin-email=admin@example.com
--admin-user=admin
--admin-password=a123456789
```
* wizard
  BJ4

* php extension 
  * bc-math
  * ctype
  * curl
  * dom
  * gd, ImageMagick 6.3.7 (or later) or both
  * intl
  * mbstring
  * mcrypt
  * hash
  * openssl
  * PDO/MySQL
  * SimpleXML
  * soap
  * spl
  * libxml
  * xsl
  * zip
  * json
  * iconv

### 常用 Command -> 解救人生的利器
* `bin/magento setup:di:compile`
* `bin/magento setup:static-content:deploy`
* `bin/magento setup:upgrade`
* `bin/magento indexer:reindex`
* `bin/magento cache:clean`
* `bin/magento cache:flush`

### 檔案結構
* app/code
* app/design
* /generated  -> compile 用
* /pub
* /setup
* /var
* /update
* /vendor

### Module -> 大小寫很重要

* etc
  * adminhtml
  * frontend
  * 神奇的 `di.xml`
* Controller
  * Adminhtml
* Block
  * adminhtml
* view -> layout & template
  * frontend
    * layout
    * templates
  * adminhtml
    * layout
    * templates
    * ui_component
* Setup
  * `installSchema.php`
  * `upgradeSchema.php`
* Model
  * Model
  * Resource Model
  * Collection
  * 隱藏版：Repository Pattern


### Theme
* app/design
  * etc/view.xml
  *  frontend
    * vendor_module



### Database Table
* setup_module
* core_config_data
  * base_url
* url_rewrite
* eav_attribute
* catalog_category_entity
  * catalog_category_entity_* 
     * datetime
     * decimal
     * int
     * text
     * varchar
* catalog_product_entity
  *  catalog_product_entity_*
     * datetime
     * decimal
     * int
     * text
     * varchar


### 參考資源 -> 再找不到就拜神吧
* Alan
* 官方文件
* Magento 從入門到放棄

### 注意事項
* 大小寫很重要！大小寫很重要！
  * PHP class 字首一律大寫
  * xml 一律小寫 -> Snake Case
    * `controll_action_action.xml`
* 權限記得給
* compile 治百病
* 耦合性別太重
* 盡量使用 ORM
