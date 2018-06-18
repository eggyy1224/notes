#松本行弘的程式世界筆記
##物件導向
###多型(polymorphysm)
用同樣的處理方法處理不同的input。可以用一致的方式操作各種不同的資料。根據資料類別的不同來挑選適當的處理方式。  

```ruby 
def box1.open
   puts "open box1"
end

def box2.open
   puts "open box2"
end

def box3.open
   puts "open box3"
end

box1.open
box2.open
box3.open

# 不一樣的物件可以呼叫同樣的方法達到多形的目的
``` 

###資料抽象化
將實作細節封裝起來，不被外部所獲得。
###繼承
可以擁有父類別的方法，需要時也可以複寫。
####prototypal inheritance：
以物件而非類別為基礎的繼承方式。
##區塊
在ruby裡面的Enumarable實作是基於類別要有each方法存在，Enumarable module會去引用本身類別的each 方法來實做在Enumarable module
##設計模式
	設計模式是將有效果的設計命名之後編錄成型路的產物。
###Open-Closed Principle:
軟體要可以擴充，但是不可以修改，就算改變了介面的實作，也不可以影響到輸出。

##Ruby on Rails
###MVC:
####M: 帶有顯示內容的物件
####V: 負責將model顯示到視窗中的物件
####C: 接收使用者輸入，藉以操作外觀與模型的物件

###Monkey patching:
活用開放類別來新增修改方法的工作。
ex:在現有類別複寫to_s方法。
####Monkey patching的目的：
1. 新增功能
2. 修改功能
3. 修正bug
4. Hook: 在呼叫方法的時候留下紀錄。

##字元編碼
搞清楚字元、字碼、字集的關係  
UTF8、UTF32、UTF16的不同

##正規表達式


