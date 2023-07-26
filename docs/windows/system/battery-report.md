# 【Windows】バッテリーの劣化・故障具合をレポート出力で調べる方法

## バッテリーレポートとは

WindowsのタブレットPCやノートPCには、「バッテリーレポート」と呼ばれる機能があります。
これは、バッテリーの健康診断結果のようなもので、バッテリーがどの程度劣化しているか、故障しているかがわかります。

## バッテリーレポートを作成する方法

以下の手順で「バッテリーレポート」を閲覧できます。

- 「コマンドプロンプト」を開きます。

- 以下のコマンドを入力し、Enterキーを押して実行します。


```
powercfg /batteryreport /output C:\Users\＜ユーザー名＞\Desktop\battery_report.html
```

- 補足
    - 「＜ユーザー名＞」は適宜変更してください。「C:\Users\＜ユーザー名＞\Desktop\battery_report.html」はバッテリレポートを保存する場所ですが、好きなところに設定できます。
    - コマンドを実行してエラーが出た場合、コマンドプロンプトを管理者権限で実行してトライしてください。それでも駄目な場合、バッテリーが故障している可能性があります。

## バッテリーレポートから劣化度を確認する方法

- バッテリーレポート「battery-report.html」をブラウザで開きます。前述の実行例の場合はデスクトップに保存されています。

- 「Installed batteries」という項目にある「DESIGN CAPACITY(設計容量)」と「FULL CHARGE CAPACITY(満充電時の容量)」の値を比較します。

- 「DESIGN CAPACITY(設計容量)」は、新品の容量と考えてください。実際は設計値なので個体差はありますが。
「FULL CHARGE CAPACITY(満充電時の容量)」は、実際に満充電したときの容量です。
- 「DESIGN CAPACITY(設計容量)」に対して「FULL CHARGE CAPACITY(満充電時の容量)」の値が80%未満だと、劣化が進んでいると判断できます。例えば、以下の場合は「(25,316/26,810)×100=94.4%」なので、劣化はそこまでしていないとわかります。

```
Installed batteries
Information about each currently installed battery
BATTERY 1
NAME	SurfaceBattery
MANUFACTURER	SMP
SERIAL NUMBER	-
CHEMISTRY	LION
DESIGN CAPACITY	26,810 mWh
FULL CHARGE CAPACITY	25,316 mWh
CYCLE COUNT	26
```

- 他にも「Recent usage」で直近3日間のバッテリーの使用状況、「Usage History」は過去のバッテリーでの駆動時間とACアダプタでの駆動時間、「Battery capacity history」では過去に満充電にした場合の満充電容量と設計容量が確認できます。特に「Battery capacity history」を見ると、どのタイミングから劣化が進みだしたかわかります。
