---
published: true
layout: bookpage_ja-JP
weight: 60
category: workflow
title: スペース、メトリクス、および カーニング
---

文字の間隔（字間スペース）は、フォント・デザインでの需要で、欠くことのできない部分です。

フォントの文字間隔デザインは、フォントの全デザイン・プロセスの不可欠の部分として行なわなければなりません。フォントが上手く機能するには、適切な文字間隔が必要です。

FontForge では、「**メトリック・ウィンドウ**」でフォントのメトリクスを指定でき、文字間の間隔を変更し、グリフ同士がどのように見えるかを評価します。「メトリック・ウィンドウ」はメイン・ウィンドウ項目の「メトリック」から、または、キーボードの <kbd>Ctrl</kbd> ＋ <kbd>K</kbd> コマンドで開くことができます。

二つのグリフ間の間隔には二つの項目があります：　第一グリフの「後のスペース」と第二グリフの「前のスペース」です。グリフ間のスペースは各グリフの「サイドベアリング」（左右の余白）から成り立っています。各グリフには、左サイドベアリングと右サイドベアリングがあります。次の例は「オープンサンズ Open Sans」フォントの小文字「a」の場合で、右サイドベアリングは「166」ユニット、左サイドベアリングは「94」ユニットに設定されています。

<img src="../en-US/images/sidebearings.png" alt="">

## <strong>「メトリック・ウィンドウ」の基本機能</strong>

文字のサイドベアリングは、FontForge の「メトリック・ウィンドウ」で 5 通りの編集が可能です。

- 各サイドベアリングの境界線を手動でドラッグします。
- 文字を手動でドラッグします。但し、文字のドラッグでは左側のサイドベアリング値のみが変更される点に注意してください。
- サイドベアリングの値を「メトリクス・ウィンドウ」のメトリクス表で直接編集します。
- キーボードを使用して、サイドベアリング値を増減します。
- 「メトリック・ウィンドウ」のメトリック・メニューでコメントを使用する。

### キーボードでサイドベアリング値を調整する

FontForge で手早くかつ正確にメトリック値を調整するひとつの方法は、キーボードの「上」「下」「左」「右」キーを使用することです。「上」「下」キーは値を増減するために用い、 <kbd>Alt</kbd> ＋ <kbd>Up</kbd>、<kbd>Alt</kbd> ＋ <kbd>Down</kbd>、<kbd>Alt</kbd> ＋ <kbd>Left</kbd> および <kbd>Alt</kbd> ＋ <kbd>Right</kbd> は「メトリック・ウィンドウ」内のその他の設定箇所への移動に使用します。

## 一般的な原則

一般的な原則として、「A、H、I、M、N、O、T、U、V、W、X、Y、o、v、w、x」のような左右対称形の文字では、左右両側におなじサイドベアリングを持ちます。たとえば、「H」の左と右のサイドベアリングは同じ大きさです。ただし、これは絶対厳守の規則ではなく、一般規則であることに注意してください。

>> ※ 訳注： この規則については [「11. 文字「o」と「n」を作成する」](../ja-JP/Creating_o_and_n.md) でも言及されています。

デザイン中の文字に字間スペースを設定する場合、自分の眼を信頼することが重要です。兎にも角にも、「デザインする、よく見る、修正する、もう一度見る」ということです。

まったくの初心者であれば、計算によるスペース設定に頼れば信頼できる結果が得られるとは思わないでください。ふたつの文字間の寸法が等しくない場合でも、目にはそれらが等しいように見えることがあります。この顕著な例は、文字「H」と「O」の間のスペース設定で見ることができます。次の例の一つ目では、「H」と「O」のサイドベアリングは同一ですが、均等でないように見えます。二つ目のサイドベアリングは同一ではありませんが、字間の間隔は均等であるようにみえます。

<img src="../en-US/images/hoohooo2.png" alt="">
<img src="../en-US/images/hoohooo1.png" alt="">

