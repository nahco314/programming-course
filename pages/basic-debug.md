# エラー

- プログラムに間違いがあったときなど、プログラムを正常に実行できないときに**エラー**が出る

+ 大きく分けて2種類
  - コンパイルエラー: 文法のミスなど、そもそもプログラムを実行できないときに出る
  - 実行時エラー: 実行中に致命的な問題が発生したときに出る

---

# エラー - コンパイルエラー

- 初心者のうちはめちゃくちゃ遭遇する
- 原因はいろいろある

+ コンパイルエラーが発生したときには、エラーの原因を報告する**エラーメッセージ**が表示される
  + これを読んでエラーを修正する

---
clicks: 3
---

# エラー - コンパイルエラーの例 1

<div id="table">

<div id="cpp-sec">

ソースコード

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
  cout << "Hello,World!" << endl
}
```

</div>

<div id="message-sec">

エラーメッセージ

<div id="code-text">

```text
./Main.cpp: In function ‘int main()’:
./Main.cpp:5:33: error: expected ‘;’ before ‘}’ token
    5 |   cout << "Hello,World!" << endl
      |                                 ^
      |                                 ;
    6 | }
      | ~                                
```

</div>
</div>

</div>

<div v-click="1" id="message-part-sec" class="small-shadow">
<div id="message-part-box"></div>
<div v-click-hide="2">
↑このあたりで問題が発生している
</div>
</div>

<div v-click="2" id="message-detail-sec" class="small-shadow">
<div id="message-detail-box"></div>
「ここに `;` が必要だよ！」と言っている
</div>

<div v-click="3" id="problem-sec" class="small-shadow">
<div id="problem-box"></div>
<div>↑</div>
<div>セミコロンを忘れている</div>
</div>

<style>

#table {
  display: flex;
}

#cpp-sec, #message-sec {
  flex: 1;
}

#message-part-sec {
  position: absolute;
  top: 233px;
  left: 508px;

  font-size: 16px;
}

#message-part-box {
  height: 20px;
  width: 114px;

  border: 2px solid blue;
}

#message-detail-sec {
  position: absolute;
  top: 230px;
  left: 505px;

  font-size: 16px;
}

#message-detail-box {
  height: 120px;
  width: 390px;

  border: 2px solid orange;
  
  margin-bottom: 8px;
}

#problem-sec {
  position: absolute;
  top: 317px;
  left: 304px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  font-size: 16px;
}

#problem-box {
  height: 16px;
  width: 16px;

  border: 2px solid red;
}

pre[class*='language-'] {
  width: fit-content;
}

#code-text .slidev-code {
  font-size: 12px  !important;
}

</style>

---

# エラー - コンパイルエラーの例 2

<div id="table">

<div id="cpp-sec">

ソースコード

```cpp
#include <bits/stdc++.h>
using namespace std;
 
int main() {
　cout << "Hello,World!" << endl;
}
```

</div>

<div id="message-sec">

エラーメッセージ

<div id="code-text">

```text
./Main.cpp:5:1: error: stray ‘\343’ in program
    5 | 　cout << "Hello,World!" << endl;
      | ^
./Main.cpp:5:2: error: stray ‘\200’ in program
    5 | 　cout << "Hello,World!" << endl;
      |  ^
./Main.cpp:5:3: error: stray ‘\200’ in program
    5 | 　cout << "Hello,World!" << endl;
      |   ^
```

</div>
</div>

</div>

<div v-click id="message-part-sec" class="small-shadow">
<div id="message-part-box"></div>
↑このあたりで問題が発生している
</div>

<div v-click id="problem-sec" class="small-shadow">
<div id="problem-box"></div>
↑ここが全角スペースになってしまっている
</div>

<style>

#table {
  display: flex;
}

#cpp-sec, #message-sec {
  flex: 1;
}

#message-part-sec {
  position: absolute;
  top: 215px;
  left: 508px;

  font-size: 16px;
}

#message-part-box {
  height: 20px;
  width: 114px;

  border: 2px solid blue;
}

#problem-sec {
  position: absolute;
  top: 317px;
  left: 76px;

  font-size: 16px;
}

#problem-box {
  height: 16px;
  width: 16px;

  border: 2px solid red;
}

pre[class*='language-'] {
  width: fit-content;
}

#code-text .slidev-code {
  font-size: 12px  !important;
}

</style>

---
clicks: 5
---

# エラー - コンパイルエラーの例 3

<div id="table">

<div id="cpp-sec">

ソースコード

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
  cout << "Hello,World!" < endl;
}
```

</div>

<div id="message-sec">

エラーメッセージ

<div v-click-hide="1" id="code-text">

