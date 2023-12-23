# README
## これは何？
「あかならべ配列」という名称の日本語かな入力配列です。

日本語かな入力配列とは、特定のキーを入力することでひらがなを入力するためのキー配列です。

一般的な日本語かな入力配列としては、JISかな入力配列とQWERTYローマ字入力配列がよく知られています。

ややこしいですがQWERTYローマ字入力配列もひらがなを入力するための配列なので日本語かな入力配列の1つです。

## あかならべ配列の名前の由来
「AZIK」配列と「和ならべ」配列という2つの日本語かな入力配列をベースに作成したため、「AZIK」のAK、「和ならべ」の「ならべ」から取って「あかならべ」としました。

## あかならべ配列のメリット
* 入力に必要なキー数がローマ字入力と同程度（3段x10キーの30キー）であり、手の移動距離が少ない
* ローマ字入力同様、英語キーボード配列でも入力できる（その他3段x10キーの30キーあればどのような物理キーボード配列でも採用できる）
* 頻出するキーはホームポジションに、頻出する組み合わせのキーは隣り合って配置されており、ローマ字入力よりも手の移動距離が少ない
* 一部の日本語かな文字（拗音・長音）はローマ字入力よりも打鍵数が少ない
* Google日本語入力のローマ字テーブル機能で実装可能なため、当該IMEがインストール可能なWindows, Mac, Linuxで利用可能

## あかならべ配列のデメリット
* 既存の日本語かな入力配列と互換性がないため、使いこなすまでに多少の学習コストが必要

とはいえ、上記デメリットを軽減すべく、学習曲線をなだらかにするために配列にはいくつか工夫をしてあります。

## インストール方法
Google日本語入力＋JIS日本語配列またはUS英語配列キーボードの場合です。

1. このリポジトリにある akanarabe_jis_us.txt をダウンロードする
1. Google日本語入力のプロパティを開き、 一般タブ -> キー設定 -> ローマ字テーブル -> 編集 -> 編集 -> インポート... を選択する
1. さきほどダウンロードした akanarabe_jis_us.txt を選択する

JIS日本語配列/US英語配列以外の独自配列を使っている人は、この後のキー配置を参考に自分で改変してみてください。

akanarabe_corvus_skk.txt は筆者が CorvusSKK というIMEで使うためのローマ字テーブルファイルです。

## あかならべ配列のチュートリアル

あかならべ配列はローマ字入力の改良を目指した配列です。

ローマ字入力同様、子音キー＋母音キーの組み合わせで日本語かな文字を入力します。

たとえば「か」を入力するためには「k」相当のキーと「a」相当のキーを組み合わせて入力します。

まずは子音キーと母音キーの配置を見てみましょう。

## 前提_チュートリアルで使用するキー配置の表記方法

一般的なQWERTYキーボードの配列の場合、以下のように表現します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | Ｑ, Ｗ, Ｅ, Ｒ, Ｔ | Ｙ, Ｕ, Ｉ, Ｏ, Ｐ
2段目 | Ａ, Ｓ, Ｄ, Ｆ, Ｇ | Ｈ, Ｊ, Ｋ, Ｌ, ；
3段目 | Ｚ, Ｘ, Ｃ, Ｖ, Ｂ | Ｎ, Ｍ, `，`, `．`, `/`

## あかならべ配列の子音キー

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, Ｚ, Ｄ, Ｇ, Ｐ | ＃, ＃, ＃, ＃, ＃
2段目 | Ｎ, Ｓ, Ｔ, Ｋ, Ｈ | ＃, ＃, ＃, ＃, ＃
3段目 | Ｍ, Ｗ, ＃, Ｒ, Ｂ | ＃, ＃, ＃, ＃, ＃

## あかならべ配列の母音キー

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ＃, ｉ, ｅ, ＃
2段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ａ, ｕ, ｏ, ＃
3段目 | ＃, ＃, ＃, ＃, ＃ | ＃, ＃, ＃, ＃, ＃

## 子音キーと母音キーの配置を覚える
以下にQWERTYキーボードのキー配置とあかならべ配列で入力される文字の対応の例を示します。

QWERTYキーボードで入力するキー | 実際の子音キーと母音キーの組み合わせ | 出力される文字
---|---|---
ｆｊ | Ｋａ | か
ｆｉ | Ｋｉ | き
ｆｋ | Ｋｕ | く
ｆｏ | Ｋｅ | け
ｆｌ | Ｋｏ | こ
ｒｊ | Ｇａ | が
ｒｉ | Ｇｉ | ぎ
: | : | :

