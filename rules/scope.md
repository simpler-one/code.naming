# Scope

プログラムにおいて名前が付けられるものは、そのスコープに応じて適切な命名をする必要があります。

<table>
<thead>
<tr>
  <th>Scope</th>
  <th>Long:Short Example</th>
  <th>Ddescription</th>
</tr>
</thead>

<tbody>
<tr>
  <td>Loop counter</td>
  <td>arrayIndexCounter:i, dataGridRowIndex:r, currentColumnIndex:c </td>
  <td>
ループカウンタとして使用される変数は短くても問題ないことが多く慣習的に1～2文字程度の名前が付けられる傾向にあります。
見ればカウンタであることが一目で分かるため、裏を返せばそれ以外の変数で用いてはいけない命名です。
なお、必ずしも1～2文字にする必要はなく、可能であればカウンタ以外でループさせるべきです。
  </td>
</tr>

<tr>
  <td>Func local</td>
  <td>stringFunctionTable:strFnTbl, foundCharacterIndex:charI, sourceObject:srcObj</td>
  <td>
関数内でのみ参照できるローカル変数は、（全てを司ろうとするGod関数でない限り）関数の目的が明確なため、
多少言葉足らずでも、その意味が自然と定まり、やや強めに短縮・省略することが可能です。
また変更してもI/Fに関わらないため理論上全く動作に影響なく、変更も容易にできます。
なお、必ずしも短縮する必要はありません。
  </td>
</tr>

<tr>
  <td>Class private</td>
  <td>stringFunctionTable:strFnTable, previousCharacter:prevChar</td>
  <td>
private変数・関数、private関数の引数など、クラス等の1ファイルで閉じたスコープを持つ物は、（全てを司ろうとするGodクラスでない限り）クラスの目的が明確なため、
ローカル変数同様、多少言葉足らずでも、その意味が自然と定まり、やや短縮・省略することが可能ですが、ローカル変数ほど強い短縮（母音抜きなど）は適しません。
また変更してもI/Fに関わらないため理論上全く動作に影響なく、変更も容易にできます。
なお、必ずしも短縮する必要は無く、また非privateなメンバ（getter等）と1:1で対応する場合は短縮しない方が良いでしょう。
  </td>
</tr>

<tr>
  <td>Project internal</td>
  <td>stringFunctionTable:strFunctionTable, previousCharacter:previousChar</td>
  <td>
クラスや非privateなメンバなど、複数のファイルに渡って参照される、比較的開いているがプロジェクトで閉じたスコープを持つ物は、そのクラスのI/Fを示すため、
言葉足らずであるべきでなく、やや堅い命名が要求されます。
使用できる短縮はHTTPやALBなど一般的に使われているものと、プロジェクト内で定められたものに限るべきです。
また変更に関しても複数のファイルに渡るため、静的型付けが弱い言語では名前の変更漏れが発生する恐れがあります。
さらに継承関係がある場合はより複雑になり、修正はより困難になるため安易な命名は避けるべきです。
  </td>
</tr>

<tr>
  <td>Open</td>
  <td>(none)</td>
  <td>
プロジェクト内に留まらす、ライブラリとしての関数やクラスの提供、WebAPIなど3rdパーティーが参照することを前提とした完全に開かれたスコープを持つ物は、
APIそのものを示すため、言葉足らずであるべきでなく、より堅い命名が要求されます。
さらに変更に関してはバージョン管理や互換性の問題が発生し、容易に修正できないため、入念な設計を要します。
また、特定の言語の体系・実装に依存した命名は好ましくありません（）。
 </td>
</tr>
</tbody>
</table>

