## Python3基本文法チートシート
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
  <td>行の先頭に#(シャープ)</td>
  <td># 行末までコメント</td>
 </tr>
 <tr>
  <td>複数行コメント</td>
  <td>三連引用符で囲う(''',""")</td>
  <td>"""<br>これは<br>コメントです<br>"""<br>または<br>'''<br>これは<br>コメントです<br>'''</td>
 </tr>
 <tr>
  <td rowspan="2">コンソール出力</td>
  <td>改行あり</td>
  <td>print(出力文字)</td>
  <td>print("Hello World")</td>
 </tr>
 <tr>
  <td>改行無し</td>
  <td>print(出力文字, end='')</td>
  <td>print("Hello World", end='')</td>
 </tr>
 <tr>
  <td rowspan="5">データ型</td>
  <td>文字列(String)</td>
  <td>動的型付け</td>
  <td>str = "hoge"</td>
 </tr>
 <tr>
  <td>整数(Int)</td>
  <td>動的型付け</td>
  <td>num = 10</td>
 </tr>
 <tr>
  <td>小数(float)</td>
  <td>動的型付け</td>
  <td>tax = 10.8</td>
 </tr>
 <tr>
  <td>論理(bool)</td>
  <td>動的型付け</td>
  <td>flag = true</td>
 </tr>
 <tr>
  <td>日付(date)</td>
  <td>datetimeモジュール使用</td>
  <td>today_date = datetime.now()</td>
 </tr>
 <tr>
  <td rowspan="5">変数</td>
  <td>定数宣言（変更不可）</td>
  <td>dataclassモジュール使用</td>
  <td>@dataclass(frozen=True)<br>class Constants:<br>&nbspMY_CONSTANT: int<br>&nbspANOTHER_CONSTANT: str<br><br>constants = Constants(42, "Hello, World")</td>
 </tr>
 <tr>
  <td>変数宣言（変更可）</td>
  <td>動的型付け</td>
  <td>x = 5<br>mes = "hello world"<br>pi = 3.14<br>is_true = True</td>
 </tr>
 <tr>
  <td>変数宣言（型推論）</td>
  <td>動的型付け</td>
  <td>x = 5<br>mes = "hello world"<br>pi = 3.14<br>is_true = True</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名 = 値</td>
  <td>x = 0</td>
 </tr>
 <tr>
  <td>キャスト（型変換）</td>
  <td>型名(変数名)</td>
  <td>str_number = "123"<br>int_number = int(str_number)</td>
 </tr>
 <tr>
  <td rowspan="5">配列</td>
  <td>宣言</td>
  <td>変数名 = []<br>※動的な配列。要素数の指定不要。</td>
  <td>empty_list = []</td>
 </tr>
 <tr>
  <td>初期化</td>
  <td>変数名 = []</td>
  <td>mixed_list = [1, "two", 3.0, True, "five"]<br>range_list = list(range(1,6))</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[配列番号] = 値</td>
  <td>my_list[2] = 10</td>
 </tr>
 <tr>
  <td>サイズ変更</td>
  <td>動的な配列</td>
  <td></td>
 </tr>
 <tr>
  <td>値コピー</td>
  <td>浅いコピー：<br>copy()メソッドやcopyモジュールのcopy関数<br>深いコピー：<br>copyモジュールのdeepcopy関数</td>
  <td>original_list = [1, 2, 3]<br>shallow_copied_list = original_list.copy()<br>deep_copied_list = copy.deepcopy(original_list)</td>
 </tr>
 <tr>
  <td rowspan="3">リスト</td>
  <td>宣言</td>
  <td>変数名 = []</td>
  <td>empty_list = []</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[要素番号] = 値</td>
  <td>my_list[2] = 10</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>変数名.append(値)</td>
  <td>my_list.append(6)</td>
 </tr>
 <tr>
  <td rowspan="3">連想配列（ディクショナリ）</td>
  <td>宣言</td>
  <td>変数名 = {} または<br>変数名 = {キー名:　値}</td>
  <td>fruit_dict = {'apple': 3, 'banana': 5, 'cherry': 2}</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名[キー名] = 値</td>
  <td>fruit_dict['apple'] = 4</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>変数名[新キー名] = 値</td>
  <td>fruit_dict['date'] = 7</td>
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
  <td>/<br>ただし割り切れない場合は、近似値で出力<br></td>
  <td>10 / 3 (出力:3.3333333333333335)</td>
 </tr>
 <tr>
  <td>商（割り算の商）</td>
  <td>/</td>
  <td>5 / 2 (出力:2)</td>
 </tr>
 <tr>
  <td>余（割り算の余り）</td>
  <td>%</td>
  <td>5 % 2 (出力:1)</td>
 </tr>
 <tr>
  <td>べき乗</td>
  <td>**</td>
  <td>2 ** 3 (出力:8)</td>
 </tr>
 <tr>
  <td rowspan="2">整数操作</td>
  <td>インクリメント</td>
  <td>変数名 += 増加数</td>
  <td>num += 1</td>
 </tr>
 <tr>
  <td>デクリメント</td>
  <td>変数名 -= 減少数</td>
  <td>num -= 1</td>
 </tr>
 <tr>
  <td rowspan="5">文字列操作</td>
  <td>結合</td>
  <td>+</td>
  <td>str1 + str2;</td>
 </tr>
 <tr>
  <td>長さ</td>
  <td>len(変数名)</td>
  <td>len(my_string)</td>
 </tr>
 <tr>
  <td>切り出し</td>
  <td>変数名[開始位置:終了位置]</td>
  <td>substring = my_string[7:12]</td>
 </tr>
 <tr>
  <td>検索</td>
  <td>find()メソッド, index()メソッド, inキーワード</td>
  <td>my_string = "Hello, World"<br>print(my_string.find("World")) 出力:7<br>print(my_string.index("World")) 出力:7<br>print("World" in my_string) 出力:True</td>
 </tr>
 <tr>
  <td>配列に分割</td>
  <td>文字列.split(区切り文字)</td>
  <td>"10,2,3".split(",")</td>
 </tr>
 <tr>
  <td rowspan="2">制御構文（選択）</td>
  <td>IF文</td>
  <td>if 条件式:<br>&nbsp処理<br>elif 別の条件式:<br>&nbsp処理<br>else:<br>&nbsp処理</td>
  <td>if x > 0:<br>&nbspprint("xは正の数です")<br>elif x == 0:<br>&nbspprint("xはゼロです")<br>else:<br>&nbspprint("xは負の数です")</td>
 </tr>
 <tr>
  <td>Switch文/Case文</td>
  <td>※python 3.10以降<br>match 変数名:<br>&nbspcase 値1:<br>&nbsp&nbsp処理<br>&nbspcase 値2:<br>&nbsp&nbsp処理<br>&nbspcase _:<br>&nbsp&nbsp処理</td>
  <td>match x:<br>&nbspcase 1:<br>&nbsp&nbspprint("xは1です")<br>&nbspcase 2:<br>&nbsp&nbspprint("xは2です")<br>&nbspcase _:<br>&nbsp&nbspprint("xは1でも2でもないです")</td>
 </tr>
 <tr>
  <td rowspan="6">制御構文（ループ）</td>
  <td>カウント制御ループ（For）</td>
  <td>for 変数名 in 反復可能なオブジェクト: <br>&nbsp処理</td>
  <td>for i in range(5):<br>&nbspprint(i)</td>
 </tr>
 <tr>
  <td>条件制御ループ(while)</td>
  <td>while 条件式:<br>&nbsp処理</td>
  <td>count = 0<br>while count < 5:<br>&nbspprint(count)<br>&nbspcount += 1</td>
 </tr>
 <tr>
  <td>コレクション制御ループ(each)</td>
  <td>for 要素 in コレクション:<br>&nbsp処理</td>
  <td>my_list = [1,2,3,4,5]<br>for number in my_list:<br>&nbspprint(number)</td>
 </tr>
 <tr>
  <td>ループスキップ(continue/skip)</td>
  <td>continue</td>
  <td>for 要素 in イテラブル:<br>&nbspif 条件:<br>&nbsp&nbspcontinue<br>&nbsp処理</td>
 </tr>
 <tr>
  <td>ループ再実行</td>
  <td>ない ※外部モジュール使用</td>
  <td></td>
 </tr>
 <tr>
  <td>ループからの早期脱出（break)</td>
  <td>break</td>
  <td>for i in range(10):<br>&nbspif i == 5:<br>&nbsp&nbspprint("iが5になったのでループを終了")<br>&nbsp&nbspbreak<br>&nbspprint(i)</td>
 </tr>
 <tr>
  <td rowspan="3">例外処理</td>
  <td>try catch</td>
  <td>try:<br>&nbsp処理<br>except 例外の種類 as 変数:<br>&nbsp処理</td>
  <td>try:<br>&nbsp#ゼロで除算はできない<br>&nbspx = 10 / 0<br>except ZeroDivisionError as e:<br>&nbspprint(f"エラーが発生しました: {e}")</td>
 </tr>
 <tr>
  <td>finally</td>
  <td>try:<br>&nbsp処理<br>except 例外の種類 as 変数:<br>&nbsp処理<br>finally:<br>&nbsp最終的な処理</td>
  <td>try:<br>&nbspx = 10 / 0<br>except ZeroDivisionError as e:<br>&nbspprint(f"エラーが発生しました: {e}")<br>finally:<br>&nbspx = 0</td>
 </tr>
 <tr>
  <td>usingブロック/try-with-resources</td>
  <td>with コンテキストマネージャ as 変数:<br>&nbsp処理<br></td>
  <td>with open('example.txt', 'r') as file:<br>&nbspcontent = file.read()<br>&nbspprint(content)</td>
 </tr>
 <tr>
  <td rowspan="2">関数（メソッド）宣言</td>
  <td>戻り値あり</td>
  <td>def 関数名(引数名):<br>&nbsp処理<br>&nbspreturn 変数名</td>
  <td>def add_numbers(x, y):<br>&nbspresult = x + y<br>&nbspreturn result</td>
 </tr>
 <tr>
  <td>戻り値なし</td>
  <td>def 関数名(引数名):<br>&nbsp処理</td>
  <td>def greet(name):<br>&nbspprint(f"Hello, {name}")</td>
 </tr>
 <tr>
  <td rowspan="3">クラス</td>
  <td>宣言</td>
  <td>class クラス名:</td>
  <td>class MyClass:<br>&nbsp処理</td>
 </tr>
 <tr>
  <td>継承</td>
  <td>class 基底クラス名:<br>&nbsp処理<br>class 派生クラス名(基底クラス名):<br>&nbsp処理</td>
  <td>class ParentClass:<br>&nbspdef __init__(self, parent_param):<br>&nbsp&nbspself.parent_param = parent_param<br>&nbspdef parent_method(self):<br>&nbsp&nbspprint(f"Parent Method: {self.parent_param}")<br><br>class ChildClass(ParentClass):<br>&nbspdef __init__(self, parent_param, child_param):<br>&nbsp&nbspsuper().__init__(parent_param)<br>&nbsp&nbspself.child_param = child_param<br>&nbspdef child_method(self):<br>&nbsp&nbspprint(f"Child Method: {self.child_param}")</td>
 </tr>
 <tr>
  <td>初期化（インスタンス化）</td>
  <td>class クラス名:<br>&nbspdef __init__(self, 引数名):<br>&nbsp&nbsp処理</td>
  <td>class Person:<br>&nbspdef __init__(self, name, age):<br>&nbsp&nbspself.name = name<br>&nbsp&nbspself.age = age<br><br>person_instance = Person("Alice", 30)</td>
 </tr>
 <tr>
  <td rowspan="5">コードブロック</td>
  <td>クラスブロック</td>
  <td>インデント</td>
  <td>class hoge:<br>&nbspdef __init__(self, param1):<br>&nbsp&nbspself.param1 = param1</td>
 </tr>
 <tr>
  <td>関数ブロック</td>
  <td>インデント</td>
  <td>def hoge():<br>&nbspprint("hello")</td>
 </tr>
 <tr>
  <td>IFブロック</td>
  <td>インデント</td>
  <td>if x > 0:<br>&nbspprint("xは正の数です")</td>
 </tr>
 <tr>
  <td>ループブロック</td>
  <td>インデント</td>
  <td>while count < 5:<br>&nbspprint(f"Count: {count}")<br>&nbspcount += 1</td>
 </tr>
 <tr>
  <td>例外処理ブロック</td>
  <td>インデント</td>
  <td>try:<br>&nbspx = 10 / 0<br>except ZeroDivisionError:<br>&nbspprint("ゼロで割ることはできません
  ")<br>except Exception as e:<br>&nbspprint(f"エラー: {e}")<br>finally:<br>&nbspprint("最終処理")</td>
 </tr>
 <tr>
  <td rowspan="2">ライブラリ/モジュール関連</td>
  <td>ライブラリ/モジュールの追加</td>
  <td>pip(Pythonパッケージインストーラー)の使用<br>$ pip install ライブラリ名</td>
  <td>pip install requests</td>
 </tr>
 <tr>
  <td>名前空間（パッケージ）の参照追加</td>
  <td>from パッケージ名 import モジュール名 as 別名</td>
  <td>from mypackage import module1 as m1</td>
 </tr>
</table>

