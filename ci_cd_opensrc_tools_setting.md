工具集
1. openLDAP on windows
2. xampp on windows
3. redmine on bitnami on windows
4. gitlab 
5. testlink on xampp on windows
6. jenkins

openLDAP安裝
1. 下載installer
2. 一直next到底

xampp
1. 下載installer
2. 一直next到底

gitlab
1. (略)

redmine
1. 下載redmine on bitnami
2. 一直next到底
3. 配置ldap
3. 建立project
4. 使用git clone --mirror將相關repo mapping到local
5. 設定windows scheduler, 每10分鐘fetch all
6. 到redmine user management page, 產生api token
7. 到redmine project management page, 設定git repo location

testlink
1. 下載testlink壓縮檔
2. 解壓到xampp/htdocs/下
3. 瀏覽器打開http://ip/testlink/install.php
4. 按提示安裝
5. 修改config.php, 配置ldap
6. 到testlink management page, 設定issue tracker system, 使用xmlrpc指向redmine對應project, xmlrpc使用redmine api token存取

jenkins
1. 下載jdk1.8, 安裝
2. 下載jenkins.war
3. 執行java -jar jenkins.war, 得到install key
4. 瀏覽器打開http://localhost:8080/install, 輸入install key, 按提示配置
5. 下載jenkins plugin(以.hbi形式), 到jenkins web page-->mamage jenkins-->manage pulgins-->advants中上傳hbi檔, 中途執依賴出錯可以忽略, 全部裝好後restart即會fix
6. 配置ldap
7. 配置jdk, git, svn, ant, publish on ssh