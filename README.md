# githubpages_relatepath_test

## description
- Github pagesでかんたんにリソースを複数公開したいケースがある。（テスト結果をCIなどで実行し結果を自動公開するなど。)
- Github Pages + JavaScript + Github APIを使うことでかんたんに実現できました
- 公開ページは[こちら](https://kashiwaguma-hiro.github.io/gh_pages_relpath_test/)

## strategy

雑にディレクトリをコミットしてpushしたら Github Pagesに公開されるようになってほしいのでまずはググってみた.  
みんな大好きstackoverflowでまさに[同じことをしようとしてる人](https://stackoverflow.com/questions/39048654/how-to-enable-directory-indexing-on-github-pages) がいたのでパクってみました.  
ディレクトリ構成は以下の様になってます.  

```
├── README.md
└── docs                   # GithubPagesで公開するディレクトリ
    ├── index.html         # GithubPagesのIndexページ. JavaScript＋GithubAPIを使ってreports配下を動的にリンク化している.
    └── reports            # 増やしていくコンテンツの配置ディレクトリ. この下にディレクトリを作ってコミットしてくだけで、公開されていく.
        ├── 20200528
        │   └── index.html
        └── 20200529
            └── index.html
```