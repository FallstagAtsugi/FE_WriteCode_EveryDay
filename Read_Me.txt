◆Reactチュートリアル
https://ja.reactjs.org/tutorial/tutorial.html

◆React_hocks 概要Q
https://mantine.dev/

◆HTML to JSX
https://transform.tools/html-to-jsx


◆npm ライブラリ
https://www.npmjs.com/


npmはパッケージ管理(NodePackageManager)
npxはパッケージ実行(NodePackageExecuter)

npm経由でコマンドを実行する場合は
package.jsonのscriptに実行コマンドを追加する必要があります。
そのため、実行コマンド自体がバージョン管理に値する場合はnpmコマンドを利用します。

それ以外の場合は基本的にnpxを利用すれば問題ありません。




Q.ts-nodeできない
https://qiita.com/testMenta339/items/3448bc244ca5e29e7e96


Q.typeScriptって？？
https://qiita.com/testMenta339/items/6ba9efdaeae23f5a8124


設計：BEM
最近フロントエンド界隈で、『BEM』という言葉を見かけることが増えてきました。BEMとは、Block、Element、Modifierの略語です。Webサイトのコンポーネント化のためのフロントエンド設計方法のひとつで、厳格なclass名の命名ルールが特徴的な手法
https://www.codegrid.net/articles/bem-basic-1



BEMは、Block、Element、Modifierという3つの概念だけ理解してしまえば、あとはclass名の命名ルールに則って記述するだけの単純な方法です。


使わないデメリット：
パーツを別の場所に流用すると表示が崩れる
パーツ単体で独立しておらず、別のパーツに依存したスタイル指定になっていると、パーツを別の場所に移動した場合に、表示が崩れることがあります。


BEMが解決を目指すポイント
１．長期間メンテナンスできる設計で、ファーストバージョンの開発をすばやく
２．チームのスケーラビリティ（BEMさえ理解していれば短期間で即戦力　＆　時間がたってもチームが変わってもメンテナンス可能な状態を維持できる）
３．コードの再利用性(パーツを完全に独立させることができれば、コードの再利用が容易に)



BEMで設計する目的
BEMはもともと、プロジェクトの成長にともなって、既存のページが変化していくことを前提として考え出されました。また、変更がある場合は、その対応コストをできるだけ低減することを目的としています。
BEMは多くの人がかかわり、長く運用されるプロジェクトに、特に向いていると言えるでしょう。キャンペーンページなどの期間限定でしか使われないサイトでも、開発をすばやく行えるため、BEMを利用する価値はあるでしょう。



◆Next.jsでSSR、SSGの方法
https://qiita.com/testMenta339/items/880690319f8babe6cb39


◆React 初心者の難問、カスタムフック（Custom Hook）
https://zenn.dev/luvmini511/articles/df410f137d1e21




Webpackとは？
Webpack=複数のファイルを１つにまとめる
※バンドルするともいう（ぎゅっと１つにまとめる）

HTMLのScriptタグは、何回もHTTP通信しないといけない
＝パフォーマンスが悪い)
CSSや画像ファイルもまとめられる
※最近は使われないが、知ってて損はない

【５分でなんとなく理解！】Webpack入門
https://qiita.com/Shagamii/items/698a67bab0cd5eefcb4f



◆state
state には、そのコンポーネント固有のデータが含まれており、これは時間の経過とともに変化する可能性があります。state はユーザ定義のものであり、プレーンな JavaScript オブジェクトでなければなりません。
コンポーネントが何かを「覚える」ためには、state というものを使います。

よく使われる表現
親コンポーネントから子コンポーネントに「props を渡す」こと





コンポーネントは props（“properties” の略）と呼ばれるパラメータを受け取り、render メソッドを通じて、表示するビューの階層構造を返します。




render メソッドが返すのはあなたが画面上に表示したいものの説明書きです。React はその説明書きを受け取って画面に描画します。

それぞれの React のコンポーネントはカプセル化されており独立して動作します。これにより単純なコンポーネントから複雑な UI を作成することができます。









// function
function test(x) {
  return x + 1;
}
 
// arrow function  引数なし (かっこがいる)
const test = () => 1; // 出力の式が一行の場合はreturnは不要
 
