# Scope

プログラムにおいて名前が付けられるものは、そのスコープに応じて適切な命名をする必要があります。

<table>
<thead>
<tr>
  <th>Scope</th>
  <th>Bad:Good Example</th>
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
なお、必ず1～2文字にする必要はなく、可能であればカウンタ以外でループさせるべきです。
  </td>
</tr>

<tr>
  <td>Fn local</td>
  <td>foundCaracterIndex:charI, sourceObject:srcObj</td>
  <td>
関数内でのみ参照できるローカル変数は、（全てを司ろうとするGod関数でない限り）関数の目的が明確なため、
多少言葉足らずでも、その意味が自然と定まり、やや強めに短縮・省略することが可能です。
また変更しても理論上全く動作に影響しないため、最初は短めの名前を付け、他の変数が増えて混乱しそうになってから変更することも容易にできます。
  </td>
</tr>

<tr>
  <td>Class private</td>
  <td></td>
  <td>

  </td>
</tr>

<tr>
  <td>Project internal</td>
  <td></td>
  <td>

  </td>
</tr>

<tr>
  <td>Application public</td>
  <td></td>
  <td>

  </td>
</tr>
</tbody>
</table>

