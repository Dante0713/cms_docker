建立 docker 環境
=====================

* 建立 docker 工作目錄

  mkdir ~/CLOUD

  cd ~/CLOUD

  git clone ssh://git@git.cloudschool.tw:2323/git-server/repos/cloudschool-docker.git .

* 下載系統專案 cloudschool-zf3

  cd ~/CLOUD/web/

  git clone ssh://git@git.cloudschool.tw:2323/git-server/repos/cloudschool-zf3.git cloudschool


* 下載中心端管理專案 cloudschool-admin

  cd ~/CLOUD/web/

  git clone ssh://git@git.cloudschool.tw:2323/git-server/repos/cloudschool-admin.git cloudschool_admin


* 多站台模式，參考 docker-composer.yml 與 nginx 設定檔的對照

docker-composer.yml 與 /etc/nginx/default.template.conf


* 將舊目錄中的 data 搬到新的環境

cp -a old-cloudschool-path/data/mysql ~/CLOUD/data/

cp -a old-cloudschool-path/data/mongodb ~/CLOUD/data/


* 執行 docker-composer

docker-composer up --build -d