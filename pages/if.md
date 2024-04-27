# 条件分岐

- 複雑な処理を記述するには、条件分岐が必要不可欠

+ C++では、**if文**を使う

<!--
条件分岐、とか言われてもピンと来にくいだろうが、とりあえず「複雑な処理には分岐がいる」というそれらしい文言でゆるく納得させて実例を見せていく
-->

---

# 条件分岐 - 命題

- 「条件」ってなに？

  <div v-click="1">
  
  - 「天気が晴れなら」 <span v-click="5"> → 「天気が晴れである」 </span>
  
  </div>
  <div v-click="2">
  
  - 「気温が 30℃ 以上なら」 <span v-click="6"> → 「気温が 30℃ より高い」 </span>
  
  </div>
  <div v-click="3">
  
  - 「x が 3 よりも小さいなら」 <span v-click="7"> → 「x が 3よりも小さい」 </span>
  
  </div>

<br>

<div v-click="4">

+ 条件には、「判断材料の部分」がある

</div>

<br>

<div v-click="8">

+ こういったものを**命題**と呼ぶ

</div>

<!--
命題という概念と、条件と命題の関係について正確に理解させる

これらの概念はC++における条件と命題(または真偽値)というような関係と似ていて、それらの理解に関わってくると思う
-->

---

# 条件分岐 - 真偽値

<v-clicks>

- 命題は、正しいか正しくないかが定まる

+ ある命題が正しいとき、その命題は真である
+ ある命題が正しくないとき、その命題は偽である

- 真/偽の2値のことを真偽値とよぶ

</v-clicks>

<!--
命題というものを本当に正確に定義・議論しようとすると大変なのでまあ多少緩く
-->

---

# 条件分岐 - 真偽値

- C++ では bool 型で扱う
  - `true` で真、 `false` で偽を表す

+ `2 < 3` みたいな感じで不等式や等式を書けば、その命題の真偽値となる

<!--
厳密に言うなら、不等式や等式といった式は評価されるとその審議に応じて真偽値となる、という感じになるんだが、難しいので「式を普通に書けばその真偽値になります」ぐらいのゆるふわさで
-->

---

# 条件分岐 - 真偽値

| 記号        | 意味           |
|-----------|--------------|
| `a == b`  | a と b が等しい   |
| `a != b`  | a と b が等しくない |
| `a < b`   | a が b 未満     |
| `a <= b`  | a が b 以下     |
| `a > b`   | a が b 超過     |
| `a >= b ` | a が b 以上     |

---

# 条件分岐 - if

- `if (条件となる真偽値) {中身}`

+ 条件となる真偽値が真のときのみ、中身の部分が実行される

<!--
真偽値あたりの概念がちゃんと導入できてれば、if文自体は難しくないはず

強いていうなら、「if文が実行されるときに条件の部分が評価されて、その値に応じて中身が実行されるかどうかが分岐する」というフローをちゃんと理解させることは重要
-->

---
clicks: 5
---

# 条件分岐 - if

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n < 0) {
    n = -n;
  }
  
  cout << n << endl;
}
```

</center>

<div v-click-hide="4"><div v-click="1" class="box" id="if-box"></div></div>

<div v-click-hide="3" id="term-sec">
<div v-click="2">
<div id="term-box"></div>
<div class="small-shadow comment">
条件
</div>
</div>
</div>

<div v-click-hide="4" id="content-sec">
<div v-click="3">
<div id="content-box"></div>
<div class="small-shadow comment">
中身
</div>
</div>
</div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

#if-box {
  border-color: orange;
  
  top: 275px;
  left: 125px;

  height: 102px;
  width: 162px;
}

#term-sec {
  position: absolute;

  top: 282px;
  left: 178px;

  font-size: 24px;

  text-align: center;
}

#term-sec .message {
  margin: 4px 0 0;
}

#term-box {
  height: 27px;
  width: 66px;

  border: 2px solid blue;
}

#content-sec {
  position: absolute;

  top: 313px;
  left: 154px;

  font-size: 24px;

  text-align: center;
}

#content-sec .message {
  margin: 4px 0 0;
}

#content-box {
  height: 27px;
  width: 88px;

  border: 2px solid blue;
}

</style>

<!--
これは入力値の絶対値を計算するプログラム
-->

---

# 条件分岐 - if

- 中身が単一の文である if 文は、{} を省略して書くこともできる
  - 推奨しない

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n < 0) n = -n;
  
  cout << n << endl;
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

<!--
こうも書けるけど、読みにくいから推奨しないよー、という紹介
-->

---

# 条件分岐 - else

- `if (条件となる真偽値) {真のときの中身} else {偽のときの中身}`

+ 条件となる真偽値が真のときは普通に if の中身が、偽のときには else の方の中身が実行される

---
clicks: 3
---

# 条件分岐 - else

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n % 2 == 0) {
    cout << "nは偶数です" << endl;
  } else {
    cout << "nは奇数です" << endl;
  }
}
```

