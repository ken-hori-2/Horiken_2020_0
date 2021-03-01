# Horiken_2020_0

# Name（リポジトリ/プロジェクト/OSSなどの名前）
 
Horiken_2020_0
 
事前情報ありの環境において，ゴールを目指しながら各経由地を巡回し，予め指定した交差点・探索エリアで必要なノードを起動，それらの状況に対応する行動させるプログラムです．

交差点では事前に指定したWPによって一時停止，信号認識ノード起動→信号機が赤の間は停止し，青になったら自律移動再開．
探索エリアでは事前に指定したポイントで探索ノード起動→探索対象が見つかるまで何度か探索し，発見したら探索対象に0.5mまで接近し，検知完了とし本来のゴールを目指す（制限時間と再試行回数設定 ：制限時間内では見つけるまで車体回転し続け，それを設定回数分だけ繰り返し，検知できたら次の行動へ移る．検知できなくても探索を諦め次の行動へ移る）．
 
# DEMO
 
"hoge"の魅力が直感的に伝えわるデモ動画や図解を載せる
https://user-images.githubusercontent.com/73274492/109467394-745bbf00-7aae-11eb-8832-cf25e20f6db4.mp4




# Features



 
"hoge"のセールスポイントや差別化などを説明する
 
# Requirement
 
"hoge"を動かすのに必要なライブラリなどを列挙する
 
* huga 3.5.2
* hogehuga 1.0.2
 
# Installation
 
Requirementで列挙したライブラリなどのインストール方法を説明する
 
```bash
pip install huga_package
```
 
# Usage
 
DEMOの実行方法など、"hoge"の基本的な使い方を説明する
 
```bash
git clone https://github.com/hoge/~
cd examples
python demo.py
```
 
# Note
 
注意点などがあれば書く
 
# Author
 
作成情報を列挙する
 
* 作成者
* 所属
* E-mail
 
# License
ライセンスを明示する
 
"hoge" is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).
 
社内向けなら社外秘であることを明示してる
 
"hoge" is Confidential.
