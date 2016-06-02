# 環境安裝 `有標記版本的，就請物下載更舊的版本`

* # VitualBox
    * 功能：虛擬機平台
    * 最小版本：`5.0.16-105671`
    * 下載連結：https://www.virtualbox.org/

* # Vagrant
    * 功能：加強型虛擬機
    * 最小版本：`1.8.1`
    * 下載連結：https://www.virtualbox.org/


# 虛擬機安裝步驟
開始以下步驟前，請先開起git bash再操作。<br>
以下流程安裝完畢後，網頁即可預覽，瀏覽網址為`localhost`
1. `mkdir ~/vagrant`
2. `cd ~/vagrant/`
3. `git clone http://git.cdo.com.tw/HardAnonymous/fedora-23-web.git`
4. `mkdir ~/vagrant/fedora-23-web/web`
5. `cd ~/vagrant/fedora-23-web/web`
6. `git clone http://git.cdo.com.tw/HardAnonymous/laravel.git`
7. `cd ~/vagrant/fedora-23-web`
8. `vagrant up` 必須要等一段時間，視網路狀況

# 虛擬機軟體安裝 `已安裝完畢，不需再次安裝`
* `vim`<br>
VI的強化文字編輯器
* `httpd`<br>
網頁伺服器
* `mysql`<br>
資料戶文字操作介面
* `mysql-server`<br>
資料庫伺服器
* `php`<br>
網頁外掛
* `php-mysql`<br>
網頁外掛
* `node`<br>
JavaScript執行環境
* `npm`<br>
JavaScript倉儲
* `composer`<br>
php倉儲

# 虛擬機設定 `已設定完畢，不需再次設定`

* `chkconfig mariadb on`<br>
開機時啟動資料庫伺服器

* `chkconfig httpd on`<br>
開機使啟動網頁伺服器

* `composer global require "laravel/installer"`<br>
預先安裝好laravel，而後可使用laravel指令新增專案

* `composer install`<br>
安裝PHP相依套件<br>

* `npm install`<br>
安裝JS倉儲相依套件

* `sudo service mariadb start`<br>
啟動資料庫伺服器

* `sudo service httpd start`<br>
啟動網頁伺服器

# 虛擬機掛載
如果有出現mount問題，請在`git bash`底下做以下指令

```
$ vagrant plugin install vagrant-vbguest
$ vagrant up
```
