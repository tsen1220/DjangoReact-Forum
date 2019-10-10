# 目錄

[啟動](#啟動)

[簡介](#簡介)

[新話題](#新話題)

[留言](#留言)

[登入](#登入)

[註冊](#註冊)

# 啟動

## 前端

React/Redux 開發。

請先安裝 Node 與 Npm。

並輸入下面的指令安裝 modules。

```
$ npm install
```

啟動伺服器

```
$ npm start
```

預設 Port 為 3000，位於 localhost。

## 後端

Python Django 開發。

須先進入虛擬環境。

```
$ cd env
$ Scripts/activate
```

成功進入虛擬環境後進入 src 目錄，並安裝所需 modules。

```
$ pip install -r requirements.txt
```

安裝完成後，啟動伺服器 Server。

```
$ py manage.py runserver
```

# 介紹

這是一個簡易的論壇，使用者可以發佈談話主題，其他用戶看到感興趣的主題，可以點進去並留言，與其他用戶進行互動。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Home.jpg' alt=''>

# 新話題

使用者登入後可以在 Posts 的位置發佈主題，或至主題列最下方發佈。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Posts%202.jpg' alt=''>

需要進行登入才能發文，不然功能會被鎖定。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/beforeLogin.jpg' alt=''>

若主題發佈者是使用者本人，則可以進行刪除貼人以及改變主題內容的動作。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/revisedelete.jpg'>

說明:發佈的貼文會 Post 到後端 API，傳至資料庫，再由前端串接，並在頁面上顯示內容。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/ArticleAPI.jpg' alt=''>

# 留言

使用者進入別人開設的主題後，可以在裡面留言，與其他用戶互動。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Reply.jpg' alt=''>

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Reply2.jpg' alt=''>

同樣地，流程與發文相同，留言會 Post 到後端 API ，並在頁面上顯示留言。

且未登入一樣無法使用留言系統。

<img  src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/beforelogincomment.jpg' alt=''>

# 登入

登入頁面。

如果沒有帳號請選擇註冊。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Login.jpg' alt=''>

當登入完成後，會將登入資訊 POST 到後端，後端會回應並傳出登入的帳號以及 Token，前端接受並儲存，並使用 Redux 進行狀態管理，確認是否為登入成功的狀態，而 Login 會變更為 Logout。

後端 API 登入後的操作。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/loginAPI.jpg' alt=''>

# 註冊

註冊頁面。

輸入以下資訊即註冊完成。

<img src='https://raw.githubusercontent.com/tsen1220/DjangoReact-MessageBoard/master/intro/Signup.jpg' alt=''>

註冊完成後跟登入一樣，後端會傳出相關資訊，並使用 Redux 進行狀態管理，並變更為登入成功的狀態。