// arrow function 引数1つ (かっこいらない)
const test = x => x + 1;
 
// arrow function 引数2つ以上 (かっこいる)
const test = (x, y) => x + y + 1;

変数に関数をあたえてるかんじってことか。
() => {} の形で書く
意識して何度も書いているうちに、

function書かなくていいのは楽かも
()とか{}とかreturn とかはしょっていいのは楽かも
と思えるようになってきたので、
ちょっとずつ使いながら慣れていくといいのかなと思います。





// オブジェクトの配列
const data = [
  { id: 101, name: 'iPhone' },
  { id: 102, name: 'Android' },
  { id: 103, name: 'Other' },
];

// IDだけ出力する (functionの場合) mapは配列を取得する関数
const ids = data.map(function(row) {
  return row.id;
});
console.log(ids);  // => [101, 102, 103]

// arrow function
const ids = data.map(row => row.id); // 引数 => 返り値 という書き方になる
console.log(ids);  // => [101, 102, 103]


結論を言いますと、アロー関数式で宣言された関数は、宣言された時点で、thisを確定（＝束縛）させてしまうのです。





『Babel(バベル)』などを使う事で
旧来の『JavaScript』に変換ができるので、
実際の現場で使うときはもれなく『Babel』などもセットに
(これがないとやってられないレベルで「Babel」は必須)







constructor を持つ React のクラスコンポーネントでは、すべてコンストラクタを super(props) の呼び出しから始めるべきです。




ORM
現時点では、[TypeORM]がよいと思っています([TypeScript]との相性/完成度の高さ/GitHubのスター数などの観点から)
ORM は prisma 一強。現時点でまだ prisma migrate が experimental だが、それでも兎にも角にも prisma の採用が多い。

React の UI Framework は Chakra の採用が増えている

prizmaにしようかなぁ
https://zenn.dev/tatsurom/articles/prisma-tutorial-from-scratch


Next.js から Prisma ORM を利用する
https://zenn.dev/mizchi/articles/1c35fdcc77065c02f631




Reactチュートリアル理解編：
https://qiita.com/testMenta339/items/65263102c5f82c69e7c7
https://qiita.com/testMenta339/items/510afed8ebd44d62af98
https://qiita.com/testMenta339/items/276a0702bb4192a5606f
https://qiita.com/testMenta339/items/1cb28ae66c45bc48a3fc
https://qiita.com/testMenta339/items/f3011012ed11761e3c7e
https://qiita.com/testMenta339/items/097f536c56dc151725f6




2.チャクラUIどうにゅう  ✖→推奨Material UI
Googleが公開している「マテリアルデザイン」というガイドラインに従ってデザインされた、Material-UIというライブラリに
Google社が自社のサービスに統一的なデザインを与えるために作成した、デザインのガイドラインであり、仕様書です。

　プログラマーも読みやすいように配慮されており、「こういった場合はマージンを16pxにして、こちらの場合では72pxにする」や「こういった部品を作る際は高さを56pxにする」といった具合で、定性的な基準よりも定量的な基準を重視した仕様書となってい
デザインはGoogle一択。自分の価値観ではなうデファクトに従う（シンプルisBest
https://codezine.jp/article/detail/14322?p=2

マテリアルデザインについて
https://hnavi.co.jp/knowledge/blog/material-design/

https://qiita.com/testMenta339/items/880690319f8babe6cb39
3.typescprit導入
https://qiita.com/testMenta339/items/3448bc244ca5e29e7e96
https://qiita.com/testMenta339/items/6ba9efdaeae23f5a8124






ESLint, Prettier については個人的には推奨と言いたいところ．やはり静的コード解析は，人がリソースを割くべきじゃないことですので自動化したい．ただ，ESLint が解析・チェック及び修正まで行ってくれるので Prettier は不要で ESLint だけで良いよね，という人もいますしそれも理解します．




推奨
React.js（以下，React）
やれるならやったほうが良い
Angular
Vue.js（以下，Vue）
こちらもほぼ同意で，React とそのラッパーである Next.js（以下，Next） を推奨します．「現代のモダンなフロントエンドのフレームワークは何？」と聞かれたら真っ先に Next と答えるくらいには，Next は素晴らしいと私は感じているフレームワークとなります．




