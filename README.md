# Prog2kakushin
プログラミングⅡのGoogle colabを保存するためのリポジトリ
# プログラム１について
## 概要
&nbsp;大富豪で遊ぶことができるプログラム．

このプログラムでは、大富豪のルールを自分で設定し、そのルールでコンピュータと対戦することができる．大富豪を上手くなりたい人には役立つと思いこのプログラムを作成した．

なお、ジョーカーは１枚、階段は無しとなっている．

## 入力と出力
設定などは、出力される表示に従って数字で入力する．

大富豪でカードを場に出すときは、カードを「h2 s2 c2」などのように、半角スペース区切りで入力する．パスしたいときは「pass」と入力する．

カードは、１文字目がスート(ハート、クローバー、スペード、ダイヤ)をそれぞれ「h」,「c」,「s」,「d」に、２文字目以降が数字(3,4,5,6,7,8,9,10,J,Q,K,A,2)になるように入力する(例：ハートのクイーン：「hQ」)．なおジョーカーは「joker」と入力する．

### 入出力例
太字部分が入力、それ以外が出力です．
* * *
最初の親は player1 です．<br>
player1 の番です．<br>
(手札) player1:13枚 com1:13枚 com2:13枚 com3:14枚 <br>
場のカード：[]<br>
自分の手札：['d4', 'c6', 's7', 's8', 'c8', 'd9', 'dJ', 'sJ', 'hJ', 'cJ', 'sK', 'dA', 'cA']<br>
場に出すカード：**dJ sJ hJ cJ**<br>

革命！！

com1:pass<br>
com2:pass<br>
com3:pass<br>
場が流れます．<br>
player1 の番です．<br>
(手札) player1:9枚 com1:13枚 com2:13枚 com3:14枚 <br>
場のカード：[]<br>
自分の手札：['dA', 'cA', 'sK', 'd9', 's8', 'c8', 's7', 'c6', 'd4']<br>
場に出すカード：**dA cA**<br>
com1が出したカード:{'h9', 'c9'}<br>
com2が出したカード:{'s6', 'joker'}<br>
com3が出したカード:{'d5', 'h5'}<br>
player1 の番です．<br>
(手札) player1:7枚 com1:11枚 com2:11枚 com3:12枚<br> 
場のカード：['d5', 'h5']<br>
自分の手札：['sK', 'd9', 's8', 'c8', 's7', 'c6', 'd4']<br>
場に出すカード：**pass**<br>
* * *

## 工夫点
- 大富豪には様々なローカルルールがあるため、いくつか主流のものを実装し、設定でオンオフを切り替えられるよう工夫した．また、人数やラウンド数も変更できるようにした．

- 手札を見やすくするため、カードを自動で強さ順にソートしてから表示するようにした(革命で強さが反転した時にも対応)．
# プログラム２について
## 概要
&nbsp;数独(ナンプレ)を自動で作成、および自動で解いてくれるプログラム．

ナンプレの問題をランダムに作成してくれるため、何度でも新しい問題で楽しむことができる．

また、ナンプレの問題の答えを知りたいときにも便利なプログラムとなっている．
## 入力と出力
表示に従って数字で入力する．

ナンプレの問題及び答えは、数字の入っていない空白のマスは0と表示される．

問題を入力する場合は、上の列から順に、9桁の数字で入力する(例：「120080470」)．空白のマスは0として入力する．

### 入出力例
太字部分が入力、それ以外が出力です．
* * *
1:問題の自動生成<br>
2:問題の自動解析<br>
3:これまでに作成/入力した問題のリストを表示<br>
4:プログラムを終了<br>
ここに数字で入力：**1**<br>

問題の自動生成を行います<br>
問題生成中...<br>
生成完了<br>
[[5 0 0 2 0 6 8 4 0]<br>
 [8 0 2 5 0 1 0 3 0]<br>
 [9 0 6 0 7 4 0 0 0]<br>
 [4 2 9 6 1 0 5 8 0]<br>
 [0 0 0 0 4 0 0 0 0]<br>
 [7 0 0 9 5 8 0 1 0]<br>
 [0 0 8 0 0 0 0 0 0]<br>
 [3 5 0 0 2 7 9 6 8]<br>
 [6 9 1 0 8 5 0 7 0]]<br>
1:答えを表示<br>
2:メインメニューに戻る<br>
ここに数字で入力：**1**<br>
 答え<br>
[[5 1 7 2 3 6 8 4 9]<br>
 [8 4 2 5 9 1 7 3 6]<br>
 [9 3 6 8 7 4 1 2 5]<br>
 [4 2 9 6 1 3 5 8 7]<br>
 [1 8 5 7 4 2 6 9 3]<br>
 [7 6 3 9 5 8 2 1 4]<br>
 [2 7 8 4 6 9 3 5 1]<br>
 [3 5 4 1 2 7 9 6 8]<br>
 [6 9 1 3 8 5 4 7 2]]<br>
* * *

## 工夫点
- ナンプレの問題生成後、答えの表示をすぐにはせずに、答えを表示するかしないかを選ばせるようにした．
  また、答えを表示しないを選んだあとでも、問題のリストから答えを確認できるようにした．

- 自動解析を行いたい問題を入力するとき、なるべく直感的に入力できるようにした．
# プログラム３について
## 概要
&nbsp;迷路をランダムに生成し、画像として出力するプログラム．

迷路で遊びたいと思ったときにすぐに迷路を作ってくれるプログラムがあると、便利だと思い、このプログラムを作成した．
## 入力と出力
迷路の縦と横の長さを整数で入力する．長さは1以上である必要がある．

大きさは30×30以内を推奨．

その後、迷路の簡易的なルールと迷路が描かれた画像が表示される．

↓入出力例

![入出力例](images/work3_example.png)

迷路の形は長方形になっており、中央あたりにある緑色の円のマークがある場所がスタート地点、長方形の迷路の外側にたどり着けばゴールとなっている．なお、白の線は壁であり、この線を越えて通ることはできない．
## 工夫点
- 迷路のサイズを、好みに合わせて変えられるようにした．

- 迷路にある程度行き止まりが存在するようにし、途中で折り返すことなくスタートからゴールまで行くことのできる道が１通りのみになるようにした．