このルールに基づくといくつか入力できない文字があることに気付くと思いますが、そうした文字の入力方法は後述します。

子音キーと母音キーの配置におけるポイントは以下です。

* 子音キーは左手、母音キーは右手に配置されています。そのため左右の手で交互に打鍵しやすく効率良く手を動かせます。
* 日本語で頻出する子音である S, K, T, N, H, R がホームポジションと動かしやすい左手人差し指近辺に配置されています。
  * QWERTYローマ字配列と比較してTとNが特に入力しやすいはずです。
* 濁音、半濁音は各清音の上下に配置されています。「が行」「ざ行」「だ行」は上段、「ば行」のみ下段となっています。
  * 清音と横の位置を揃えているので、濁音の位置が覚えられていない状態でも、基本は清音の指を上にずらした先のキーを入力すれば濁音を入力できます。
  * 濁音は「ば行」のみ下段ですが、薬指、中指は上段の方が動かしやすく、人差し指は下段の方が動かしやすいことからそのように定義しています。
  * QWERTYキーボードでもTよりBの方が楽に指を動かせると感じるはずです。
  * 「ば行」と「ぱ行」だと前者の方が入力頻度が高いため、入力しやすい人差し指下段にBを配置しました。
  * QWERTYにおけるBと同じ位置のため、それで覚えましょう。
* 母音は日本語で頻出する「ai」「ei」「ou」といった二重母音が入力しやすい配置にしてあります。
  * 日本語の熟語は上記の組み合わせを含むことがとても多いです。
  * 例えば「製造工程」といった単語はQWERTYローマ字入力だと指があちらこちらに飛びますが、あかならべ配列だとQWERTYキーボードで soi wlk flk doi で入力できます。
* 「D+i」の組み合わせのみ、「ぢ」は殆ど使われないので「でぃ」が入力できるようにしてあります。
* 「っ」はローマ字同様に子音キーの連打で入力可能です。例えば「けっか」はQWERTYキーボードで fo ffj で入力できます。

## その他の単打キー
右手には母音以外にも単打で入力可能なキーがいくつか存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | や, ＃, い, え, ー
2段目 | ＃, ＃, ＃, ＃, ＃ | ゆ, あ, う, お, ん
3段目 | ＃, ＃, ＃, ＃, ＃ | よ, っ, `、`, `。`, ー

単打キーのポイントは以下です。

* 「ん」をローマ字のNNではなく単打キーかつ母音の近くのキーで入力できるようにしてあります。
  * 日本語で頻出する「an」「in」「un」「en」「on」をスムーズに入力できます。
  * たとえば「新幹線」といった単語はQWERTYキーボードでは si; fj; so; で入力できます。
* 「やゆよ」を子音キーＹと母音キーの組み合わせによる入力ではなく、単打キー化してあるので入力しやすくしてあります。
  * QWERTYキーボードでYのキーから縦に並んでいるので覚えやすいです。
  * 「やゆよ」との連接で出てきやすい「yan」「yui」「yuu」「you」「yon」をスムーズに入力できる配置です。
  * 「や」と母音の連接はほぼ出てこないので、母音をスムーズに入力できないQWERTYキーボードのYキーに配置しています。
* 長音「ー」をローマ字入力より入力しやすい位置に配置しています。
* 促音「っ」を単打でも入力できるようにしてあります。

## 拗音母音、長音母音キー
右手には通常の母音に加えて拗音と長音を母音として入力可能な拡張母音キーも存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | ya, i-, i, e, e-
2段目 | ＃, ＃, ＃, ＃, ＃ | yu, a, u, o, o-
3段目 | ＃, ＃, ＃, ＃, ＃ | yo, a-, u-, ＃, ＃

拡張母音キーのポイントは以下です。

* 「ゃゅょ」が母音キーとして使える
  * 「きゅ」を「K+yu」で入力できます。QWERTYキーボードだと fh で「きゅ」を入力可能です。
  * QWERTYキーボードでYのキーから縦に並んでいるので覚えやすいです。