</center>

<div v-click-hide="2" id="true-sec">
<div v-click="1">
<div id="true-box"></div>
<div class="small-shadow comment">
真ならここ
</div>
</div>
</div>

<div v-click-hide="3" id="false-sec">
<div v-click="2">
<div id="false-box"></div>
<div class="small-shadow comment">
偽ならここ
</div>
</div>
</div>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

#true-sec {
  position: absolute;

  top: 313px;
  left: 154px;

  font-size: 24px;

  text-align: center;
}

#true-sec .message {
  margin: 4px 0 0;
}

#true-box {
  height: 27px;
  width: 345px;

  border: 2px solid blue;
}

#false-sec {
  position: absolute;

  top: 373px;
  left: 154px;

  font-size: 24px;

  text-align: center;
}

#false-sec .message {
  margin: 4px 0 0;
}

#false-box {
  height: 27px;
  width: 345px;

  border: 2px solid blue;
}

</style>

<!--
2で割ったあまりで偶奇を判定するのも実は自明じゃないので説明する
-->

---

# 条件分岐 - else

- 中身が単一の文である else 文は、{} を省略して書くこともできる
  - if と同様

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n % 2 == 0) cout << "nは偶数です" << endl;
  else cout << "nは奇数です" << endl;
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 20px  !important;
}

</style>

---

# 条件分岐 - else if

- if と else を組み合わせて、複雑な分岐もできる
  - 「A ならこれを、B ならこれを、C ならこれを実行する」みたいな

---

# 条件分岐 - else if

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n % 15 == 0) {
    cout << "FizzBuzz" << endl;
  } else if (n % 3 == 0) {
    cout << "Fizz" << endl;
  } else if (n % 5 == 0) {
    cout << "Buzz" << endl;
  } else {
    cout << n << endl;
  }
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 16px  !important;
}

</style>

<!--
FizzBuzzがプログラミング界隈で有名な(海外の数字遊びの再現の)プログラムであるという説明はする
-->

---

# 条件分岐 - else if

- `else if` という構文があるわけではない
- else の中身が単一の文(if 文)なので、{}を省略可能

<!--
あくまでelse ifはifとelseを組み合わせたものでしかない(特別な構文要素とかではない)ってのは言っておきたい(そんなに重要でもないが)
-->

---

# 条件分岐 - else if

+ こう書いても一緒

<center>

```cpp
int main() {
  int n;
  cin >> n;
  
  if (n % 15 == 0) {
    cout << "FizzBuzz" << endl;
  } else {
    if (n % 3 == 0) {
      cout << "Fizz" << endl;
    } else {
      if (n % 5 == 0) {
        cout << "Buzz" << endl;
      } else {
        cout << n << endl;
      }
    }
  }
}
```

</center>

<style>

pre[class*='language-'] {
  width: 800px;
  margin-top: 20px;
}

.slidev-code code {
  font-size: 11.5px  !important;
}

</style>

<!--
elseの後のifが入る部分の{}を省略しなかったらこうなるよー、っていうことね
-->

---

# 条件分岐 - 論理演算

- 真偽値の計算を**論理演算**と呼ぶ
  - 「A または B」「C でないなら」とか

| 記号         | 意味                     |
|------------|------------------------|
| `A && B`   | A かつ B                 |
| `A \|\| B` | A または B                |
| `!A`       | A の否定(A が真なら偽、偽なら真になる) |

<style>

table {
  margin-top: 50px;
}

</style>

<!--
論理演算といういかつめの言葉で紹介したあと、「または」とかの簡単な概念だよー、って言う
-->

---

# 条件分岐 - 論理演算

- 例
  - `n % 15 == 0` は `n % 3 == 0 && n % 5 == 0` と書き換えることができる

<!--
これもそんなに自明なことじゃないので説明
-->

---

# 条件分岐

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cq
