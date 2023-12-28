## C基本文法チートシート
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
  <td>/* */ で囲う</td>
  <td>/*<br>&nbspこれは<br>&nbspコメントです<br>*/</td>
 </tr>
 <tr>
  <td rowspan="2">コンソール出力</td>
  <td>改行あり</td>
  <td>printf に"\n"を含める</td>
  <td>printf("Hello, World\n");</td>
 </tr>
 <tr>
  <td>改行無し</td>
  <td>print に"\n"を含めない</td>
  <td>printf("Hello, World");</td>
 </tr>
 <tr>
  <td rowspan="5">データ型</td>
  <td>文字列(String)</td>
  <td>char</td>
  <td>char myString[] = "Hello, World";</td>
 </tr>
 <tr>
  <td>整数(Int)</td>
  <td>int</td>
  <td>int myInteger = 42;</td>
 </tr>
 <tr>
  <td>小数(float)</td>
  <td>float, double</td>
  <td>float myFloat = 3.14;<br>double myDouble = 3.1415926535;</td>
 </tr>
 <tr>
  <td>論理(bool)</td>
  <td>なし</td>
  <td>int myBoolean = 1;</td>
 </tr>
 <tr>
  <td>日付(date)</td>
  <td>time_t</td>
  <td>#include &lttime.h&gt<br>time_t currentTime = time(NULL);</td>
 </tr>
 <tr>
  <td rowspan="5">変数</td>
  <td>定数宣言（変更不可）</td>
  <td>const</td>
  <td>const int myImmutableConstant = 42;</td>
 </tr>
 <tr>
  <td>変数宣言（変更可）</td>
  <td>型 変数名 = 値</td>
  <td>char myChar = 'A';</td>
 </tr>
 <tr>
  <td>変数宣言（型推論）</td>
  <td>auto</td>
  <td>auto myInteger = 42;<br>auto myFloat = 3.14;<br>auto myChar = 'A';</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名 = 値</td>
  <td>int myInteger; //宣言<br>myInteger = 42; //代入</td>
 </tr>
 <tr>
  <td>キャスト（型変換）</td>
  <td>(新しい型)式</td>
  <td>int myInteger = 42;<br>double myDouble;<br>myDouble = (double)myInteger;</td>
 </tr>
 <tr>
  <td rowspan="5">配列</td>
  <td>宣言</td>
  <td>データ型 配列名[要素数]</td>
  <td>int numbers[10];<br>float grades[5];</td>
 </tr>
 <tr>
  <td>初期化</td>
  <td>配列名[配列番号] = 値</td>
  <td>//宣言(要素数指定しない)と初期化<br>int numbers[] = {1, 2, 3, 4, 5};<br>//部分的な初期化(残りは0で初期化)<br>int numbers[8] = {1,2,3,4,5};</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>配列名[配列番号] = 値</td>
  <td>myArray[1] = 10;</td>
 </tr>
 <tr>
  <td>サイズ変更</td>
  <td>動的な配列を作成して行う<br>malloc <- メモリ割当<br>realloc <- サイズ変更<br>free <- メモリ開放</td>
  <td>// 5つの整数分のメモリを割当<br>int *myArray = (int *)malloc(5 * sizeof(int));<br>//サイズを変更<br>int newSize = 10;<br>myArray = (int *)realloc(myArray, newSize * sizeof(int));<br>//メモリを解放<br>free(myArray);</td>
 </tr>
 <tr>
  <td>値コピー</td>
  <td>memcpy(コピー先, コピー元, サイズ)</td>
  <td>int originalArray[] = {1,2,3,4,5};<br>int copiedArray[5];<br>memcpy(copiedArray, originalArray, sizeof(originalArray));</td>
 </tr>
 <tr>
  <td rowspan="3">リスト</td>
  <td>宣言</td>
  <td>ポインタと構造体を組み合わせてリストを模倣する</td>
  <td></td>
 </tr>
 <tr>
  <td>代入</td>
  <td></td>
  <td></td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td></td>
  <td></td>
 </tr>
 <tr>
  <td rowspan="3">連想配列（ディクショナリ）</td>
  <td>宣言</td>
  <td>stdlib.h や string.h を使用して、類似の動作を模倣する</td>
  <td></td>
 </tr>
 <tr>
  <td>代入</td>
  <td></td>
  <td></td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td></td>
  <td></td>
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
  <td>/ ※キャストが必要な場合あり</td>
  <td>fload quotient = (float)a / b;</td>
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
  <td>math.hヘッダに含まれるpow関数</td>
  <td>#include &ltstdio.h><br>#include &ltmath.h><br>int main(){<br>&nbspdouble base = 2.0;<br>&nbspdouble exponent = 3.0;<br>&nbspdouble result = pow(base, exponent);</td>
 </tr>
 <tr>
  <td rowspan="2">整数操作</td>
  <td>インクリメント</td>
  <td>++</td>
  <td>num++;</td>
 </tr>
 <tr>
  <td>デクリメント</td>
  <td>--</td>
  <td>num--;</td>
 </tr>
 <tr>
  <td rowspan="5">文字列操作</td>
  <td>結合</td>
  <td>string.hヘッダのstrcat関数またはstrncat関数<br>※strncat関数は結合する文字数を指定することができ、これによりバッファオーバーフローのリスクを減少させる</td>
  <td>char str1[50] = "Hello, ";<br>char str2[] = "world!";<br>//str1にstr2を最大で(50-strlen(str1)  - 1)文字まで結合する<br>strncat(str1, str2, sizeof(str1) - strlen(str1) - 1);</td>
 </tr>
 <tr>
  <td>長さ</td>
  <td>strlen(文字列)<br>※ヌル終端文字を含める</td>
  <td>size_t length = strlen(str);</td>
 </tr>
 <tr>
  <td>切り出し</td>
  <td>strncpy関数やmemcpy関数などを組み合わせて利用する</td>
  <td>void extractSubString(const char *src, char *dst, int start, int length){<br>&nbspstrncpy(dst, src + start, length);<br>&nbspdst[length] = '\n';<br>}<br>・・・<br>char originalString[] = "Hello, World";<br>char extractedString[20];<br>// 5番目の位置から5文字文の部分文字列を取り出す<br>extractSubString(originalString, extractedString, 5, 5);</td>
 </tr>
 <tr>
  <td>検索</td>
  <td>strstr(文字列, 検索パターン)</td>
  <td>char originalStr[] = "Hello, World";<br>char searchPattern[] = "World";<br>char *result = strstr(originalStr, searchPattern);</td>
 </tr>
 <tr>
  <td>配列に分割</td>
  <td>strtok(文字列, 区切り文字)<br>※区切り文字を'\n'で埋める</td>
  <td>char input[] = "apple,orange,banana";<br>const char delimiter[] = ",";<br>char *token = strtok(input, delimiter);<br>while (token != NULL){<br>&nbspprintf("%s\n, token);<br>&nbsptoken = strtok(NULL, delimiter);<br>}</td>
 </tr>
 <tr>
  <td rowspan="2">制御構文（選択）</td>
  <td>IF文</td>
  <td>if (条件式) {<br>&nbsp//真の処理<br>} else if (別の条件式) {<br>&nbsp//真の処理<br>} else {<br>&nbsp//偽の処理<br>}<br></td>
  <td>if (number > 0) {<br>&nbspprintf("Number is positive.\n");<br>} else if (number == 0) {<br>&nbspprintf("Number is zero.\n");<br>} else { <br>&nbspprintf("Number is nagative.\n");<br>}</td>
 </tr>
 <tr>
  <td>Switch文/Case文</td>
  <td>switch (制御式) {<br>&nbspcase 値1:<br>&nbsp&nbsp処理<br>&nbspcase 値2:<br>&nbsp&nbsp処理<br>&nbspdefault:<br>&nbsp&nbsp偽の処理</td>
  <td>int day = 8;<br>switch (day) {<br>&nbspcase 1:<br>&nbsp&nbspprintf("Monday\n");<br>&nbsp&nbspbreak;<br>&nbspcase 2:<br>&nbsp&nbspprintf("Tuesday\n");<br>&nbsp&nbspbreak;<br>&nbsp・・・省略<br>&nbspdefault:<br>&nbsp&nbspprintf("Invalid day\n");</td>
 </tr>
 <tr>
  <td rowspan="6">制御構文（ループ）</td>
  <td>カウント制御ループ（For）</td>
  <td>for (初期化; 条件式; 更新式) {<br>&nbsp処理<br>}</td>
  <td>for (int i = 0; i <= 10; i++){<br>&nbspprintf("%d\n", i);<br>}</td>
 </tr>
 <tr>
  <td>条件制御ループ(while)</td>
  <td>while (条件式) {<br>&nbsp処理<br>}</td>
  <td>while (i <= 10){<br>&nbspprintf("%d\n", i);<br>&nbspi++;<br>}</td>
 </tr>
 <tr>
  <td>コレクション制御ループ(each)</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td>ループスキップ(continue/skip)</td>
  <td>continue</td>
  <td>for (int i = 1; i <= 5; i++) {<br>&nbspif (i % 2 == 0) {<br>&nbsp&nbspcontinue;<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td>ループ再実行</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td>ループからの早期脱出（break)</td>
  <td>break</td>
  <td>int number;<br>while (1) {<br>&nbspprintf("整数を入力(0で終了): ");<br>&nbspscanf("%d", &number);<br>&nbspif (number == 0) {<br>&nbsp&nbspbreak; //ループから脱出<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">例外処理</td>
  <td>try catch</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td>finally</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td>usingブロック/try-with-resources</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td rowspan="2">関数（メソッド）宣言</td>
  <td>戻り値あり</td>
  <td>戻り値の型 関数名(引数の型1 引数1, 引数の型2 引数2, ...) {<br>&nbsp処理<br>&nbspreturn 戻り値;<br>}</td>
  <td>#include &ltstdio.h><br><br>//関数宣言<br>int doubleValue(int x);<br>int main() {<br>&nbspint number = 5;<br>&nbspint result = doubleValue(number);<br>&nbspprintf("2倍した結果: %d\n", result);<br><br>&nbspreturn 0;<br>}<br><br>//関数定義<br>int doubleValue(int x) {<br>&nbspreturn 2 * x;<br>}</td>
 </tr>
 <tr>
  <td>戻り値なし</td>
  <td>void 関数名(引数の型1 引数1, 引数の型2 引数2, ...) {<br>&nbsp処理<br>}</td>
  <td>void printMessage() { <br>&nbspprintf("Hello, World\n");<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">クラス</td>
  <td>宣言</td>
  <td>構造体(struct)や関数を使用して、クラスのような構造を作成する</td>
  <td>//構造体の宣言<br>struct Point {<br>&nbspint x;<br>&nbspint y;<br>}<br></td>
 </tr>
 <tr>
  <td>継承</td>
  <td>なし(複雑)</td>
  <td></td>
 </tr>
 <tr>
  <td>初期化（インスタンス化）</td>
  <td>構造体(struct)や関数を使用して模倣</td>
  <td>//構造体の宣言<br>struct Point {<br>&nbspint x;<br>&nbspint y;<br>}<br>//メソッド(関数)の宣言<br>void printPoint(struct Point p);<br>int main() {<br>&nbsp//構造体のインスタンス化<br>&nbspstruct Point myPoint = {10, 20};<br>&nbsp//メソッドの呼び出し<br>&nbspprintPoint(myPoint);<br>&nbspreturn 0;<br>}<br>//メソッド(関数)の定義<br>void printPoint(struct Point p) {<br>&nbspprintf("x: %d, y: %d\n", p.x, p.y);<br>}</td>
 </tr>
 <tr>
  <td rowspan="5">コードブロック</td>
  <td>クラスブロック</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td>関数ブロック</td>
  <td>波括弧</td>
  <td>void printMessag() {<br>&nbspprintf("Hello, World!\n");<br>}</td>
 </tr>
 <tr>
  <td>IFブロック</td>
  <td>波括弧</td>
  <td>if (number > 0) {<br>&nbspprintf("Number is positive.\n");<br>} else if (number == 0) {<br>&nbspprintf("Number is zero.\n");<br>} else { <br>&nbspprintf("Number is nagative.\n");<br>}</td>
 </tr>
 <tr>
  <td>ループブロック</td>
  <td>波括弧</td>
  <td>for (int i = 0; i <= 10; i++){<br>&nbspprintf("%d\n", i);<br>}</td>
 </tr>
 <tr>
  <td>例外処理ブロック</td>
  <td>なし</td>
  <td></td>
 </tr>
 <tr>
  <td rowspan="2">ライブラリ/モジュール関連</td>
  <td>ライブラリ/モジュールの追加</td>
  <td>ヘッダーファイルの取得、依存関係管理ツール(CMake, Autotools, Makefile, pkg-config)の使用</td>
  <td></td>
 </tr>
 <tr>
  <td>名前空間（パッケージ）の参照追加</td>
  <td>#include</td>
  <td>#include &ltstdio.h><br>#include "myheader.h"</td>
 </tr>
</table>