* 長音付き母音が母音キーとして使える
  * 「かー」を「K+a-」で入力できます。QWERTYキーボードだと fm で「かー」を入力可能です。
  * 「コーナーケース」をQWERTYキーボードで入力する場合 f; am fp sk で入力できます。
  * 通常母音のaiueoの隣に同じ音の長音母音を配置しているため覚えやすくなっています。
  * 長音母音は長音単打キーで代替可能なので必ずしも覚える必要はありません。打鍵数を減らしたくなってきてから覚えましょう。

## 外来音子音レイヤ
ここまでのルールだと入力できない「ヴぃ」「ふぁ」「ちぇ」などの外来音を入力するための外来音子音レイヤと、レイヤ切り替えキーが存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, Ｗ, ＃, ＃, Ｔ | ＃, ＃, ＃, ＃, ＃
2段目 | ☆, Ｓ, Ｄ, Ｆ, Ｊ | ＃, ＃, ＃, ＃, ＃
3段目 | ＃, ＃, Ｃ, Ｖ, ＃ | ＃, ＃, ＃, ＃, ＃

外来音子音レイヤのポイントは以下です。

* レイヤ切り替えキーは☆の位置、QWERTYキーにおけるAキーです。
* A入力後は概ねQWERTYキーの配置通りのキーで外来音の子音が入力できます。
  * A->QWERTYキーボード上の外来音の音を示すキー->あかならべ配列の母音キー の順番で入力します。
  * もちろん長音母音も使えます。
  * 「しぇ」をQWERTYキーボードで入力する場合 aso で入力できます。
  * 「ふぁ」をQWERTYキーボードで入力する場合 afj で入力できます。
  * 「ちゃー」をQWERTYキーボードで入力する場合 acm で入力できます。
  * 「っ」も他の文字同様にAキー連打で入力可能です。たとえば「ばっふぁ」はQWERTYキーボードで ba aafj で入力できます。
  * 「でぃ」と「ぢ」のみ通常の濁音と外来音レイヤで入力できる文字が交換されています。「でぃ」はQWERTYキーボードで ei で、「ぢ」はQWERTYキーボードで adi で入力することになります。
  * JはQWERTYキーボードだと右手側であるため、近い音であるQWERTYキーのGの位置で入力可能です。
  * つまり「じぇ」をQWERTYキーボードで入力する場合 ago で入力できます。
  * 外来音は出現頻度が少ないため、QWERTYとほぼ同じ位置に子音を置き「A」でレイヤ切り替えすることだけ覚えておけば入力方法を思い出せるようにして学習コストを下げています。
* 詳しくは後述の表をご覧ください。

## 小文字・記号レイヤ
「ぁ」などの小文字および一部記号を入力するためのレイヤと、レイヤ切り替えキーが存在します。

段数 | 左手 | 右手
-----|-----|-----
1段目 | ＃, ＃, ＃, ＃, ＃ | ゃ, ＃, ぃ, ぇ, ＃
2段目 | ＃, ＃, ＃, ＃, ＃ | ゅ, ぁ, ぅ, ぉ, ＃
3段目 | ＃, ＃, ☆, ＃, ＃ | ょ, ＃, `,`, `.`, ・

小文字・外来音レイヤのポイントは以下です。

* レイヤ切り替えキーは☆の位置、QWERTYキーにおけるCキーです。
* C入力後に単打キーと同じ場所のキーを入力することで小文字が入力可能です。
* 「ゃ」をQWERTYキーボードで cy で入力できます。
* 「・」は通常のローマ字だとQWERTYキーボードの / で入力可能ですが、あかならべ配列では既に「ー」で使用しているため小文字・外来音レイヤで入力可能にしました。
* 「,」「.」は「、」「。」から変換せずに半角のカンマやドットが打ちたいときに使う想定です。

## あかならべ配列をカスタマイズする際のポイント
* ダウンロードした akanarabe_jis_us.txt を編集して、GoogleIMEで再度インストール方法にあるインポートを実行することで、あかならべ配列をカスタマイズすることができます。
* akanarabe_jis_us.txt は単なるテキストファイルなのでメモ帳アプリなどを使って編集してください。
* QWERTYキーボード配列におけるQキーはあかならべ配列で **1度も** 使用されていません。したがって Q + 他のキー の組み合わせで好きな文字を入力させるようなカスタマイズが追加可能です。
  * たとえばQWERTYキーボードのQの段と組み合わせて qq, qw, qe, qr, qt, qy, qu, qi, qo に対してJIS配列の数字段のキーで入力できる記号である `!"#$%&'()` を割り当てたりすると記号の入力が楽になるかもしれません。
  * vimキーバインドのカーソル移動キーであるhjklと組み合わせて qh, qj, qk, ql に対して矢印記号である ←, ↓, ↑, → を割り当てたりすると矢印の入力が楽になるかもしれません。
  * あるいは単純に二つ目の単打キーとして「っ」や「ー」を入力できるようにしても良いかもしれません。
  * あかならべ配列を使っていて、特定の文字をもっと効率良く入力したくなったならカスタマイズしてみましょう！
