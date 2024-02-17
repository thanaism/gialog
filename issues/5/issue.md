---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/thanaism/gialog/issues/5/comments
created_at: '2024-02-05T16:44:27Z'
events_url: https://api.github.com/repos/thanaism/gialog/issues/5/events
html_url: https://github.com/thanaism/gialog/issues/5
id: 2119000462
labels: []
labels_url: https://api.github.com/repos/thanaism/gialog/issues/5/labels{/name}
locked: false
milestone: 
node_id: I_kwDOLOSKe85-TWGO
number: 5
performed_via_github_app: 
reactions:
  "+1": 0
  "-1": 0
  confused: 0
  eyes: 0
  heart: 0
  hooray: 0
  laugh: 0
  rocket: 0
  total_count: 0
  url: https://api.github.com/repos/thanaism/gialog/issues/5/reactions
repository_url: https://api.github.com/repos/thanaism/gialog
state: open
state_reason: 
timeline_url: https://api.github.com/repos/thanaism/gialog/issues/5/timeline
title: gialogの仕組みを簡単に調べる
updated_at: '2024-02-05T16:47:03Z'
url: https://api.github.com/repos/thanaism/gialog/issues/5
user:
  avatar_url: https://avatars.githubusercontent.com/u/62784012?v=4
  events_url: https://api.github.com/users/thanaism/events{/privacy}
  followers_url: https://api.github.com/users/thanaism/followers
  following_url: https://api.github.com/users/thanaism/following{/other_user}
  gists_url: https://api.github.com/users/thanaism/gists{/gist_id}
  gravatar_id: ''
  html_url: https://github.com/thanaism
  id: 62784012
  login: thanaism
  node_id: MDQ6VXNlcjYyNzg0MDEy
  organizations_url: https://api.github.com/users/thanaism/orgs
  received_events_url: https://api.github.com/users/thanaism/received_events
  repos_url: https://api.github.com/users/thanaism/repos
  site_admin: false
  starred_url: https://api.github.com/users/thanaism/starred{/owner}{/repo}
  subscriptions_url: https://api.github.com/users/thanaism/subscriptions
  type: User
  url: https://api.github.com/users/thanaism

---
## Markdownファイルは必要か？

もともとGatsbyでブログを作っていたのだけど、upgrageを怠っているうちに開発サーバーが立ち上がらなくなった。

去年からM1 Macを使い始めたのもあり、おそらくGatsby本体のバージョンを上げたりなんだりしないといけなさそうなのだ。

Gatsbyの良い点として、可搬性の高いmdファイルが直接手元に残るというのがある。

一方で、いちいちエディタを立ち上げてする編集は面倒だ。

ブラウザで完結しないので、出先でちょこっとメモ書き程度の記事をpublishするというのもやりにくい。

## Issueの可搬性はどうなのか

gialogのコードを見ると、gatsbyの内部でもおそらく使われているremarkを活用してIssueをレンダリング可能な形式に変換している。

ということは元データとなるmarkdownがあるはずだが、これは[gialog-sync](https://github.com/r7kamura/gialog-sync)というGitHub Actions上で生成されているようだ。

gialog-syncのリポジトリをざっと読むと、rubyで書かれていて、GitHub上のEventを受け取り、そのcontentをパースして特定フォルダに出力するといった内容だった。

Actionsビルド時に一時的に使われているだけっぽいので、そのままだと直接取り出すのは面倒そうだが、工夫すれば不可能ではなさそうだ。

可搬性は若干落ちる一方で、GitHub Issueの編集画面を使って記事を投稿できるという手軽さは非常によいと感じる。

個人ブログにも大した記事は残っていないし、めぼしい記事だけこっちに移行して、ドメイン挿げ替えてもいいかなーという気持ちになっている。

## Honoってtsxが動くんですね

話は少し逸れるが、gialogでホストされるページ自体はNext.jsのSSGで動いている。

このSSGをHonoのSSGに置き換えるという記事を見かけた。

https://zenn.dev/razokulover/articles/9818ef632f677f

そこで初めて知ったのだが、Honoでtsxを使ってコンポーネントを作り、配信できるようだ。

Cloudflareをまだちゃんと使ったことがないので、いずれHonoとセットで挑戦したい。