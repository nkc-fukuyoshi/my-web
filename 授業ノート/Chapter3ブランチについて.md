## Chapter3ブランチについて

- ブランチ(枝)を利用することによって、複数の状態をGit上で管理することができる。
  
  [例]
  状態①　新機能を開発している状態
  状態②　既存のバグを修正したり、コードの微調整をしている状態
  状態①を「newブランチ」、状態②を「master」ブランチに持たせることで、それぞれの状態を分けて管理して開発を進めれる。
  
  ⇒ソースコードが分けて考えれるため、混乱を防げる。　

### 分けたブランチをマージする

- 状態を分けて開発を進めた結果、最終的は状態①の「new」ブランチは 状態②の「master」に合流させることが多い

- ブランチの合流　＝　Gitでは<mark>マージ</mark>といい、Gitが自動的に「new」ブランチの変更点を「master」ブランチに反映してコミットしてくれる

- 2つのブランチをマージする際に片方のブランチしか変更点がない場合は「マージコミット：**Merge branch 'ブランチ名'**」は作られない。このようなマージを「ファストフォワード(早送り)」という。

### ブランチをマージする際の衝突(コンフリクト)

- ブランチを分けて開発を進めていくと、ブランチをマージする際に同じファイル、同じ個所を修正している場合に<u>Gitが自動でマージできなかった</u>ため「**競合、衝突、コンフリクト**」ということが起こる。

- この状態になった際には、
  ・相手の内容で解決する
  ・自分の内容で解決する
  ・手作業でファイルを修正して解決する
  の中からチームで相談して解決する必要がある

- コンフリクトは極力起こらないほうが良い。(間違いや手間の元)
  コンフリクトしないようにするには、<u>ブランチを作りすぎない</u>、<u>複数のブランチでいろいろな作業をしない</u>ことがポイント。


