```uml
@startuml
start
:発注処理;
note left : <&person> 営業:新規商品の発注
:入荷商品の確認;
note left : <&person> 物流:在庫切れ、在庫補充の発注
:入荷処理;
note left : <&person> 物流:
stop
@enduml
```
