# Kous-OS
  
本プログラム群はUEFIで起動しX86-64アーキテクチャ上で動作するOSを形成します 
![screen shot](https://imgur.com/h6ZTOEM.jpg)

## 1. 変更点
(1) コマンド入力の時に ">"や"<"を使うと標準の入出力をファイルに割り当てることができます。

![enter image description here](https://imgur.com/8y0rDwU.jpg)
    
(2)   コマンド入力の時に行末に"&"をつけるとバックグラウンドで起動します。

![enter image description here](https://imgur.com/XWTbZ3G.jpg)
  
## 2. OSのコマンド

  ls         ・・・ファイルリストの表示

 ps         ・・・プロセスの表示
  
  cat      ・・・ファイルの内容を表示
  
   cp       ・・・ファイルのコピー
  
  mv     ・・・ファイルをコピーして元のファイルを消去
  
  rm      ・・・ファイルの消去

 cls      ・・・画面の消去


### edit       ・・・エディタ

テキストファイルを編集します
  
![enter image description here](https://imgur.com/lrM0GpZ.jpg)
  
・コマンドライン

edit [ファイル名]

編集キー

r ・・・ファイルを読み込む、何も入力せずEnterを押せばコマンドラインで指定したファイルが読み込まれる。

w ・・・編集内容をファイルに書き込む、何も入力せずEnterを押せばコマンドラインで指定したファイルに書き込まれる。

下矢印キー・・・下に移動

上矢印キー・・・上に移動

i・・・現在の行の直前にテキストを挿入する

挿入時にはプロンプト">"が表示される。

"."を入力すると挿入モードが解除される

a・・・現在の行の直後にテキストを挿入する

d・・・現在の行を削除する

m・・・現在の行の文字列を置換する

s・・・現在の行をマークする

c・・・マークした行を現在の行の直前に挿入する
そのままでは1行しか挿入されないが、"10c"のように直前に数字を打てばその行数分挿入される。

q・・・エディタを終了する

  
  
### asm       ・・・アセンブラ

アセンブラのソースファイルから実行可能ファイルを作成します

・コマンドライン

asm  ソースファイル [実行ファイル]

例
asm asm.s hello.efi


詳細は以下を参照して下さい

https://github.com/kousoz80/asm_x64


### orc       ・・・コンパイラ

コンパイラのソースファイルからアセンブラのソースファイルを作成します。

・コマンドライン

orc  ヘッダファイル ソースファイル

例
orc stdio.rh hello.r

※作成されるアセンブラのソースファイル名は"asm.s"に固定されています。

詳細は以下を参照して下さい

https://github.com/kousoz80/oregengo_R


## 3. 今後の予定
  
1. ~~マルチタスク化~~(完了)
2. ウィンドウマネージャの導入
3. デバイス(USB)ドライバの導入

