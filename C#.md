## C#基本文法チートシート
<table>
 <tr>
  <td>文法名</td>
  <td>詳細</td>
  <td>書き方</td>
  <td>サンプル</td>
 </tr>
 <tr>
  <td rowspan="2">コメント</td>
  <td>一行コメント</td>
  <td>先頭をスラッシュ2つ</td>
  <td>// 行末まで全部コメント</td>
 </tr>
 <tr>
  <td>複数行コメント</td>
  <td>/* */で囲う</td>
  <td>/* この中だけコメント */</td>
 </tr>
 <tr>
  <td rowspan="2">コンソール出力</td>
  <td>改行あり</td>
  <td>Console.WriteLine</td>
  <td>Console.WriteLine("Hello World");</td>
 </tr>
 <tr>
  <td>改行無し</td>
  <td>Console.Write</td>
  <td>Console.Write("Hello World");</td>
 </tr>
 <tr>
  <td rowspan="5">データ型</td>
  <td>文字列(String)</td>
  <td>string</td>
  <td>string str = "hoge";</td>
 </tr>
 <tr>
  <td>整数(Int)</td>
  <td>int</td>
  <td>int num = 10;</td>
 </tr>
 <tr>
  <td>小数(float)</td>
  <td>float, double, decimal</td>
  <td>decimal tax = 10.8;</td>
 </tr>
 <tr>
  <td>論理(bool)</td>
  <td>bool</td>
  <td>bool flag = true;</td>
 </tr>
 <tr>
  <td>日付(date)</td>
  <td>DateTime</td>
  <td>DateTime today = DateTime.Today;</td>
 </tr>
 <tr>
  <td rowspan="5">変数</td>
  <td>定数宣言（変更不可）</td>
  <td>const + データ型 + 変数名</td>
  <td>const int x = 0;</td>
 </tr>
 <tr>
  <td>変数宣言（変更可）</td>
  <td>データ型 + 変数名</td>
  <td>int x = 0;</td>
 </tr>
 <tr>
  <td>変数宣言（型推論）</td>
  <td>var + 変数名</td>
  <td>var x = 0;</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名 = 値</td>
  <td>x = 0;</td>
 </tr>
 <tr>
  <td>キャスト（型変換）</td>
  <td>(型名)変数名<br>または、文字列なら型によっては、<br>型名.Parse</td>
  <td>long longNum = 100.2;<br>int intNum = (int)longNum;<br>または、<br>string numString = "100"; <br>int intNum = int.Parse(numString);</td>
 </tr>
 <tr>
  <td rowspan="5">配列</td>
  <td>宣言</td>
  <td>型[] 変数名 = new 型[要素数]</td>
  <td>string[] strArray = new string[3];</td>
 </tr>
 <tr>
  <td>初期化</td>
  <td>型[] 変数名 = new 型[]{0番目の値, 1番目の値}</td>
  <td>string[] strArray = {"a","b","c"}; <br>または<br>string[] strArray = new string[]{"a","b","c"};</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[配列番号] = 値</td>
  <td>strArray[0] = "hoge";</td>
 </tr>
 <tr>
  <td>サイズ変更</td>
  <td>Array.Resize(変数, 要素数)</td>
  <td>Array.Resize(strArray, 10);</td>
 </tr>
 <tr>
  <td>値コピー</td>
  <td>Array.Copy(元変数, 先変数, 要素数)</td>
  <td>Array.Copy(src, dest, 10);</td>
 </tr>
 <tr>
  <td rowspan="3">リスト</td>
  <td>宣言</td>
  <td>new List<型>()<br><br>以下の記述が必要<br>using System.Linq;<br>using System.Collections.Generic;</td>
  <td>var list = new List<string>();</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[要素番号] = 値</td>
  <td>list[0] = "hoge";</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>変数名.add(値)</td>
  <td>list.add("hoge");</td>
 </tr>
 <tr>
  <td rowspan="3">連想配列（ディクショナリ）</td>
  <td>宣言</td>
  <td>new Dictionary<型,型>()</td>
  <td>var dic = new Dictionary<string,string>();</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[キー名] = 値</td>
  <td>dic["key"] = "value";</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>変数名.add(キー名,値)<br>※キーがなければ代入方式でも追加される</td>
  <td>dic.add("key", "value");</td>
 </tr>
 <tr>
  <td rowspan="7">算術演算</td>
  <td>和（足し算）</td>
  <td>+</td>
  <td>1 + 2</td>
 </tr>
 <tr>
  <td>差（引き算）</td>
  <td>-</td>
  <td>1 - 2</td>
 </tr>
 <tr>
  <td>乗（かけ算）</td>
  <td>*</td>
  <td>1 * 2</td>
 </tr>
 <tr>
  <td>除（割り算）</td>
  <td>/<br>ただし割り切れない場合は、<br>どちらか少数変換しないと<br>小数点が切り捨てになる</td>
  <td>(decimal)1 / 2; (出力:0.5)</td>
 </tr>
 <tr>
  <td>商（割り算の商）</td>
  <td>/</td>
  <td>5 / 2; (出力:2)</td>
 </tr>
 <tr>
  <td>余（割り算の余り）</td>
  <td>%</td>
  <td>5 % 2 (出力:1)</td>
 </tr>
 <tr>
  <td>べき乗</td>
  <td>Math.Pow()</td>
  <td>Math.Pow(3, 2) (出力:9)</td>
 </tr>
 <tr>
  <td rowspan="2">整数操作</td>
  <td>インクリメント</td>
  <td>++</td>
  <td>num++</td>
 </tr>
 <tr>
  <td>デクリメント</td>
  <td>--</td>
  <td>num--</td>
 </tr>
 <tr>
  <td rowspan="5">文字列操作</td>
  <td>結合</td>
  <td>+</td>
  <td>str1 + str2;</td>
 </tr>
 <tr>
  <td>長さ</td>
  <td>文字列.Length</td>
  <td>str1.Length</td>
 </tr>
 <tr>
  <td>切り出し</td>
  <td>文字列.Substring</td>
  <td>"あいうえお".Substring(1,3);<br>(出力:"いうえ")</td>
 </tr>
 <tr>
  <td>検索</td>
  <td>文字列.IndexOf</td>
  <td>"あいうえお".IndexOf("い"); <br>(出力:1)</td>
 </tr>
 <tr>
  <td>配列に分割</td>
  <td>文字列.Split</td>
  <td>"10,2,3".Split(",");</td>
 </tr>
 <tr>
  <td rowspan="2">制御構文（選択）</td>
  <td>IF文</td>
  <td>if (条件) {処理} else if {処理} else {処理}</td>
  <td>if(a == 0)<br>{<br>&nbsp処理<br>}<br>else if (a == 1)<br>{<br>&nbsp処理<br>}<br>else<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>Switch文/Case文</td>
  <td>switch(変数)<br>{<br>&nbspcase 値1:<br>&nbsp&nbsp処理<br>&nbsp&nbspbreak;<br>&nbspcase 値2:<br>&nbsp&nbsp処理<br>&nbsp&nbspbreak;<br>&nbspdefault:<br>&nbsp&nbsp処理<br>&nbsp&nbspbreak;<br>}</td>
  <td>switch(num)<br>{<br>&nbspcase 1:<br>&nbsp&nbspConsole.WriteLine(num);<br>&nbsp&nbspbreak;<br>&nbspcase 10:<br>&nbsp&nbspConsole.WriteLine(num);<br>&nbsp&nbspbreak;<br>&nbspdefault:<br>&nbsp&nbspConsole.WriteLine(num);<br>&nbsp&nbspbreak;<br>}</td>
 </tr>
 <tr>
  <td rowspan="6">制御構文（ループ）</td>
  <td>カウント制御ループ（For）</td>
  <td>for(int i = 0; i < 10; i++) {処理}</td>
  <td>for(int i = 0; i < 10; i++)<br>{<br>&nbspConsole.WriteLine(i);<br>}</td>
 </tr>
 <tr>
  <td>条件制御ループ(while)</td>
  <td>while(条件式) {処理}</td>
  <td>var num = 0;<br>while(num < 0)<br>{<br>&nbspnum++;<br>}</td>
 </tr>
 <tr>
  <td>コレクション制御ループ(each)</td>
  <td>foreach(変数宣言 in 配列名){処理}</td>
  <td>var strArray[] = {"a","b","c"};<br>foreach(string str in strArray)<br>{<br>&nbspConsole.WriteLine(str);<br>}</td>
 </tr>
 <tr>
  <td>ループスキップ(continue/skip)</td>
  <td>continue</td>
  <td>for(int i = 0; i < 10; i++)<br>{<br>&nbspif(i % 2 == 0){<br>&nbsp&nbspcontinue;<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td>ループ再実行</td>
  <td>ない</td>
  <td></td>
 </tr>
 <tr>
  <td>ループからの早期脱出（break)</td>
  <td>break</td>
  <td>for(int i = 0; i < 10; i++)<br>{<br>&nbspif(i % 2 == 0){<br>&nbsp&nbspbreak;<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">例外処理</td>
  <td>try catch</td>
  <td>try{処理}catch(exception){処理}</td>
  <td>try<br>{<br>&nbsp処理<br>}<br>catch(Exception)<br>{<br>&nbspConsole.WriteLine("Error");<br>}</td>
 </tr>
 <tr>
  <td>finally</td>
  <td>try{処理}catch(exception){処理}finally{処理}</td>
  <td>try<br>{<br>&nbsp処理<br>}<br>catch(Exception)<br>{<br>&nbspConsole.WriteLine("Error");<br>}<br>finally<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>usingブロック/try-with-resources</td>
  <td>using(idsposable変数のインスタンス化){処理}</td>
  <td>using (FileStream fs = new FileStream("test.txt", File.Mode.Read))<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td rowspan="2">関数（メソッド）宣言</td>
  <td>戻り値あり</td>
  <td>戻り値データ型 関数名(データ型 引数名){return xxx;}</td>
  <td>int Add(int a, int b)<br>{<br>&nbspreturn a + b;<br>}</td>
 </tr>
 <tr>
  <td>戻り値なし</td>
  <td>void 関数名(データ型 引数名){処理}</td>
  <td>void ShowMessage(String Message)<br>{<br>&nbspConsole.WriteLine(Message);<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">クラス</td>
  <td>宣言</td>
  <td>class クラス名{}</td>
  <td>class human<br>{<br>&nbspprivate String name;<br>public void SetName(String inputName)<br>&nbsp&nbsp{<br>&nbsp&nbsp&nbspname = inputName;<br>&nbsp&nbsp}<br>&nbsp}</td>
 </tr>
 <tr>
  <td>継承</td>
  <td>class 派生クラス名 : 基底クラス名{ 派生クラスの定義 }</td>
  <td>class Adult : human<br>{<br>&nbspprivate int Age;<br>}</td>
 </tr>
 <tr>
  <td>初期化（インスタンス化）</td>
  <td>class クラス名1{アクセス修飾子 クラス名1{処理}}</td>
  <td>class Person<br>{<br>&nbsppublic Person(string n, int a)<br>&nbsp{<br>&nbsp&nbspname = n;<br>&nbsp&nbspage = a;<br>&nbsp}<br>}<br><br>Person personInstance = new Person("Alice", 30);</td>
 </tr>
 <tr>
  <td rowspan="5">コードブロック</td>
  <td>クラスブロック</td>
  <td>中括弧</td>
  <td>class hoge<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>関数ブロック</td>
  <td>中括弧</td>
  <td>void hoge()<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>IFブロック</td>
  <td>中括弧</td>
  <td>if ( a == 0)<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>ループブロック</td>
  <td>中括弧</td>
  <td>for(int i = 0; i < 10; i++)<br>{<br>&nbsp処理<br>}</td>
 </tr>
 <tr>
  <td>例外処理ブロック</td>
  <td>中括弧</td>
  <td>try<br>{<br>&nbsp処理<br>}<br>catch(Exception)<br>{<br>&nbspConsole.WriteLine("Error");<br>}</td>
 </tr>
 <tr>
  <td rowspan="2">ライブラリ/モジュール関連</td>
  <td>ライブラリ/モジュールの追加</td>
  <td>VisualStudioのソリューションエクスプローラーで、[参照]⇒[参照の追加]⇒モジュールを指定する。<br>実体は、csprojファイルのItemGroup>Referenceノード内に追加。<br>または<br>CLIでdotnet add package パッケージ名</td>
  <td></td>
 </tr>
 <tr>
  <td>名前空間（パッケージ）の参照追加</td>
  <td>ファイル先頭で、<br>using 名前空間;</td>
  <td>using System.Text;</td>
 </tr>
</table>
