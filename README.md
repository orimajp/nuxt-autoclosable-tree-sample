# nuxt-autoclosable-tree-sample
ドキュメント管理アプリメニュー用ツリーコンポーネントテスト。

# 期待する動作
* アイテムをクリックすると下位階層が開き、下位以外の展開階層が閉じる
* 下位階層が開いているアイテムをクリックしても閉じない
* クリックするとアイテムIDが取得できる

# 実現方法
* 再帰的コンポーネント
* 下位階層を開く関数の再帰呼び出し

# 技術的な勘所
* 再帰的コンポーネントでは自コンポーネント名を`name`属性に指定する
* 開閉状態は親コンポーネントのデータで管理する
* 展開コンポーネントは開かれたコンポーネント階層のIDを配列で持つ
* 開閉操作は再帰的コンポーネントを呼ぶ親コンポーネントの関数で行う

# 実行方法
1. git clone
2. npm install
3. npm run dev

# 参考URL
* [Vue.js で Recursive にコンポーネントを呼び出して、階層が深いメニュー的なものを作る - Qiita](https://qiita.com/superyusuke/items/ef23435c93be3c23a5a7)
* [How to find a node in a tree with JavaScript - Stack Overflow](https://stackoverflow.com/questions/9133500/how-to-find-a-node-in-a-tree-with-javascript)
