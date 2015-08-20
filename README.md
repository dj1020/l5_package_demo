# PHP 也有 day #18 - Laravel Package 開發實務

by Ronald

## 介紹和活用 Composer.json
1. composer init
2. 要設 repositories，不然預設會用 packagist 當做預設的函式庫，會按順序去抓自訂的 repo url，這樣就不需要把 repo 放進 packagist。
3. 設 autoload 決定 src 位置
4. classmap 設的就是 class file, 會直接 require 進來
5. scripts 可以做非常多的事！ 查 composer 頁面 <https://getcomposer.org/doc/articles/scripts.md>
    - Command Events
    - Install Events
    - Package Events
6. scripts 不只可以 run shell command，哇，可以 run 某個 class 中的靜態方法 
7. minimum-stability: [ 'dev', 'stable', 'dist', 'alpha' ]，有可能 dep 的 package 會需要用到 dev 版的 package，會報錯，但可以在 require 加入 @dev 來指定使用 dev 版。

### Composer.json - repositories

1. types: [ composer | vcs | PEAR | package ]
2. vcs: 使用 "Satis"，類似 packagist 的服務，但輕量，可以自己下載安裝建一個類似 packagist 的 server
3. package: 如果沒有上傳，可以放在檔案系統中，一個 zip 檔
4. "Satis" 是 composer 官方推薦自己架 package server 用的唷！
5. Satis 是去 "鏡像" 你的 repo

### Satis

1. 官網 <https://github.com/composer/satis>
2. 建 config.json 在安裝目錄下
3. build，build 到 web 資料夾下


## 如何使用 Packagist


## Private pacakge (Bitbucket, etc...)


## Laravel 5 Package (Service Provider, Routing, Resources, File groups)


## Package 開發實務



## Q:
1. Ranald Blog 在哪？ <http://blog.sharenjoy.com>