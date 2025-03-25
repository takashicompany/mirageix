# MirageiX

<img src = "https://github.com/takashicompany/mirageix/blob/master/images/01.jpg?raw=true" width = "600px" />

MirageiX(ミラージークス)は44キーの一体型キーボードです。  
PCBを極限まで切り詰めたことでキーキャップのみが浮き出るようなビジュアルを実現しました。  
透明なアクリルケースを用いることで蜃気楼のようなキーボード表現が楽しめます。  
キー配列もTRONというキーボードの配置を参考にしているため、見た目以上にスムーズなタイピングを実現します。  
キースイッチはソケットで固定されるため、キースイッチの交換を容易に行えます。  

---

MirageiX is a 44-key integrated keyboard.  
The PCB has been trimmed to the limit to create a visual appearance in which only the keycaps seem to float.  
By using a transparent acrylic case, you can enjoy a mirage-like keyboard expression.  
The key layout is based on the TRON keyboard layout, making typing smoother than it looks.  
Keyswitches are fixed with sockets, allowing easy replacement of keyswitches.

# 部品と道具

一部の画像は遊舎工房の商品サイトのものを流用させて頂いております。

## キットに同梱されている部品

|画像|部品|個数|備考|
|:--|:--|:--|:--|
|<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/010-01.jpg?raw=true" width = "200px" />|基板|1||
|<img src = "https://github.com/user-attachments/assets/7905ab65-cbd3-40fc-ad86-46748c8f58a2" width = "200px" />|[ダイオード(SMDタイプ)](https://shop.yushakobo.jp/products/a0800di-02-100)|44|キースイッチの入力を伝達します。|
|<img src = "https://github.com/user-attachments/assets/0e29d3a8-6f48-49ca-94f1-489cd59eb975" width = "200px" />|[タクタイルスイッチ - 2pin 3.5x6x4.3mm](https://shop.yushakobo.jp/products/a0800ts-01-1)|1|ファームウェアを書き込む際に使用します。|
|<img src = "https://github.com/takashicompany/rookey/raw/master/images/build/IMG_6672.jpg?raw=true" width = "200px" />|[ウレタンクッション](https://shop.yushakobo.jp/products/a0800ur-01-6)|8|滑り止めとして底面に貼ります。|
||[ネジ(M2 5mm)](https://shop.yushakobo.jp/products/a0800n2?variant=37665432993953)|26|スペーサーとプレートを固定します。|
||[スペーサー(M2 5ミリ以上)](https://shop.yushakobo.jp/products/a0800c2)|13|スペーサーとプレートを固定します。|

## 別途用意が必要な部品

|画像|部品|個数|備考|
|:--|:--|:--|:--|
|<img src = "https://github.com/takashicompany/rookey/assets/4215759/1fe9f782-f64b-4291-b03c-e1532b05013b" width = "200px" />|[Pro Micro](https://shop.yushakobo.jp/products/21)|1|MCU(Micro Controller Unit)というキーボードの頭脳部分です。|
|<img src = "https://github.com/user-attachments/assets/d60e4af6-f18a-495d-8f19-fe73f1f5d113" width = "200px" />|[コンスルー](https://shop.yushakobo.jp/products/31?variant=37665714372769)|2|MCUの交換を容易にします。無くても組み立てることは可能ですが、故障時や組み立てミスの際にリカバリーがしやすくなります。**採用を強く推奨します。**|
|<img src = "https://github.com/user-attachments/assets/5f61fd48-66ec-4989-b5de-17fe812b2177" width = "200px" />|[キースイッチソケット(MX)](https://shop.yushakobo.jp/products/a01ps)|44|キースイッチの取り替えが用意になります。|
|<img src = "https://github.com/takashicompany/rookey/blob/master/images/build/IMG_6653.jpg?raw=true" width = "200px" />|[Cherry MX互換キースイッチ](https://shop.yushakobo.jp/collections/all-switches)|44||
|<img src = "https://github.com/takashicompany/rookey/assets/4215759/eafcac57-31fe-4c3a-829c-3cbf697e00ff" width = "200px" />|[Cherry MX軸用キーキャップ](https://shop.yushakobo.jp/collections/keycaps)|44|全て1uとなります。|

## 組み立てに必要な道具

初めての方は、[こちら](https://shop.yushakobo.jp/products/a9900to)を購入するのが確実です。

|道具|備考|
|:--|:--|
|ハンダごて|おすすめは[HAKKO FX-600](https://www.hakko.com/japan/products/hakko_fx600.html)です。[こて台](https://www.hakko.com/japan/products/hakko_kote_board.html)もあると、より作業をスムーズに進められます。|
|ハンダ|[こちら](https://www.goot.jp/products/detail/se_06008)などを使う方が多いようです。|
|ピンセット|100均などで手に入るものでも充分利用できるかと思います。|
|ニッパー|100均などで手に入るものでも充分利用できるかと思います。|

## あるとさらに完成度が高くなる道具
|道具|備考|
|:--|:--|
|マスキングテープ|キースイッチをハンダ付けする際に役立ちます。|

# 組み立て方

## 1. 基板の表裏を確認する

### 表
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/010-01.jpg?raw=true" width = "600px" />

### 裏
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/010-02.jpg?raw=true" width = "600px" />

## 2. ダイオードのハンダ付け

<!--
### スルーホール

基板にダイオードをハンダ付けします。ダイオードはキースイッチを押下した際に電流をMCUに伝達する役目を持ちます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-01.jpg?raw=true" width = "600px" />

ダイオードは基板の裏側から取付けます。ダイオードの配置箇所の「`▷|`」の縦線とダイオードの黒い線の方向が同じになるように置きます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-02.jpg?raw=true" width = "600px" />

ダイオードが基板の穴を通るように足を折り曲げます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-03.jpg?raw=true" width = "600px" />

ダイオードの足を基板に通します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-04.jpg?raw=true" width = "600px" />

反対側からダイオードの足が出ていることを確認します。
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-05.jpg?raw=true" width = "600px" />

基板とダイオードの足をハンダ付けします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-06.jpg?raw=true" width = "600px" />

ハンダ付けした後にダイオードの足をニッパーなどで切ります。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-a-07.jpg?raw=true" width = "600px" />

### SMD
-->

基板にダイオードをハンダ付けします。ダイオードはキースイッチを押下した際に電流をMCUに伝達する役目を持ちます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-b-01.jpg?raw=true" width = "600px" />

ダイオードは基板の裏側から取付けます。ダイオードの配置箇所の「`▷|`」の縦線とダイオードの線の方向が同じになるように置きます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-b-02.jpg?raw=true" width = "600px" />

基板のダイオードハンダ付け箇所の片方にハンダを事前に載せておきます。([予備ハンダ](https://www.p-ban.com/htmlmail_qanda/2019/12/))  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-b-03.jpg?raw=true" width = "600px" />

ピンセットでダイオードを掴みながら、予備ハンダを溶かしてダイオードの片側をハンダ付けします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-b-04.jpg?raw=true" width = "600px" />

もう片方もハンダ付けしたら完了です。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/020-diode-b-05.jpg?raw=true" width = "600px" />

当キーボードではありませんが、SMDダイオードのハンダ付け手順を動画にまとめたものです。

https://user-images.githubusercontent.com/4215759/126895350-43ae4cd4-408b-4ff4-ab5c-2903e0420978.mov

## 4. リセットスイッチの取り付け

リセットスイッチはファームウェアを書き込む際に使用します。

### タクタイルスイッチ

基板の表面から取り付けます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/030-reset-a-01.jpg?raw=true" width = "600px" />

タクタイルスイッチの足を基板の穴に挿し込みます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/030-reset-a-02.jpg?raw=true" width = "600px" />

基板を裏返してタクタイルスイッチの足が出ていることを確認します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/030-reset-a-03.jpg?raw=true" width = "600px" />

タクタイルスイッチの足と基板をハンダ付けします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/030-reset-a-04.jpg?raw=true" width = "600px" />


## 4. MCUの取付け

MCU(Micro Controller Unit)は簡単に説明するとキーボードの頭脳部分です。キースイッチ等の入力を処理してPC等に伝達します。  

### Pro Micro

Pro Microは基板の`表側|裏側`に取り付けます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-pm-01.jpg?raw=true" width = "600px" />

コンスルーを取り付けます。コンスルーは故障したときや組み立て手順を間違えてしまった際のリカバリーを容易にします。**使用することを強く推奨します。** 当ビルドガイドではコンスルーを用いた手順のみを公式とします。ご了承ください。 [コンスルーには向きがあります](https://zenn.dev/digitarhythm/articles/276cd44a36ed32#%E3%82%B3%E3%83%B3%E3%82%B9%E3%83%AB%E3%83%BC%E3%81%AEpromicro%E3%81%B8%E3%81%AE%E8%A3%85%E7%9D%80)ので確認の上基板に挿し込んでください。基板とのハンダ付けは不要です。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-pm-02.jpg?raw=true" width = "600px" />

Pro Microをコンスルーに挿します。この時コンスルーのピンがPro Microから出ていることを確認します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-pm-03.jpg?raw=true" width = "600px" />

Pro Microとコンスルーをハンダ付けします。**コンスルーと基板はハンダ付けしないでください。**
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-pm-04.jpg?raw=true" width = "600px" />

<!--
### Waveshare RP2040-Zero

当キーボードでは、Waveshare RP2040-Zeroを使用します。  
<img src = "https://github.com/user-attachments/assets/f00b9381-6d04-48e2-aeb9-90fa7b754eb1" width = "600px" />

下図の位置にMCUを置きます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-rp2040-zero-02.jpg?raw=true" width = "600px" />

基板のハンダ付けの銀箔とMCUのハンダ付け箇所が合致するように位置合わせを行います。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-rp2040-zero-03.jpg?raw=true" width = "600px" />

基板とMCUをハンダ付けします。置き場所がズレていないかを随時確認しながらハンダ付けを行います。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-rp2040-zero-04.jpg?raw=true" width = "600px" />

全部で23箇所をハンダ付けしたら完了です。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/040-rp2040-zero-05.jpg?raw=true" width = "600px" />
-->

## 5. ファームウェアの書き込み

ファームウェアのソースコードは[こちら](https://github.com/takashicompany/qmk_firmware/tree/master/keyboards/takashicompany/mirageix)です。

ファームウェアを書き込んで動作チェックを行います。MCUとPCを接続してください。  

<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/050-firmware-01.jpg?raw=true" width = "600px" />

### Pro Micro

*以下の項目は異なるキーボードの画像を使用していますが、手順は同様です。*

Pro Microにファームウェアを書き込みます。ファームウェアは[Remapから書き込む]()ことができます。

<img src = "https://github.com/user-attachments/assets/b1b23ce1-76be-411c-ac60-f279fc0dc829" width = "600px" />

Remapでのファームウェア書き込みは[こちら](https://docs.dailycraft.jp/buildguides/firmware/remap.html)を参照すると手順が分かりやすいかと思います。

Remapの使い方は[こちら](https://salicylic-acid3.hatenablog.com/entry/remap-manual)を参照するのが分かりやすいかと思います。

RemapでダイオードやPro Microが正しく動作するかを確認できます。USBでPCに接続しRemapを開いた後に、右下の3点リーダからTest Matrix modeを選択してください。  
<img src = "https://github.com/user-attachments/assets/bbf50785-3b81-409f-b537-e246f61435c5" width = "600px" />

金属製のピンセットなどで赤丸の箇所を通電させることで擬似的にキースイッチの入力を再現できます。スイッチソケットを用いない場合はキースイッチ用の穴同士をピンセットなどで通電させます。  
<img src = "https://github.com/takashicompany/palmslave/blob/master/images/build/IMG_1006_b.jpg?raw=true" width = "600px" />

全てのキースイッチが点灯するかを確認します。なお、分割型のキーボードの場合は、ファームウェアは左手側をUSBとして接続することを前提としているので、片手側のみを接続した場合は左手側が点灯します。  
<img src = "https://github.com/user-attachments/assets/fff6db54-1183-41e4-b80f-9ce3ca1ff5d8" width = "600px" />

もし点灯しないキーがあった場合はダイオードやスイッチソケットのハンダ付けを再度行うと改善することがあるかと思います。

## 6. キースイッチソケットの取付け

キースイッチソケットは基板とキースイッチを接続するものです。この部品を用いることでキースイッチ自体を基板にハンダ付けする必要がなくなるのでキースイッチの交換が容易になります。  

<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/060-switch-socket-01.jpg?raw=true" width = "600px" />

キースイッチソケットは基板の裏側に取付けます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/060-switch-socket-02.jpg?raw=true" width = "600px" />

基板にあるキースイッチハンダ付け箇所の片側にハンダを載せておきます。([予備ハンダ](https://www.p-ban.com/htmlmail_qanda/2019/12/))  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/060-switch-socket-03.jpg?raw=true" width = "600px" />

キースイッチソケットをピンセットで持ちながら予備ハンダを溶かしながらソケットの片側と基板をハンダ付けします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/060-switch-socket-04.jpg?raw=true" width = "600px" />

もう片方もハンダ付けをします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/060-switch-socket-05.jpg?raw=true" width = "600px" />

## 7. キースイッチとプレートの取付け

スイッチプレートに保護シートがある場合は剥がしてください。アクリル板の場合は水を少量つけてピンセットで端を持つと剥がれやすいことがあります。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-01.jpg?raw=true" width = "600px" />

基板の上にスイッチプレートを載せます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-02.jpg?raw=true" width = "600px" />

キースイッチを用意します。  
<!--
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-03.jpg?raw=true" width = "600px" />
-->
<img src = "https://github.com/takashicompany/rookey/blob/master/images/build/IMG_6653.jpg?raw=true" width = "600px" />

<!--
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-04-js-01.jpg?raw=true" width = "600px" />


<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-04-js-02.jpg?raw=true" width = "600px" />


<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-04-js-03.jpg?raw=true" width = "600px" />
-->

<!--
数個のキースイッチをスイッチプレートに挿し込んで、基板とスイッチプレートをキースイッチで仮止めします。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-04.jpg?raw=true" width = "600px" />
-->

数個のキースイッチをスイッチプレートに挿し込んで、基板とスイッチプレートをキースイッチで仮止めします。その後、全てのキースイッチを取付けます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/070-switch-05.jpg?raw=true" width = "600px" />

<!--
## 7b. ロータリーエンコーダの取付け

ロータリエンコーダは回転操作による入力が可能です。スクロール操作によく使われます。ロータリーエンコーダによっては押し込みによりキー入力が可能なものもあります。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/071-rotary-01.jpg?raw=true" width = "600px" />

基板の表面にロータリーエンコーダーを差し込みます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/071-rotary-02.jpg?raw=true" width = "600px" />

基板の裏側からロータリーエンコーダの足が出ていることを確認します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/071-rotary-03.jpg?raw=true" width = "600px" />

ロータリーエンコーダの足と基板をハンダ付けしたら完了です。
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/071-rotary-04.jpg?raw=true" width = "600px" />
-->

## 8. ボトムプレートの取付け

ボトムプレートに保護シートがある場合は剥がしてください。アクリル板の場合は水を少量つけてピンセットで端を持つと剥がれやすいことがあります。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-01.jpg?raw=true" width = "600px" />

スペーサーとネジを使用してボトムプレートとスイッチプレートを固定します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-02.jpg?raw=true" width = "600px" />

ボトムプレートの底面側からネジ穴にネジを挿します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-03.jpg?raw=true" width = "600px" />

ボトムプレートの上面側から挿したネジをスペーサーで固定します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-04.jpg?raw=true" width = "600px" />

<!--
ボトムプレートの上に基板とスイッチプレートを重ねます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-05.jpg?raw=true" width = "600px" />
-->

ボトムプレートの上に基板とスイッチプレートを重ねて、スペーサーとスイッチプレートをネジで固定します。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/080-bottom-06.jpg?raw=true" width = "600px" />

## 10. 滑り止めの貼り付け

滑り止めとしてウレタンクッションやゴム足シールを底面に貼り付けます。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/100-01.jpg?raw=true" width = "600px" />

姿勢や打鍵スタイルにあわせて滑り止めを貼ります。以下は取り付け例です。  
<img src = "https://github.com/takashicompany/mirageix/blob/master/images/build/100-02.jpg?raw=true" width = "600px" />

## 12. キーキャップの取り付け

キースイッチにキーキャップを取り付けます。  
<img src = "https://github.com/takashicompany/keyboard-name-here/blob/master/images/build/110-keycap-01.jpg?raw=true" width = "600px" />

### xx. 完成した後の楽しみ方

完成しましたら、ぜひSNSなどに写真を投稿頂ければと思います。
Twitterのハッシュタグは [`#MirageiX #自作キーボード`](https://twitter.com/search?q=%23%E8%87%AA%E4%BD%9C%E3%82%AD%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%20%23MirageiX&src=typed_query) を付けていただけると幸いです。
キットを組み立てた感想や、キーボードを使った所感などをお待ちしております！

また、毎週日曜日の１9時より実施されている[#KEEP_PD](https://twitter.com/hashtag/KEEB_PD?f=live)に投稿頂くこともオススメです。  
開催の告知は[@KEEB_PD](https://twitter.com/KEEB_PD)にて行われております。

ご不明な点などございましたら、[@takashicompany](https://twitter.com/takashicompany)にメンションやDM頂ければ回答できるかと思います。

