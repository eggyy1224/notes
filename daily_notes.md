##2018/06/08
###1. 使用devise時新增user時的參數若為array的話在`configure_xxx_parmas`方法裡要用以下形式：
```ruby
def configure_sign_up_params
   devise_parameter_sanitizer.permit(:sign_up, keys: [:name, :role,   :student_type, { :program_ids => [] } ])
end
```
上面的{progrmam_ids: []}便是陣列參數的形式。  

###2. `modlel.human_attribute_name`的用法請參照：
[這裡](https://apidock.com/rails/ActiveModel/Translation/human_attribute_name)

##2018/06/10
### 1. fire.app 會把編譯好的 css 放 `stylesheets/style.css`，因此 HTML 裡面直接寫`<link rel="stylesheet" media="screen" href="stylesheets/styles.css">` 就會載入了
### 2.  chrome debugger ->  Network tab -> 點 Img tab 可以找到 image 的 request
### 3. `$git pull rebase` <-這個指令可以將遠端的分支拉下來並且將本地端的commits rebase上去。
### 4. `git checkoout -b xxxx ->checkout a branch`<- create it if it is not exist
### 5. `git checkout -b xxxx remote-name/xxxx` -> pull a remote branch to local machine
### 6. redis-cli -> 進入redis console, flushdb -> 清掉資料庫
##2018/06/12
###1.每天記錄用到的gem功能為何。
###2.看別人的ＰＲ！！

##2018/06/13
###1. 到貨通知分類批次寄信功能需要用背景排程(sidekiq)。
###2. 要檢查使用者是否已經購買過訂閱的商品（可以考慮在使用者將商品加入購物車的時候將product_subscription改狀態）
###3. 寫一個task為過去的紀錄改狀態

##2018/06/15
###1. lighthouse ruby:2.4.0
###2. 可以在Rails專案的根目錄加一個.ruby-version檔案，內容寫指定的ruby版本即可。

##2018/06/18
###1. activerecord `or`（將兩個ActiveRecord_Relation連集再一起）方法的使用：
[點這裡](https://stackoverflow.com/questions/32753168/rails-5-activerecord-or-query)
###2.要在一個query撈出兩層的relation的data:
[點這裡](https://stackoverflow.com/questions/31545306/rails-activerecord-query-for-joining-multiple-tables)
###3.一個query要關聯兩個table
[點這裡](https://stackoverflow.com/questions/17147431/ruby-on-rails-joining-multiple-tables-and-how-to-extract-data)
###4.activerecord的寫法：
[點這裡](https://stackoverflow.com/questions/31096009/activerecord-or-query-hash-notation)

