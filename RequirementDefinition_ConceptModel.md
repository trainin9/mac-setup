```uml
@startuml
object 顧客
object 販売商品
object パッケージ商品
object 仕入れ商品
object 取引先

顧客 ."*" 販売商品 : 販売する
販売商品 "*"..o パッケージ商品
販売商品 <|.. パッケージ商品
販売商品 <|.. 仕入れ商品

仕入れ商品 "*"..o 取引先 : 仕入れる
@enduml
```