* あかならべ配列はJIS配列とUS配列のどちらにも対応できるような配列になっていますが、JIS配列だけに対応すれば良い場合 QWERTYキーボードの : に二つ目の長音キーを割り当てると長音入力が楽になるかもしれません。

## 外来音入力のQWERTY対応表
* 外来音の入力方法は少し特殊なので、QWERTYキーボードと入力文字の対応表を載せておきます。

QWERTYキーボードで入力するキー | 外来音レイヤにおけるキーの組み合わせ | 出力される文字
------------------|----------------|-----------------
awi | ☆W+i | うぃ
awo | ☆W+e | うぇ
awl | ☆W+o | うぉ
atj | ☆T+a | つぁ
ati | ☆T+i | てぃ
atk | ☆T+u | とぅ
ato | ☆T+e | つぇ
atl | ☆T+o | つぉ
aty | ☆T+ya | ちゃ
ath | ☆T+yu | てゅ
atn | ☆T+yo | ちょ
atm | ☆T+a- | つぁー
atu | ☆T+i- | てぃー
at, | ☆T+u- | とぅー
atp | ☆T+e- | つぇー
at; | ☆T+o- | つぉー
asj | ☆S+a | しゃ
asi | ☆S+i | し
ask | ☆S+u | しゅ
aso | ☆S+e | しぇ
asl | ☆S+o | しょ
asy | ☆S+ya | しゃ
ash | ☆S+yu | しゅ
asn | ☆S+yo | しょ
asm | ☆S+a- | しゃー
asu | ☆S+i- | しー
as, | ☆S+u- | しゅー
asp | ☆S+e- | しぇー
as; | ☆S+o- | しょー
adi | ☆D+i | ぢ
adk | ☆D+u | どぅ
ady | ☆D+ya | ぢゃ
adh | ☆D+yu | ぢゅ
adn | ☆D+yo | ぢょ
adu | ☆d+i- | ぢー
ad, | ☆d+u- | どぅー
afj | ☆F+a | ふぁ
afi | ☆F+i | ふぃ
afk | ☆F+u | ふゅー
afo | ☆F+e | ふぇ
afl | ☆F+o | ふぉ
afh | ☆F+yu | ふゅ
afm | ☆F+a- | ふぁー
afu | ☆F+i- | ふぃー
af, | ☆F+u- | ふゅー
afp | ☆F+e- | ふぇー
af; | ☆F+o- | ふぉー
agj | ☆J+a | じゃ
agi | ☆J+i | じ
agk | ☆J+u | じゅ
ago | ☆J+e | じぇ
agl | ☆J+o | じょ
agy | ☆J+ya | じゃ
agh | ☆J+yu | じゅ
agn | ☆J+yo | じょ
agm | ☆J+a- | じゃー
agu | ☆J+i- | じー
ag, | ☆J+u- | じゅー
agp | ☆J+e- | じぇー
ag; | ☆J+o- | じょー
acj | ☆C+a | ちゃ
aci | ☆C+i | ち
ack | ☆C+u | ちゅ
aco | ☆C+e | ちぇ
acl | ☆C+o | ちょ
acy | ☆C+ya | ちゃ
ach | ☆C+yu | ちゅ
acn | ☆C+yo | ちょ
acm | ☆C+a- | ちゃー
acu | ☆C+i- | ちー
ac, | ☆C+u- | ちゅー
acp | ☆C+e- | ちぇー
ac; | ☆C+o- | ちょー
avj | ☆V+a | ヴぁ
avi | ☆V+i | ヴぃ
avk | ☆V+u | ヴ
avo | ☆V+e | ヴぇ
avl | ☆V+o | ヴぉ
avh | ☆V+yu | びゅー
av, | ☆V+u | びゅー
avm | ☆V+a- | ヴぁー
avu | ☆V+i- | ヴぃー
av, | ☆V+u- | びゅー
avp | ☆V+e- | ヴぇー
av; | ☆V+o- | ヴぉー
