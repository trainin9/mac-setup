```uml
@startuml
left to right direction

actor 経営者

rectangle システムに直接関わる人 {
  actor 顧客
  actor 営業
  actor 物流
  actor システム部門
  actor オーダー部門
  経営者 -- 営業
  経営者 -- 物流
  顧客 -- (商品販売サイト)
  営業 -- (商品販売サイト)
  物流 -- (商品販売サイト)
  システム部門 -- (商品販売サイト)
  オーダー部門 -- (商品販売サイト)
  (商品販売サイト) .. [出荷システム]
  (商品販売サイト) .. [入荷システム]
  (商品販売サイト) .. [決済システム]
}
@enduml
```
