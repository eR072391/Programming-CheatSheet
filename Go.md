## Golang基本文法チートシート

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
  <td>先頭にスラッシュ2つ</td>
  <td>// これは一行コメントです</td>
 </tr>
 <tr>
  <td>複数行コメント</td>
  <td>/* */ で囲む</td>
  <td>/* <br>これは<br>複数行コメントです<br> */</td>
 </tr>
 <tr>
  <td rowspan="2">コンソール出力</td>
  <td>改行あり</td>
  <td>fmtパッケージを使用<br>fmt.Print</td>
  <td>fmt.Print("これは改行なしの出力")</td>
 </tr>
 <tr>
  <td>改行無し</td>
  <td>fmt.Println</td>
  <td>fmt.Println("これは改行ありの出力")</td>
 </tr>
 <tr>
  <td rowspan="5">データ型</td>
  <td>文字列(String)</td>
  <td>var 変数名 string</td>
  <td>var greeting string = "Hello, Golang!"</td>
 </tr>
 <tr>
  <td>整数(Int)</td>
  <td>var 変数名 int</td>
  <td>var num int = 42</td>
 </tr>
 <tr>
  <td>小数(float)</td>
  <td>var 変数名 float<サイズ></td>
  <td>var pi float64 = 3.14</td>
 </tr>
 <tr>
  <td>論理(bool)</td>
  <td>var 変数名 bool</td>
  <td>var isTrue bool = true</td>
 </tr>
 <tr>
  <td>日付(date)</td>
  <td>timeパッケージ使用</td>
  <td>var currentTime time.Time = time.Now()</td>
 </tr>
 <tr>
  <td rowspan="5">変数</td>
  <td>定数宣言（変更不可）</td>
  <td>const 定数名 = 値</td>
  <td>const Pi = 3.14159265359</td>
 </tr>
 <tr>
  <td>変数宣言（変更可）</td>
  <td>varキーワード使用<br>var 変数名 データ型</td>
  <td>var age int //宣言<br>age = 25 //値を代入</td>
 </tr>
 <tr>
  <td>変数宣言（型推論）</td>
  <td>:= を使用</td>
  <td>age := 25 //int型として推論<br>age := "John" //string型として推論</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>変数名 = 値</td>
  <td>var age int = 25<br>country := "USA"</td>
 </tr>
 <tr>
  <td>キャスト（型変換）</td>
  <td>float32(), float64()<br>int()<br>strconv.Itoa()<br>strconv.Atoi()<br>[]byte(), string()</td>
  <td>//整数型から浮動小数点型への変換<br>var a int = 42<br>var b float64 = float64(a)<br>//浮動小数点型から整数型への変換<br>var x float64 = 3.14<br>var y int = int(x)<br>//整数型から文字列型への変換<br>var number int = 42<br>var str string = strconv.Itoa(number)<br>//文字列型からバイトスライスへの変換<br>var str string = "Hello, Go!"<br>var bytes []byte = []byte(str)<br>//バイトスライスから文字列型への変換<br>var bytes []byte = []byte{72, 101, 108, 108, 111}<br>var str string = string(bytes)</td>
 </tr>
 <tr>
  <td rowspan="5">配列</td>
  <td>宣言</td>
  <td>var 配列名 [要素数]要素の型</td>
  <td>var numbers [5]int</td>
 </tr>
 <tr>
  <td>初期化</td>
  <td>var 変数名 = [要素数]型{値}</td>
  <td>var numbers = [5]int{1, 2, 3, 4, 5}<br>// 自動的に要素数を数える<br>var numbers = [...]int{1, 2, 3, 4, 5}<br>// 特定の要素を指定して初期化<br>var numbers = [5]int{2: 10, 4: 20}</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>配列名[配列番号] = 値</td>
  <td>var array1 = [3]int{1, 2, 3}<br><br>array1[0] = 10<br>array1[2] = 30</td>
 </tr>
 <tr>
  <td>サイズ変更</td>
  <td>スライスを使用した配列にappend()を使用して代入する。<br>append(配列名, 値)</td>
  <td>numbers := []int{1, 2, 3, 4, 5}<br>numbers = append(numbers, 6)</td>
 </tr>
 <tr>
  <td>値コピー</td>
  <td>配列名 := 配列名</td>
  <td>originalArray := [3]int{1, 2, 3}<br><br>copiedArray := originalArray</td>
 </tr>
 <tr>
  <td rowspan="3">リスト</td>
  <td>宣言</td>
  <td>リストとしてスライスが利用される</td>
  <td>var myList []int</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>append(配列名, 値)</td>
  <td>myList = append(myList, 1)</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>append(配列名, 値)</td>
  <td>myList = append(myList, 2, 3)<br>// ...演算子を使用して既存スライスを展開<br>myList = append(myList, []int{1, 2, 3}...)</td>
 </tr>
 <tr>
  <td rowspan="3">連想配列（ディクショナリ）</td>
  <td>宣言</td>
  <td>map<br>※makeはデータ構造を初期化するために使用</td>
  <td>// 空のマップを作成<br>myMap := make(map[string]int)<br>// 初期化と同時に値を設定<br>myMap := map[string]int{<br>&nbsp"one": 1,<br>&nbsp"two": 2,<br>&nbsp"three": 3,<br>}</td>
 </tr>
 <tr>
  <td>代入</td>
  <td>連想配列名[キー名] = 値</td>
  <td>myMap := make(map[string]int)<br>myMap["one"] = 1<br>myMap["two"] = 2<br>myMap["three"] = 3</td>
 </tr>
 <tr>
  <td>要素追加</td>
  <td>同上</td>
  <td></td>
 </tr>
 <tr>
  <td rowspan="7">算術演算</td>
  <td>和（足し算）</td>
  <td>+</td>
  <td>5 + 3</td>
 </tr>
 <tr>
  <td>差（引き算）</td>
  <td>-</td>
  <td>5 - 3</td>
 </tr>
 <tr>
  <td>乗（かけ算）</td>
  <td>*</td>
  <td>5 * 3</td>
 </tr>
 <tr>
  <td>除（割り算）</td>
  <td>/</td>
  <td>10 / 2</td>
 </tr>
 <tr>
  <td>商（割り算の商）</td>
  <td>/</td>
  <td>10 / 3</td>
 </tr>
 <tr>
  <td>余（割り算の余り）</td>
  <td>%</td>
  <td>10 % 3</td>
 </tr>
 <tr>
  <td>べき乗</td>
  <td>mathパッケージのpow関数<br>math.Pow(底, 指数)</td>
  <td>base := 2.0<br>exponent := 3.0<br>result := math.Pow(base, exponent)</td>
 </tr>
 <tr>
  <td rowspan="2">整数操作</td>
  <td>インクリメント</td>
  <td>++</td>
  <td>count++</td>
 </tr>
 <tr>
  <td>デクリメント</td>
  <td>--</td>
  <td>count--</td>
 </tr>
 <tr>
  <td rowspan="5">文字列操作</td>
  <td>結合</td>
  <td>+演算子, fmt.Sprintf,<br>strings.Join</td>
  <td>str1 := "Hello"<br>str2 := ", World!"<br>result := str1 + str2<br>result := fmt.Sprintf("%s%s", str1, str2)<br><br>strSlice := []string{"Hello", ", World!"}<br>result := strings.Join(strSlice, "")</td>
 </tr>
 <tr>
  <td>長さ</td>
  <td>len(文字列)</td>
  <td>length := len(str)</td>
 </tr>
 <tr>
  <td>切り出し</td>
  <td>スライスを使用</td>
  <td>// 0から5番目(5番目は含まれない)<br>sliced1 := str[0:5] <br>// 終了インデックスを省略<br>sliced2 := str[7:]</td>
 </tr>
 <tr>
  <td>検索</td>
  <td>stringsパッケージ使用<br>1. 文字列が含まれているか検索->Contains(文字列, 検索文字列)<br>2. 文字列が何番目から始まっているか検索->Index(文字列, 検索文字列)<br>3. 文字列が何番目から始まっているか検索(後ろから)->LastIndex(文字列, 検索文字列)</td>
  <td>str := "Hello, World!"<br>isPresent := strings.Contains(str, "World")<br>index := strings.Index(str, "World")<br>lastIndex := strings.LastIndex(str, "o")</td>
 </tr>
 <tr>
  <td>配列に分割</td>
  <td>stringsパッケージ使用<br>Split(文字列, 区切り文字)</td>
  <td>str := "apple,orange,banana,grape"<br>result := strings.Split(str, ",")</td>
 </tr>
 <tr>
  <td rowspan="2">制御構文（選択）</td>
  <td>IF文</td>
  <td>if 条件式 {<br>} else if 条件式 {<br>} else {<br>}<br>または<br>if 変数の宣言と初期化; 条件 {<br>}</td>
  <td>if x > 5{<br>&nbspfmt.Println("xは5より大きい")<br>} else if x < 5 {<br>&nbspfmt.Println("xは5より小さい")<br>} else {<br>&nbspfmt.Println("xは0")<br>}<br>または<br>if y := 15; y > 10 {<br>&nbspfmt.Println("yは10より大きい")<br>}</td>
 </tr>
 <tr>
  <td>Switch文/Case文</td>
  <td>swich 値 {<br>case 条件式または値:<br>&nbsp処理<br>case 条件式または値:<br>&nbsp処理<br>default:<br>&nbsp偽の処理</td>
  <td>switch day {<br>case "Monday":<br>&nbspfmt.Println("It's Monday!")<br>case "Tuesday":<br>&nbspfmt.Println("It's Tuesday!")<br>・・・省略<br>または<br>switch { <br>case number < 0:<br>&nbspfmt.Println("Negative number")<br>case number == 0:<br>&nbspfmt.Println("Zero")<br>case number > 0:<br>&nbspfmt.Println("Positive number")<br>default:<br>&nbspfmt.Println("Invalid number")</td>
 </tr>
 <tr>
  <td rowspan="6">制御構文（ループ）</td>
  <td>カウント制御ループ（For）</td>
  <td>for 初期化文; 条件式; 後処理文 {<br>}</td>
  <td>for i := 0; i < 5; i++ {<br>&nbspfmt.Println(i)<br>}</td>
 </tr>
 <tr>
  <td>条件制御ループ(while)</td>
  <td>while文はない<br>for文を使用</td>
  <td>for {<br>無限ループ<br>}</td>
 </tr>
 <tr>
  <td>コレクション制御ループ(each)</td>
  <td>for 添字, 値 := コレクション {<br>}</td>
  <td>fruits := []string{"apple", "banana", "cherry"}<br>for index, value := range fruits {<br>&nbspfmt.Printf("Index: %d, Value: %s\n", index, value)<br>}</td>
 </tr>
 <tr>
  <td>ループスキップ(continue/skip)</td>
  <td>continue</td>
  <td>for i := 0; i < 5; i++ {<br>&nbspif i == 2 {<br>&nbsp&nbspcontinue<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td>ループ再実行</td>
  <td>continueとbreakを組み合わせて、特定の条件が満たされた場合にループを再実行を行う</td>
  <td>for {<br>&nbsp// ループ本体<br><br>&nbsp// 特定の条件が満たされた場合、ループを再実行<br>&nbspif someCondition {<br>&nbsp&nbspcontinue<br>&nbsp}<br><br>&nbsp// ループを抜ける条件があればbreakを使う<br>&nbspif anotherCondition {<br>&nbsp&nbspbreak<br>&nbsp}<br><br>&nbsp// ループから抜けずに通常の処理を続ける<br>}</td>
 </tr>
 <tr>
  <td>ループからの早期脱出（break)</td>
  <td>break</td>
  <td>for i := 0; i < 5; i++ {<br>&nbspif i == 3 {<br>&nbsp&nbspbreak<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">例外処理</td>
  <td>try catch</td>
  <td>try-catchブロックはない<br>関数がエラーを返すことで行う<br>Goの慣習で関数がエラーを返す場合、そのエラーは通常2つの戻り値のうちの2番目として返す。呼び出し元でこれを確認する<br>nilはnull値を表す</td>
  <td>func divide(a, b int) (int, error) {<br>&nbspif b == 0 {<br>&nbsp&nbspreturn 0, errors.New("division by zero")<br>&nbsp}<br>&nbspreturn a / b, nil<br>}<br>func main() {<br>&nbspresult, err := divide(10, 2)<br>&nbspif err != nul {<br>&nbsp&nbspfmt.Println("Error:", err)<br>&nbsp} else {<br>&nbsp&nbspfmt.Println("Result:", result)<br>&nbsp}</td>
 </tr>
 <tr>
  <td>finally</td>
  <td>finally文はない<br>defer文を使用して関数が終了する際に実行されるコードを記述する</td>
  <td>func main() {<br>&nbsp// 開始時の処理<br><br>&nbsp// 関数終了時に実行する関数を以下に記述<br>&nbspdefer 関数名()<br><br>&nbsp// 本来の処理<br>}</td>
 </tr>
 <tr>
  <td>usingブロック/try-with-resources</td>
  <td>defer文を使用</td>
  <td>filePath := "example.txt"<br>// ファイルを開く<br>file, err := os.Open(filePath)<br>if err != nil {<br>&nbspfmt.Println("Error:", err)<br>&nbspreturn<br>}<br>// 関数が終了する際に確実にファイルを閉じる<br>defer file.Close()</td>
 </tr>
 <tr>
  <td rowspan="2">関数（メソッド）宣言</td>
  <td>戻り値あり</td>
  <td>func 関数名(パラメータ1 型1, パラメータ2 型2, ...) 戻り値の型 {<br>&nbsp// 関数の本体<br>&nbspretun 戻り値<br>}</td>
  <td>func ad(a, b int) int {<br>&nbspsum := a + b<br>&nbspreturn sum<br>}</td>
 </tr>
 <tr>
  <td>戻り値なし</td>
  <td>func 関数名(パラメータ1 型1, パラメータ2 型2, ...) {<br>&nbsp// 関数の本体<br>}</td>
  <td>func greet(name string) {<br>&nbspfmt.Println("Helo, " + name + "!")<br>}</td>
 </tr>
 <tr>
  <td rowspan="3">クラス</td>
  <td>宣言</td>
  <td>Go言語はOOPをサポートしているが、classというのはない<br>構造体(struct)とメソッドを使用してOOPの考え方を実現する</td>
  <td>// Person 構造体の定義<br>type Person struct {<br>&nbspFirst Name string<br>&nbspAge int<br>}<br>// NewPersonコンストラクタ関数<br>func NewPerson(firstName string, age int) *Person {<br>&nbspreturn &Person{<br>&nbsp&nbspFirstName: firstName,<br>&nbsp&nbspAge: age,<br>&nbsp}<br>}<br>// GetNameメソッド<br>func (p *Person) GetName() string {<br>&nbspreturn p.FirstName + " " + p.LastName<br>}<br><br>func main() {<br>&nbsp// Personオブジェクトの生成と初期化<br>person := NewPerson("John", 30)<br>&nbsp// メソッドの呼び出し<br>&nbspfmt.Println("Name:", person.GetName())<br>}</td>
 </tr>
 <tr>
  <td>継承</td>
  <td>構造体(struct)とインターフェース(interface)を使用して表す</td>
  <td></td>
 </tr>
 <tr>
  <td>初期化（インスタンス化）</td>
  <td>構造体(struct)を使用</td>
  <td>// Person構造体<br>type Person struct {<br>&nbspFirstName string<br>&nbspLastName string<br>&nbspAge int<br>}<br>func main() {<br>// フィールドごとに初期化<br>&nbspperson := Person{<br>&nbsp&nbspFirstName: "John",<br>&nbsp&nbspLastName: "Doe",<br>&nbsp&nbspAge: 30,<br>&nbsp}<br>}</td>
 </tr>
 <tr>
  <td rowspan="5">コードブロック</td>
  <td>クラスブロック</td>
  <td>波括弧</td>
  <td>// Person 構造体の定義<br>type Person struct {<br>&nbspFirst Name string<br>&nbspAge int<br>}<br>// NewPersonコンストラクタ関数<br>func NewPerson(firstName string, age int) *Person {<br>&nbspreturn &Person{<br>&nbsp&nbspFirstName: firstName,<br>&nbsp&nbspAge: age,<br>&nbsp}<br>}<br>// GetNameメソッド<br>func (p *Person) GetName() string {<br>&nbspreturn p.FirstName + " " + p.LastName<br>}<br><br>func main() {<br>&nbsp// Personオブジェクトの生成と初期化<br>person := NewPerson("John", 30)<br>&nbsp// メソッドの呼び出し<br>&nbspfmt.Println("Name:", person.GetName())<br>}</td>
 </tr>
 <tr>
  <td>関数ブロック</td>
  <td>波括弧</td>
  <td>func add(a, b int) int {<br>}</td>
 </tr>
 <tr>
  <td>IFブロック</td>
  <td>波括弧</td>
  <td>if x > 5{<br>&nbspfmt.Println("xは5より大きい")<br>} else if x < 5 {<br>&nbspfmt.Println("xは5より小さい")<br>} else {<br>&nbspfmt.Println("xは0")<br>}<br>または<br>if y := 15; y > 10 {<br>&nbspfmt.Println("yは10より大きい")<br>}</td>
 </tr>
 <tr>
  <td>ループブロック</td>
  <td>波括弧</td>
  <td>for i := 0; i < 5; i++ {<br>&nbspfmt.Println(i)<br>}</td>
 </tr>
 <tr>
  <td>例外処理ブロック</td>
  <td>波括弧</td>
  <td>func divide(a, b int) (int, error) {<br>&nbspif b == 0 {<br>&nbsp&nbspreturn 0, errors.New("division by zero")<br>&nbsp}<br>&nbspreturn a / b, nil<br>}<br>func main() {<br>&nbspresult, err := divide(10, 2)<br>&nbspif err != nul {<br>&nbsp&nbspfmt.Println("Error:", err)<br>&nbsp} else {<br>&nbsp&nbspfmt.Println("Result:", result)<br>&nbsp}</td>
 </tr>
 <tr>
  <td rowspan="2">ライブラリ/モジュール関連</td>
  <td>ライブラリ/モジュールの追加</td>
  <td>「go mod init モジュール名」<br>Go Modulesを利用するために、プロジェクトのディレクトリ内で実行する<br>「go get パッケージのパス」<br>パッケージやモジュールをダウンロードし、ビルドしてインストールする<br>「go install パッケージのパス」<br>パッケージをビルドし、実行可能ファイルを$GOPATH/binに、ライブラリを$GOPATH/pkg にインストールします</td>
  <td>$ go mod init myproject<br>$ go get github.com/git-gonic/gin</td>
 </tr>
 <tr>
  <td>名前空間（パッケージ）の参照追加</td>
  <td>import</td>
  <td>import "mypackage/mylib"<br>import (<br>&nbsp&nbsp"fmt"<br>&nbsp&nbsp"time"<br>)</td>
 </tr>
</table>

