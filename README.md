# new_can_kiban_template
新CAN基板（[メインドキュメント](https://t-semi.esa.io/posts/7)）のテンプレートです。\
FDCAN1とUSART2を実装してあります。\
CubeIDE1.15.1を使用しています。\
[esa](https://t-semi.esa.io/posts/256)に具体的な使い方も含めて設定も乗っけておきました。

## 諸々の詳しい設定
### CAN
* フィルター：フィルターのモードは`FDCAN_FILTER_RANGE`で、ID1とID2はそれぞれ0と0x7ffです。
* ID：初期値は0です。変更するときは`TxHeader.Identifier`にIDを代入してください。
* パラメーターは[ここ](https://t-semi.esa.io/posts/123)からコピペしました。
* FIFO1を使用しています。
### USART
BaudRateは115200です。\
今まで通り`printf`すればパソコンのシリアルモニタに表示できます。