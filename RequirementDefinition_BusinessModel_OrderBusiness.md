```uml
@startuml
|顧客|
start
:商品購入;
fork
  :メール確認;
  :支払い;
|オーダー担当|
fork again
  :オーダー確認;
  :入金確認;
endfork
while (入金額の差違) is (入金額と請求額に差違がある)
  :入金の差違の解消;
  if (オーダー接続) then (キャンセル)
    :オーダー取り消し;
    stop
  else (キャンセルしない)
  endif
endwhile (入金額と請求額が一致する)
:出荷指示;
fork
|顧客|
:オーダー状況の確認;
fork again
  |物流|
  :出荷業務;
  :出荷完了指示;
  |オーダー担当|
  :配達完了メール通知待ち;
  :オーダー完了登録;
endfork
stop
@enduml
```
