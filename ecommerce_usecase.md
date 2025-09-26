@startuml
left to right direction
actor "顧客" as Customer
actor "管理者" as Admin

rectangle "ルイ・ヴィトン注文販売システム" {

  ' --- 顧客のユースケース ---
  Customer --> (アカウントログイン)
  Customer --> (商品検索・在庫確認)
  Customer --> (商品選択・確認)
  Customer --> (カートに入れる)
  Customer --> (配送先・クレカ登録)
  Customer --> (支払い（クレカのみ）)
  Customer --> (注文内容確認)
  Customer --> (商品購入確定)
  Customer --> (レビュー投稿)
  Customer --> (注文キャンセル申請)

  ' --- 管理者のユースケース ---
  Admin --> (在庫確認)
  Admin --> (決済確認)
  Admin --> (発送処理／発送完了メール送信)
  Admin --> (到着確認／到着完了メール送信)
  Admin --> (注文キャンセル対応)

}
@enduml
