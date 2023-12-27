## Ruby基本文法チートシート
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
  <td>=begin で始まり<br>=endで終わる</td>
  <td>=begin<br>これは<br>コメントです</br>=end</td>
 </tr>
 <tr>
  <td rowspan="2">コンソール出力</td>
  <td>改行あり</td>
  <td>puts</td>
  <td>puts "Hellom World"</td>
 </tr>
 <tr>
  <td>改行無し</td>
  <td>print</td>
  <td>print "Hello, World"</td>
 </tr>
 <tr>
  <td rowspan="5">データ型</td>
  <td>文字列(String)</td>
  <td>動的型付け</td>
  <td>str = "Hello, World"</td>
 </tr>
 <tr>
  <td>整数(Int)</td>
  <td>動的型付け</td>
  <td>num = 42</td>
 </tr>
 <tr>
  <td>小数(float)</td>
  <td>動的型付け</td>
  <td>fload_num = 3.14</td>
 </tr>
 <tr>
  <td>論理(bool)</td>
  <td>動的型付け</td>
  <td>is_true = true</td>
 </tr>
 <tr>
  <td>日付(date)</td>
  <td>Dateクラス</td>
  <td>current_date = Date.today</td>
 </tr>
 <tr>
  <td rowspan="5">変数</td>
  <td>定数宣言（変更不可）</td>
  <td>大文字の変数名</td>
  <td>MY_CONSTANT = 42</td>
 </tr>
 <tr>
  <td>変数宣言（変更可）</td>
  <td>小文字の変数名</td>
  <td>my_variable = "Hello"</td>
 </tr>
 <tr>
  <td>変数宣言（型推論）</td>
  <td>動的型付け</td>
  <td>my_variable = "Hello"<br>my_variable = 123</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名 = 値</td>
  <td>my_string = "hello, ruby"<br>my_integer = 42</td>
 </tr>
 <tr>
  <td>キャスト（型変換）</td>
  <td>整数への型変換:to_i<br>浮動小数点数への型変換:to_f<br>文字列への型変換:to_s</td>
  <td>#整数への型変換<br>float_number = 3.14<br>integer_number = float_number.to_i<br>puts integer_number (出力:3)</td>
 </tr>
 <tr>
  <td rowspan="5">配列</td>
  <td>宣言</td>
  <td>変数名 = 要素</td>
  <td>empty_array = []<br>new_array = Array.new(3)</td>
 </tr>
 <tr>
  <td>初期化</td>
  <td>変数名 = 要素</td>
  <td>fruits = ["apple","banana","orange"]<br>numbers = Array.new(3, 0) #[0,0,0]<br>colors = %w(red green blue)</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[配列番号] = 値</td>
  <td>fruits[1] = "grape"<br>#2〜4番目の要素に代入<br>numbers[1..3] = [10, 20, 30]</td>
 </tr>
 <tr>
  <td>サイズ変更</td>
  <td>末尾に追加:push(), <<演算子<br>先頭に追加:unshiftメソッド<br>末尾の削除:popメソッド<br>先頭の削除:shiftメソッド</td>
  <td>fruits = ["apple", "banana", "orange"]<br>fruits.push("kiwi")<br>fruits << "kiwi"<br>fruits.unshift("apple")<br>fruits.pop<br>fruits.shift</td>
 </tr>
 <tr>
  <td>値コピー</td>
  <td>浅いコピー:変数をそのまま代入<br>深いコピー:dupメソッド</td>
  <td>fruits = ["apple", "banana", "orange"]<br>copied_array = fruits<br>new_copied_array = fruits.dup</td>
 </tr>
 <tr>
  <td rowspan="3">リスト</td>
  <td>宣言</td>
  <td>変数名 = 要素</td>
  <td>empty_array = []<br>new_array = Array.new(3)</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[配列番号] = 値</td>
  <td>fruits[1] = "grape"<br>#2〜4番目の要素に代入<br>numbers[1..3] = [10, 20, 30]</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>末尾に追加:push(), <<演算子<br>先頭に追加:unshiftメソッド</td>
  <td>fruits = ["apple", "banana", "orange"]<br>fruits.push("kiwi")<br>fruits << "kiwi"<br>fruits.unshift("apple")</td>
 </tr>
 <tr>
  <td rowspan="3">連想配列（ディクショナリ）</td>
  <td>宣言</td>
  <td>変数名 = {キー名: 値}<br>変数名 = {文字列キー名 => 値}</td>
  <td>person = {name: "John", age: 30, city: "Tokyo"}<br>person = {"name" => "John", "age" => 25, "city" => "New York"}</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[:キー名] = 値<br>変数名[文字列キー名] = 値</td>
  <td>person[:age] = 31<br>person["city"] = "America"</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>merge! メソッド</td>
  <td>person.merge!({hoby: "pc"})<br>person.merge!({"hoby": "pc"})</td>
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
  <td>/</td>
  <td>10 / 3</td>
 </tr>
 <tr>
  <td>商（割り算の商）</td>
  <td>/</td>
  <td>10 / 3 (出力:3)</td>
 </tr>
 <tr>
  <td>余（割り算の余り）</td>
  <td>%</td>
  <td>5 % 2 (出力:1)</td>
 </tr>
 <tr>
  <td>べき乗</td>
  <td>**</td>
  <td>3 ** 2 (出力:9)</td>
 </tr>
 <tr>
  <td rowspan="2">整数操作</td>
  <td>インクリメント</td>
  <td>+=</td>
  <td>num += 1</td>
 </tr>
 <tr>
  <td>デクリメント</td>
  <td>-=</td>
  <td>num -= 1</td>
 </tr>
 <tr>
  <td rowspan="5">文字列操作</td>
  <td>結合</td>
  <td>文字列1 + 文字列2<br>文字列1.concat(文字列2)<br>文字列1 << 文字列2</td>
  <td>result = str1 + str2<br>str1.concat(str2)<br>str1 << str2</td>
 </tr>
 <tr>
  <td>長さ</td>
  <td>文字列.length<br>文字列.size</td>
  <td>str1.length<br>str1.size</td>
 </tr>
 <tr>
  <td>切り出し</td>
  <td>文字列.slice(開始位置, 文字数)<br>範囲演算子</td>
  <td>text = "Hello, World"<br>substring = text.slice(7, 5)<br>puts substring (出力:World)<br>substring = text[0..4]<br>puts substring (出力:Hello)</td>
 </tr>
 <tr>
  <td>検索</td>
  <td>文字列.include?(検索文字列) #戻り値:bool<br>文字列.index(検索文字列) #戻り:index</td>
  <td>text = "Hello, World"<br>result = text.include?("World")<br>puts result (出力:true)<br>result = text.index("World")<br>puts result (出力:7)</td>
 </tr>
 <tr>
  <td>配列に分割</td>
  <td>文字列.split(分割文字)</td>
  <td>"10,2,3".split(",");</td>
 </tr>
 <tr>
  <td rowspan="2">制御構文（選択）</td>
  <td>IF文</td>
  <td>if 条件<br>&nbsp処理<br>elsif<br>&nbsp処理<br>else<br>&nbsp処理<br>end</td>
  <td>x = 5<br>if x > 0<br>&nbspputs "xは正の数"<br>elsif x == 0<br>&nbspputs "xはゼロ"<br>else<br>&nbspputs "xは負の数"<br>end</td>
 </tr>
 <tr>
  <td>Switch文/Case文</td>
  <td>case 式<br>when 値1<br>&nbsp処理<br>when 値2, 値3<br>&nbsp処理</td>
  <td>day = "Sunday"<br>case day<br>when "Monday"<br>&nbspputs "It's Monday."<br>when "Tuesday", "Sunday"<br>&nbspputs "It's Tuesday or Sunday"</td>
 </tr>
 <tr>
  <td rowspan="6">制御構文（ループ）</td>
  <td>カウント制御ループ（For）</td>
  <td>for 変数 in イテレータ<br>&nbsp処理<br>end</td>
  <td>fruit in fruits<br>&nbspputs fruit<br>end</td>
 </tr>
 <tr>
  <td>条件制御ループ(while)</td>
  <td>while 条件 do<br>&nbsp処理<br>end<br>※doは省略可</td>
  <td>while i <= 5<br>&nbspputs i<br>&nbspi += 1<br>end</td>
 </tr>
 <tr>
  <td>コレクション制御ループ(each)</td>
  <td>イテレータ.each do |変数|<br>&nbsp処理<br>end</td>
  <td>fruits.each do |fruit|<br>&nbspputs fruit<br>end</td>
 </tr>
 <tr>
  <td>ループスキップ(continue/skip)</td>
  <td>next 条件<br>※条件は省略可</td>
  <td>(1..5).each do |num|<br>&nbspputs "Processing #{num}"<br>&nbspnext<br>&nbspputs "This line won't be reached"<br>end<br>または<br>(1..10).each do |num|<br>#偶数の場合にスキップ<br>&nbspnext if num.even?<br>&nbspputs num<br>end</td>
 </tr>
 <tr>
  <td>ループ再実行</td>
  <td>redo 条件<br>※条件は省略可, 無限ループに注意</td>
  <td>while count < 3<br>&nbspputs "Count: #{count}"<br>&nbspcount += 1<br>#countが2の場合、ループを再実行する<br>&nbspredo if count == 2<br>end</td>
 </tr>
 <tr>
  <td>ループからの早期脱出（break)</td>
  <td>break 条件<br>※条件は省略可</td>
  <td>(1..5).each do |num|<br>&nbspputs num<br>&nbspbreak if num == 3<br>end</td>
 </tr>
 <tr>
  <td rowspan="3">例外処理</td>
  <td>try catch</td>
  <td>try{処理}catch(exception){処理}</td>
  <td>try<br>{<br>&nbsp処理<br>}<br>catch(Exception)<br>{<br>&nbspConsole.WriteLine("Error");<br>}</td>
 </tr>
 <tr>
  <td>finally</td>
  <td>begin<br>&nbsp処理<br>rescue [例外の型]<br>&nbsp例外処理<br>ensure<br>&nbsp必ず実行される処理<br>end</td>
  <td>begin<br>&nbspresult = 10 / 0<br>rescue ZeroDivisionError => e<br>&nbspputs "エラー: #{e.message}"<br>ensure<br>&nbspputs "ensure節が実行されました"<br>end</td>
 </tr>
 <tr>
  <td>usingブロック/try-with-resources</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td rowspan="2">関数（メソッド）宣言</td>
  <td>戻り値あり</td>
  <td>def 関数名(引数名)<br>&nbsp処理<br>&nbspreturn 変数名<br>end</td>
  <td>def add_numbers(a, b)<br>&nbspresult = a + b<br>&nbspreturn result<br>end</td>
 </tr>
 <tr>
  <td>戻り値なし</td>
  <td>def 関数名(引数名)<br>&nbsp処理<br>end</td>
  <td>def greet(name)<br>&nbspputs "Hello, #{name}"<br>end</td>
 </tr>
 <tr>
  <td rowspan="3">クラス</td>
  <td>宣言</td>
  <td>class クラス名<br>&nbsp#クラスのメンバやメソッドを定義<br>end</td>
  <td>class Dog<br>&nbspdef bark<br>&nbsp&nbspputs "Woof, woof!"<br>end</td>
 </tr>
 <tr>
  <td>継承</td>
  <td>class 子クラス < 親クラス名<br>&nbsp#子クラスのメンバやメソッドを定義<br>end</td>
  <td>class Car<br>&nbspdef accele<br>&nbsp&nbspputs("アクセルを踏みました")<br>&nbspend<br>end<br><br>class FamilyCar < Car<br>&nbspdef openRoof<br>&nbsp&nbspputs("ルーフを開けました")<br>&nbspend<br>end<br><br>sc = SportsCar.new<br>sc.openRoof<br>sc.accele<br>(出力:ルーフを開けました<br>アクセルを踏みました)</td>
 </tr>
 <tr>
  <td>初期化（インスタンス化）</td>
  <td>class クラス名<br>&nbspdef initialize(引数名)<br>&nbsp&nbsp処理<br>&nbspend<br>end</td>
  <td>class Person<br>&nbspdef initialize(name, age)<br>&nbsp&nbsp@name = name<br>&nbsp&nbsp@age = age<br>&nbspend<br>end<br><br>person = Person.new("Alice", 25)</td>
 </tr>
 <tr>
  <td rowspan="5">コードブロック</td>
  <td>クラスブロック</td>
  <td>なし</td>
  <td>class Person def speak puts "hello" end end</td>
 </tr>
 <tr>
  <td>関数ブロック</td>
  <td>なし</td>
  <td>def execute_block puts "Start of the block" end</td>
 </tr>
 <tr>
  <td>IFブロック</td>
  <td>なし</td>
  <td>if a < 0 puts "aは負の数" end</td>
 </tr>
 <tr>
  <td>ループブロック</td>
  <td>なし</td>
  <td>(1..5).each do |n| puts n end</td>
 </tr>
 <tr>
  <td>例外処理ブロック</td>
  <td>なし</td>
  <td>begin 10 / 0 rescure ZeroDivisionError "Error: Division by zero" end</td>
 </tr>
 <tr>
  <td rowspan="2">ライブラリ/モジュール関連</td>
  <td>ライブラリ/モジュールの追加</td>
  <td>RubyGemsの使用<br>$ gem install ライブラリ名</td>
  <td>gem install nokogiri</td>
 </tr>
 <tr>
  <td>名前空間（パッケージ）の参照追加</td>
  <td>ファイル先頭で、<br>require '名前空間'</td>
  <td>require 'nokogiri'</td>
 </tr>
</table>

