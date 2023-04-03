# Laravel 10 Flare 錯誤追蹤

Flare 是一個為 Laravel 客製化的異常情況追蹤，它可以幫助你花更多的時間修復錯誤，而減少發現它們的時間，且方便在同一個地方追蹤所有 PHP 和 JavaScript 錯誤。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令測試你的 Flare 配置。
```sh
$ php artisan flare:test
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/debug` 來進行錯誤例外觸發。

## 畫面截圖
![](https://i.imgur.com/Ch0vBGi.png)
> 測試 Flare 配置

![](https://i.imgur.com/YY0Ez9t.png)
> 觸發錯誤例外以中斷程式流程

![](https://i.imgur.com/n2Ip0EG.png)
> 使用 Flare 確認程式錯誤的偵測