このようなサンプル・テキストを生成するツールは、[Nina Stössinger](http://www.ninastoessinger.com/) 氏が作成した [Stringmaker](http://www.ninastoessinger.com/stringmaker/) を利用できます。

## <strong>メトリクス編集用の「メトリック・メニュー」コマンド</strong>

「**幅の中央に**」（Center in Width）：　このコマンドは、作業中のグリフを現在の文字幅の中央に移動します。

「**ウィンドウ・タイプ**」（Window Type<sup>※</sup>）：　FontForge の「メトリック・ウィンドウ」はメトリクス調整に二通りの動作モードが設定できます。

>>《※ 訳注：　メニュー項目から対象となるグリフの **アウトライン・ウィンドウを開く** ⇒ **メトリック** ⇒ **メトリック・ウィンドウを開く** ⇒ **メトリック** ⇒ **Window Type**》

- 「**送り幅のみ**」（Advance Width Only）：　このモードでは、メトリック・ビューはグリフの「送り幅」調整のみに使用できます。

- 「**両方**」（Both）：　このモードでは、メトリック・ビューは「送り幅」か「カーニング」のどちらかを調整できます。

「**幅を設定**」（Set Width）：　このコマンドは作業中のグリフの幅を変更します。

「**左サイドベアリングを設定**」（Set LBearing）：　左側のサイドベアリング値を変更できます。

「**右サイドベアリングを設定**」（Set RBearing）：　右側のサイドベアリング値を変更できます。

## <strong>字間スペース設定の基本</strong>

以下の方法は、フォントのメトリック設定を行なうに際して、効果的に開始できることを意図して考え出されたものです。

手始めに、メトリック・ウィンドウで小文字の「o」が並ぶ文字列で文字の間隔が適切に見えるまで左右のサイドベアリングを調整します。この「適切」な感じを見出すひとつの方法は、「文字 o の内部の空白」に調和する「文字 o の間の空白」というものを探すことです。一般的には、傾斜したフォントまたはイタリック体のフォントという例外を除いて、小文字「o」の左右のサイドベアリングは同一であるべきです。「o」文字列のスペース設定に満足できたら、フォントから「n」文字を挿入して（次の画像を参照）、「n」の間隔が「o」文字列の並びと調和するように「n」のサイドベアリングを調整します。わたしたちの眼の見え方の性質上、「n」の右側のサイドベアリングは常に左側のサイドベアリングよりも小さな値になり、「o」の両側のサイドベアリングは「n」のいずれのサイドベアリングよりも小さいことに注意してください。

<img src="../en-US/images/snapshot1_1.png" alt="">

「n」と「 o」の字間が適切に設定し終えたら、この二文字の設定内容を他の文字の文字列のサイドベアリング設定に利用できます。たとえば、
 
- 「o」の左側のサイドベアリングは、「c」「d」「e」「q」の左側サイドベアリングに利用できます。
- 「o」の右側のサイドベアリングは、「b」「p」の右側サイドベアリングに利用できます。
- 「n」の右側のサイドベアリングは、「h」「m」の右側サイドベアリングに利用できます。
- 「n」の左側のサイドベアリングは、「b」「h」「k」「m」「p」「r」の左側サイドベアリングに利用できます。

**【注意】**　上記の内容は、言及されている文字で正しいサイドベアリング値を見つけるための出発点として、超効果的なガイドライン（目安）です。

<img src="../en-US/images/snapshot2.png" alt="">

ここからは、上図にあるように、「n」と「o」の文字列に対して、残りの小文字のサイドベアリング設定を行なうと合理的です。ここでも、自分の眼を信じて、適切な文字間の調和を求めてください。

## <strong>大文字</strong>

大文字も、上述の原則を用いて、同じようにスペース調整が可能です。たとえば、文字列「Hooooo」を手始めに、後続の「o」の文字列とバランスが取れるまで「H」の右側のサイドベアリングを調整します。「H」の左側のサイドベアリングを右側のサイドベアリングと等しくすると、大文字「O」は「H」に対して間隔を開けることができます（下図を参照）。

<img src=" ../en-US/images/snapshot3.png" alt="">

このあと、すべての残りの文字の字間をすでにスペース設定の終わった文字に対して調整します。このやり方は、フォントの字間設定の第一歩として十分に利用できますが、より高レベルの文字間隔を実現するには、さらに細かなスペースの微調整が必要であることにも注意してください。この目的で利用できるその他の文字列には、「naxna」「auxua」「noxno」「Hxndo」などがあります。

## <strong>カーニング</strong>

[カーニング](../ja-JP/Glossary.md#kerning-カーニング)（Kerning）とは特定の文字のペア（組み合わせ）に適用される字間スペースの調整のことです。カーニングを設定すると、文字のサイドベアリングに設定された間隔に加えて、個別の特定文字ペア（組み合わせ）のスペース設定も適用します。文字の間隔調整のためにしばしばカーニング処理が必要になる一般的な文字の組み合わせ例は、「WA」「Wa」「To」「Av」などです。以下の例では、カーニング処理がない場合、文字の組み合わせ「To」と「Av」の文字間隔が広くなりすぎますが、カーニング処理ありの場合、こうした組み合わせ文字の字間は、それ以外のフォントの字間の感じにずっとよく調和しています。

<img src="../en-US/images/kern1.png" alt="">
<img src="../en-US/images/kern2.png" alt="">

FontForge の「メトリック・ウィンドウ」を使用して、サイドベアリングとカーニング値の両方を指定できます。カーニング値は、FontForge ではいくつかの方法でフォントに適用可能です。その中の二つを以下に示します：　クラスを使用したカーニングと個々の文字ペア（組み合わせ）のカーニングです。

## <strong>FontForge の「メトリック」メニュー</strong>

「**ウィンドウ・タイプ**」（Window Type）：　FontForge の「メトリック・ウィンドウ」はカーニング調整に二通りの動作モードが設定できます。

- 「**カーニングのみ**」（Kerning Only）：　このモードでは、メトリック・ビューは「カーニング」調整のみに使用できます。

- 「**両方**」（Both）：　このモードでは、メトリック・ビューは「送り幅」か「カーニング」のどちらかを調整できます。

「**クラス毎のカーニング**」（Kern By Classes）：　このコマンドは、カーニング・クラスを操作するダイアログ・ウィンドウを開きます。

「**カーニングペアの詳細**」（Kern Pair Closeup）：　このコマンドは、すでに設定済のカーニング・ペアの調整や新しいペアの作成ができるダイアログ・ウィンドウを開きます（下記参照）。

<img src="../en-US/images/kerncloseup.png" alt="" height="686" width="632">

## <strong>キーボードでカーニング値を調整する</strong>

サイドベアリング値の調整と同様、カーニング値もキーボードの <kbd>Up</kbd>、<kbd>Down</kbd>、<kbd>Left</kbd> および <kbd>Right</kbd> キーを用いて FontForge で素早く且つ正確に編集できます。<kbd>Up</kbd> と <kbd>Down</kbd> キーは設定値の増減に用い、<kbd>Alt</kbd> ＋ <kbd>Up</kbd>、<kbd>Alt</kbd> ＋ <kbd>Down</kbd>、<kbd>Alt</kbd> ＋ <kbd>Left</kbd> および <kbd>Alt</kbd> ＋ <kbd>Right</kbd> は「メトリック・ウィンドウ」内のその他の設定箇所への移動に使用します。

## <strong>個々の文字ペアのカーニング</strong>

これは FontForge のカーニング・ペア作成の最も基本的な部分です。「メトリック・ウィンドウ」では、右側の文字を左側の文字の方へ／方から手動で動かすか、ウィンドウ内のメトリクス・テーブルで直接カーニング値を編集することで、二文字間のカーニング値を調整できます。文字をドラッグしてカーニング値を変更するには、二つの文字の間にマウス・カーソルが移動したときに現れる「カーニング・ツール」ハンドルを使用します（次のスクリーン・ショットをご覧ください）。メトリクス・テーブル内のカーニング値は、手動で値を入力するか、キーボードの「上／下」キーを使って値を増／減して、変更が可能です。

<img src="../en-US/images/mnl-kern.png" alt="">

## <strong>クラスを用いたカーニング</strong>

クラスを用いたカーニングでは、字間を大幅に短縮できます。

FontForge の「**カーニング・クラス**」（Kern class）を作成すると、同じカーニング値を持つ文字のグループを構築できます。たとえば、ある文字（たとえば文字「T」など）が前に来るときに文字「o、c、d、e、q」が常に同じカーニング値を持つ場合のクラス（「o_left_bowl」のように名前を付けます）を作成できます。また「T」自体が Tcaron や Tbar などの他の文字を含む別のクラスのメンバーであることもあります。

カーニングを用いたクラスは「GPOS 検索」の一種です。このカーニングに関する情報は、メニュー項目から **エレメント** ⇒ **フォント情報** ⇒ **Lookups**(検索) ⇒ **GPOS** タブ と辿れば見つかります（いつでもこの処理を実行でき、いつでも処理を中断した場所に戻ることができます）。

<img src="../en-US/images/kernclass1.png" alt="">

「**Add Lookup**（検索の追加）」ボタンをクリックし、「種類」欄で「**Pair Position (Kerning)**」〔ペア位置 (カーニング)〕を選択します。

<img src="../en-US/images/kernclass2.png" alt="">

「&lt;New&gt;」ボタンは押さないでください。その隣の下矢印ボタン🔽をクリックし、「**kern: 横書きカーニング**」を選択します。「New」の部分に「Kern」と記載されます。一番下の「**Lookup Name**」（検索名）欄の名称は「デフォルト」（自動表示）のままでも構いませんし、自分で指定することもできます。そのあと、「**OK**」ボタンを押します。

「GPOS」タブに戻ると、たった今選択した「検索名」が検索テーブルに表示されています。各カーニング・クラスには、個別のサブテーブルがあります。サブテーブルを作成するには、「**Add Subtable**」（サブテーブルを追加）ボタンを押します。サブテーブル名は、デフォルトのままで構いません。

多くの選択肢があるサブテーブルの設定ウィンドウが表示されます。

<img src="../en-US/images/kernclass3.png" alt="">

最初に「**Use individual kerning pairs**」（個々のカーニングペアを使用）か「**Use a matrix of kerning classes**」（カーニングクラスの組み合わせを使用）のどちらかを選択します。

クラスを選択すると、クラスを作成できる以下のダイアログが開きます。**もし、 元字（オリジナル）と一緒に参照先をカーニングしたい場合は、クラスを選択します。**

このダイアログで作成しているクラス間のカーニング値を FontForge が「推測」（guess）または「自動カーニング」（Autokern）できるように選択することも可能である点に注意してください。FontForge でカーニング値を推定する場合、間違いなく多くの試行錯誤と実験が必要になりますが、フォントのカーニングにどのような改善がもたらされるかを確認する簡単な方法として「自動カーニング」機能（autokern）を使用することは理に適っています。

別の値を試す必要があるまでは、残りのパラメーター値はそのまま変更しないでおきましょう。

上記のダイアログで「**OK**」をクリックすると、次のウィンドウが開き、この二つのクラスのカーニング量を微調整できます。たとえば、二番目のスクリーンショットでは、文字「T」が含まれるクラスがひとつ、文字「o」が含まれるクラスがひとつの、ふたつのクラスが作成されました。

<img src="../en-US/images/kern_classes_1.png" />

<img src="../en-US/images/kernclass4.png" alt="">

すべてのグリフを選択し後からクラスを削除することも、あるいは、カーニングを施したいグリフだけを選択することもできます。同時に調整したいすべてのグリフを選択すると、一緒にカーニングを行ないたくない異なる書記体系の文字（たとえば、ラテン文字、ギリシア文字、キリル文字、…）を作業中でない限り、FontForge は選択したグリフをクラスに配置します。

「**OK**」ボタンを押すと、上部に幾つかのパラメーター、ふたつのクラスのリスト、一番下に文字の組み合わせ表がある、大きなウィンドウが開きます《※ 訳注：直ぐ上の二番目のスクリーンショットのことか？》。文字の組み合わせ表内のボックスを選択すると、その文字ペアがどのようにカーニングされるかを見ることができます。もし気に入らなければ、グリフのペアの上に表示されている「カーニング・オフセット」ボックスで、カーニングのオフセット値を調節できます。

万が一何かおかしなことが発生したら、そして実際にそうなったら、「**Cancel**」ボタンを押してください。そして、サブテーブルをダブル・クリックすると大きなウィンドウに戻ります（サブテーブルが表示されない場合は、テーブルの横にあるプラス記号を押してください）。何の問題もなく多くの作業を行なえた場合には、「**OK**」ボタンを押してから作業に戻ってください。そうすれば、万が一おかしなことが起こった場合にそれまでの作業内容を失なわずに済みます。

「メトリック・ウィンドウ」は、後で最終確認に用いることができます。このウィンドウで調整作業を行なっている間は、何度もクラスやペアをカーニングしますかといったことを口うるさく聞いてきます。でも、それを気に入るかどうかを試しにやってみてはいかがでしょうか？　ただし、経験を積んだデザイナーはそのようなお節介が気に入らないことも判っていますので、上述のようにすべてのカーニングを実行してください：　すなわち、**要素** ⇒ **フォント情報** ⇒ **ルックアップ** ⇒ **GPOS タブ** ⇒ **プラス記号** を押して展開し、サブテーブルをダブルクリックします。

## 手動カーニング

もし「自動カーニング」の値を調整する必要がある場合は（現実に起こり得る話ですが）、そのときは、いくつかの方法で対応できます。

- 「**クラスを用いたカーニング**」のダイアログ・ウィンドウを利用します。
- 「**メトリック・ウィンドウ**」を利用します。
- **メトリクス** メニューの「カーニングペアの詳細」コマンドを利用します。

## こちらも参照してください

[Strategies for determining letter spacing](http://letterpunch.blogspot.com/2014/09/strategies-for-setting-letter-spacing-part-one.html)〔文字間隔決定のための戦略 2014.09.21〕（英語サイト）