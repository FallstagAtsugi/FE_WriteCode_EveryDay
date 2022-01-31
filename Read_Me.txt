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