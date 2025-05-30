graph TD
    A[TOP (ログイン画面)] -->|一般会員ログイン| B(福利厚生事業一覧画面)
    A -->|管理者ログイン| C(管理者専用画面)

    B -->|事業パネルクリック| D[福利厚生事業詳細情報<br>(申込画面)]
    D --o|「申込」ボタン| B
    D -->|「戻る」ボタン| B

    C -->|事業パネルクリック| E[申込者一覧表示画面<br>(該当事業の申込者情報)]
    E -->|「抽選」ボタン<br>(期日経過後)| C
    C -->|マスタ更新メニュー| F(福利厚生事業マスタ更新画面)
    C -->|マスタ更新メニュー| G(福利厚生センター会員マスタ更新画面)

    subgraph 全画面共通フッター (ログイン後)
        direction LR
        Footer_UserPage_Button["会員専用ページ"ボタン]
        Footer_Logout_Button["ログアウト"ボタン]
    end

    B -.-> Footer_UserPage_Button
    D -.-> Footer_UserPage_Button
    H[会員画面<br>(申込履歴・お知らせ)]
    Footer_UserPage_Button --> H

    B -.-> Footer_Logout_Button
    D -.-> Footer_Logout_Button
    C -.-> Footer_Logout_Button
    E -.-> Footer_Logout_Button
    H -.-> Footer_Logout_Button

    Footer_Logout_Button --> A