Testing your Apps
推奨
Jest (for unit test)
react-testing-library (for unitiIntegration test)
Enzyme (for unitiIntegration test)
Cypress (for E2E)

そして推奨ライブラリも完全同意です．今はこれらのライブラリを使えばだいたいフロントエンドのテストはカバーできると言って差し支えないと思います．私自身すべてのライブラリを一度は触っておりますが，Jest と Cypress が多めで，残り二つは軽く触ったかあるいは途中でジョインしたプロジェクトですでに使われており，そのテストコードを眺めた程度のため，ググった知識しかないです（自身の不勉強さが現れるなぁ…🙇）．


個人的にはとりあえずフロントエンドのユニットテストを初めて書く方には Jest から入門することをおすすめします．モダンなテスティングライブラリとして豊富な機能を備えており，かつドキュメント・サンプルコードも充実しているため，この子でもとりあえずは十分にアプリケーションの自動ユニットテストの環境は整えられると思います．欲しい機能としては

・高速に実行
・モッキング
・カバレッジ
・アサーション
・スナップショット
・スパイ

だいたいこのあたりで，Jest はすべて備わっております．また対応しているライブラリも React, Vue, Angular, Node.js と幅広く，突っ込んだ使い方をしない限りはとても使いやすい子ですね．




Type Chekcers
推奨
TypeScript



その上で推奨に挙がっている TypeScript ですが，Microsoft 社が生み出した最高傑作の一つと言っても良い，皆さんご存知のオープンソースのプログラミング言語です．個人的にはそこまで好きではないですがフロントエンドの開発において十分に恩恵を受けていますし，世界的にも今や フロントエンドの型チェックのデファクトスタンダード と言っても過言ではないでしょう．今後も TypeScript は進化していくでしょうしこの流れは当分続くと思っています．したがって，今型チェックのツールを入れるのであれば TypeScript で間違いないかなと．



TypeScript を私はお勧めします．理由としましては，

現代のフロントエンドの開発におけるエディタも VSCode が主流になってきている
VSCode も Microsoft 社が開発しており，TypeScript との相性がかなり良い
TypeScript の方が利用実績も多い（はず）
ググラビリティが高い（ググったときの雑音が Flow は多い）
以上，TypeScript で幸せなフロントエンド開発を！




Server Side Rendering(SSR)
推奨
React.js/Next.js



そもそも今は SSR やる？とか必要？という議論が起きているくらいですし，今後必要性は薄くなってくることは間違いないと思います．というのも Google bot が進化してきており，今後 SPA の Web アプリでもしっかり SEO が効くようになる未来が来るでしょう．もちろん動画投稿サービスや SNS サービスなど 更新頻度が高い Web アプリ であれば十分に検討に上がると思います．

この手の話は色んな所で議論が活発に行われておりますし，ググってみると（この後言及しますが）SPA / SSR / SSG / ISR の比較記事がたくさん書かれておりますので，そちらを見ていただくほうが良いと思います．

その上で個人的には推奨に挙がっている React.js/Next.js が最もおすすめのフレームワークですね．そもそも（二回目） 現代では Next.js に Pre-rendering という機能が組み込まれており，この概念の議論も生まれております．これは簡単に言うとページ毎に SSR/SSG を選択できるというものです．選択肢が増えるのはありがたいですねぇ👍詳しくは下記リンクより公式サイトをご一読ください．






思ったより自分がフロントエンド技術について触っていないものばかりだったことを改めて認識しましたね．ついつい UI ライブラリやフレームワークばかり目が行きがちですが， フロントエンドの技術全体を見渡すと優先的にキャッチアップすべき技術は他に沢山あります ．

やはり技術者としては作ることもそうですが，

作ったものがしっかりエンドユーザの手に届くこと
ビジネスを加速させるための技術的ソリューションの提供
当たり前にシステムやアプリが動作するサポートをすること
に注力することが肝要ですので，来年も技術のプロとしての自覚とともに何を学んで行くのかは吟味しつつ選んでいきたいと思います．