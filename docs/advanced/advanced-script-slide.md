# スクリプト SLIDE

Lua スクリプトを使用して SLIDE を成形し、譜面に貼り付けることができます。パラメーターを受け取れるようにし、その値に応じた処理も行うことができます。



## 呼び出し方

1. 編集ツールバーの ![選択](../../img/edit-toolbar-select.png) をクリックして選択モードに切り替えます。

2. 挿入したい位置をクリックしてカーソル (赤線) を移動させます。

3. メニューの **挿入** > **スクリプト SLIDE** をクリックします。

4. **スクリプト:** のドロップダウンリストから呼び出すスクリプトを選択することができます。



## スクリプトの例

`Margrete/scripts/slide` 内に以下の例があらかじめ入っています。

* `curve.lua` 曲線 SLIDE

* `meandering.lua` 蛇行 SLIDE

* `noise.lua` 雑音 SLIDE

* `zigzag.lua` 蛇腹 SLIDE



## スクリプトの書き方

スクリプトは `Margrete/scripts/slide` 内に拡張子 `lua` のファイルを配置することで起動時に自動で読み込まれます。



### スクリプトの初期化と main 関数

Margrete はスクリプトを初めて読み込んだときにスクリプト全体が一回だけ実行されます。その後 SLIDE を出力する際に `main` 関数が呼び出されます。(SLIDE 出力はパラメーターを操作したときのプレビュー反映も含まれます)



```lua

-- スクリプトが読み込まれたときに実行される



function main()

  -- SLIDE を出力する際に実行される

end

```



### スクリプトヘッダー

スクリプト表示名とコントロールを定義するための部分です。スクリプトの先頭に記述します。



```lua

--!mgscr-begin

--title,<title>

--!mgscr-end

```



* `title` スクリプト表示名



### コントロールの設置

![](img/script-slide-ctrls.png)  

パラメーターをユーザーが自由に編集するために、コントロールを設置することができます。個数制限はありませんが、画面に収まらなくなった場合はスクロールバーが表示されます。変数名を指定できるので、実行時に値をそのまま参照することができます。  

スクリプトヘッダーの `--!mgscr-begin` から `--!mgscr-end` までの間に 1 コントロール 1 行で記述します。



#### 小節数入力

```lua

--variable,beat,<varName>,<label>,<currentMeas>,<currentBeatNumer>,<currentBeatDenom>

```



* `varName` 変数名

* `label` 表示名

* `currentMeas` 小節数の初期値

* `currentBeatNumer` 1 小節未満の指定のための分子の初期値

* `currentBeatDenom` 1 小節未満の指定のための分母の初期値



`varName` で指定した変数には 1 小節 を 1920 とした数値が代入されます。



#### トラックバー

```lua

--variable,track,<varName>,<label>,<min>,<max>,<current>

```



* `varName` 変数名

* `label` 表示名

* `min` 最小値

* `max` 最大値

* `current` 初期値



#### トラックバー (2 の冪)

```lua

--variable,pow2track,<varName>,<label>,<min>,<max>,<current>

```



* `varName` 変数名

* `label` 表示名

* `min` 最小値 (2^min が実際の値になります)

* `max` 最大値 (2^max が実際の値になります)

* `current` 初期値 (2^current が実際の値になります)





#### チェックボックス

```lua

--variable,check,<varName>,<label>,<current>

```



* `varName` 変数名

* `label` 表示名

* `current` 初期値 (ON == 1 / OFF == 0)



`varName` で指定した変数にはチェック状態が 0 か 1 で代入されます。





### SLIDE の出力

配列変数 `g_Elements` に以下のような連想配列を挿入することで出力できます。  

最初の要素と最後の要素はそれぞれ SLIDE の始点と終点になります。



```lua

{

  x = (number),

  width = (number),

  tick = (number)

}

```



* `x` ノーツの横位置

* `width` ノーツの幅

* `tick` ノーツの時間位置 (1 小節 == 1920)



## 簡単な例

* ギザギザの SLIDE を出力します。

* Length コントロールで SLIDE の長さを、 Width コントロールで幅を調整できます。



![](img/script-slide-example.png)



```lua

--!mgscr-begin

--title,Zigzag

--variable,beat,length,Length,0,1,4

--variable,track,width,Width,1,16,4

--!mgscr-end



function main()

  for tick = 0, length, 32 do

    table.insert(g_Elements, {

      x = tick % 64 / 32 * 2,

      width = width,

      tick = tick

    })

  end

end

```

