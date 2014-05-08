依爾特系統 - Drupal 7 登入器
==========

何謂依爾特
----------

依爾特為一位php造詣有一定深度的神人我學長(以下簡稱fntsrlike)，為了學校開發的登入器

該專案網址：[Ilt_System](https://github.com/fntsrlike/ilt_system)

fntsrlike熟讀OAuth規則之後，即將OAuth規則直接應用

為何會說是直接應用，因為fntsrlike對於變數都沒有使用一般OAuth規則

所以在基本範例中，他是自行撰寫php類庫進行依爾特的使用

基本範例：[Demo Ilt](https://gist.github.com/fntsrlike/9347203)

行29: IltOAuthClient是使用他個人開發之ilt.php類庫

為何要開發模組
----------

因為我們無法使用現有之模組OAuth2和依爾特系統直接進行OAuth註冊

所以必須將此部分畫為新的模組，連接Drupal和Ilt兩者之API

達成在Drupal上使用單鍵即可使用依爾特登入

其實也是彌補資訊社使用Drupal進行學校系統之開發

此模組將會是本人第一個開發模組，以及是資訊社之第一個私人模組

再加上依爾特是針對學校的學生開發之會員系統，比起學校官方的系統省去帳號密碼之窘境

未來搭配簡易的群組管理更是能區分學生權限

使用方法
----------

在釋出Release版本之前，請先開啟你的Drupal專案目錄

1. Terminal + Git Bash (Windows用戶請使用反斜線'\\')

		cd <Drupal_Root>/sites/all/modules
		git colne git@github.com:s890081tonyhsu/Ilt_on_Drupal.git
		mv Ilt_on_Drupal ilt_auth

2. Only Terminal on Linux (without git)

		cd <Drupal_Root>/sites/all/modules
		wget --no-check-certificate -O ilt_module.zip https://github.com/s890081tonyhsu/Ilt_on_Drupal/archive/master.zip
		unzip ilt_module.zip
		cp -r ilt_module/Ilt_on_Drupal-master ilt_auth
		( yes | ) rm -r ilt_module
		rm ilt_module.zip

3. Windows Desktop Users (without git)

		點選網站右下方之 "Download ZIP" ，儲存到你的暫存位置
		到達 <Drupal_Root>/sites/all/modules 目錄
		開啟壓縮檔，將 "Ilt_on_Drupal" 解壓縮到該目錄下方
		將 "Ilt_on_Drupal" 更名為ilt_auth

4. Git軟體用戶

		到達 <Drupal_Root>/sites/all/modules 目錄
		建立一資料夾，名為 "ilt_auth"
		使用你的軟體將該專案clone下來，你可以直接clone到該資料夾或是將clone下來的資料複製到該資料夾
		
當你使用以上方法取得此模組後，請到Drupal頁面進行設定(目前尚未完成)

		點選模組(Module)
		尋找模組名稱(Ilt OAuth Module)
		點選右方設定按鈕，把從依爾特系統取得之API key填入
		登出後，在登入頁面選擇 "使用Ilt登入"

貢獻方法
----------

如果你想貢獻此專案，請先參照依爾特專案之API以及Drupal API

  - 如果你在使用上出現問題或是有更好的建議，請對此專案發送Issue(Github用戶)或是寄送Email(s890081tonyhsu[at]gmail.com)

  - 如果你有成功改進程式碼或是新增功能者，可以對此Fork專案，並發送Pull Request給我

開發者 OtomeSound 於 2014-05-08 建立