```text
./Main.cpp: In function ‘int main()’:
./Main.cpp:5:26: error: no match for ‘operator<’ (operand types are ‘std::basic_ostream<char>’ and ‘<unresolved overloaded function type>’)
    5 |   cout << "Hello,World!" < endl;
      |   ~~~~~~~~~~~~~~~~~~~~~~~^~~~~~
In file included from /usr/include/c++/9/regex:62,
                 from /usr/include/x86_64-linux-gnu/c++/9/bits/stdc++.h:110,
                 from ./Main.cpp:1:
/usr/include/c++/9/bits/regex.h:1048:5: note: candidate: ‘template<class _BiIter> bool std::__cxx11::operator<(const std::__cxx11::sub_match<_BiIter>&, const std::__cxx11::sub_match<_BiIter>&)’
 1048 |     operator<(const sub_match<_BiIter>& __lhs, const sub_match<_BiIter>& __rhs)
      |     ^~~~~~~~
/usr/include/c++/9/bits/regex.h:1048:5: note:   template argument deduction/substitution failed:
./Main.cpp:5:28: note:   ‘std::basic_ostream<char>’ is not derived from ‘const std::__cxx11::sub_match<_BiIter>’
    5 |   cout << "Hello,World!" < endl;
      |                            ^~~~
In file included from /usr/include/c++/9/regex:62,
                 from /usr/include/x86_64-linux-gnu/c++/9/bits/stdc++.h:110,
                 from ./Main.cpp:1:
/usr/include/c++/9/bits/regex.h:1124:5: note: candidate: ‘template<class _Bi_iter, class _Ch_traits, class _Ch_alloc> bool std::__cxx11::operator<(std::__cxx11::__sub_match_string<_Bi_iter, _Ch_traits, _Ch_alloc>&, const std::__cxx11::sub_match<_BiIter>&)’
 1124 |     operator<(const __sub_match_string<_Bi_iter, _Ch_traits, _Ch_alloc>& __lhs,
      |     ^~~~~~~~
/usr/include/c++/9/bits/regex.h:1124:5: note:   template argument deduction/substitution failed:
./Main.cpp:5:28: note:   ‘std::basic_ostream<char>’ is not derived from ‘std::__cxx11::__sub_match_string<_Bi_iter, _Ch_traits, _Ch_alloc>’
    5 |   cout << "Hello,World!" < endl;
      |                            ^~~~
In file included from /usr/include/c++/9/regex:62,
                 from /usr/include/x86_64-linux-gnu/c++/9/bits/stdc++.h:110,
               ...
```

</div>

<div v-click-hide="3">
<div v-click="1" style="color: red">
→長すぎ！
</div>
<div v-click="2">
→とりあえず最初の部分だけ見てみる
</div>
</div>

<div v-click="3" id="code-text">

```text
./Main.cpp: In function ‘int main()’:
./Main.cpp:5:26: error: no match for ‘operator<’ ...(略)
    5 |   cout << "Hello,World!" < endl;
      |   ~~~~~~~~~~~~~~~~~~~~~~~^~~~~~

...(略)
```

</div>

</div>

</div>

<div v-click="4" id="message-detail-sec" class="small-shadow">
<div id="message-detail-box"></div>
<div>↑</div>
<div>とにかく、ここらへんがおかしいっぽい？</div>
</div>

<div v-click="5" id="problem-sec" class="small-shadow">
<div id="problem-box"></div>
<div>↑</div>
<div>ここが &lt;&lt; でなく &lt; になってしまっている</div>
</div>

<style>

#table {
  display: flex;
}

#cpp-sec, #message-sec {
  flex: 1;
  word-break: break-all;
  min-width: 0;
}

#message-detail-sec {
  position: absolute;
  top: 258px;
  left: 600px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  font-size: 16px;
}

#message-detail-box {
  height: 40px;
  width: 24px;

  border: 2px solid blue;
}

#problem-sec {
  position: absolute;
  top: 315px;
  left: 174px;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  font-size: 16px;
}

#problem-box {
  height: 20px;
  width: 20px;

  border: 2px solid red;
}

pre[class*='language-'] {
  width: fit-content;
}

#code-text .slidev-code {
  font-size: 12px  !important;
}

.slidev-vclick-hidden {
    block-size: 0;
}

</style>

---

# エラー - コンパイルエラーの対処法

1. エラーメッセージを読み、おかしそうなところを探す
    - エラーメッセージには非本質な部分が多いときもあるので、うまく取捨選択する
2. わからなければ、エラーメッセージ(の重要そうな部分)で検索してみる
3. それでもわからなければ、人に聞く(「なんでも質問」などで)
    - **まずググろう**

---

# エラー - 実行時エラー

- 実行中に致命的な問題が発生したときに実行時エラーが発生する
  - 実行時エラーが発生すると、プログラムは直ちに終了する
- これも原因はいろいろあるが、まだそんなに遭遇しないかも

+ 実行時エラーは、**エラーメッセージが表示されない**(ものによるが)

---

# エラー - 実行時エラー

- ここまでの内容の範囲で発生する可能性のある実行時エラーは、おそらく1種類だけ

<v-click>

+ ゼロ除算: ゼロで割り算をしようとすると実行時エラーになる
  - 当然、0で割ったあまりを求めようとしてもエラー

</v-click>

---

# エラー

- 演習問題
  - https://atcoder.jp/contests/apg4b/tasks/APG4b_cu
