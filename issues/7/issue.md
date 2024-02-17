---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/thanaism/gialog/issues/7/comments
created_at: '2024-02-05T16:55:08Z'
events_url: https://api.github.com/repos/thanaism/gialog/issues/7/events
html_url: https://github.com/thanaism/gialog/issues/7
id: 2119021373
labels: []
labels_url: https://api.github.com/repos/thanaism/gialog/issues/7/labels{/name}
locked: false
milestone: 
node_id: I_kwDOLOSKe85-TbM9
number: 7
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
  url: https://api.github.com/repos/thanaism/gialog/issues/7/reactions
repository_url: https://api.github.com/repos/thanaism/gialog
state: open
state_reason: 
timeline_url: https://api.github.com/repos/thanaism/gialog/issues/7/timeline
title: コードブロックの表示をチェックする
updated_at: '2024-02-05T16:55:08Z'
url: https://api.github.com/repos/thanaism/gialog/issues/7
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
gialog（dialogをもじっているので、ジャイアログと呼ぶのが正しいのだろうか）はNext.jsで書かれているので、気になったら自分でスタイルを当て直すなりすればいいのだが。

もはや、そういうのも面倒なのでデフォルト表示のまま何がどう表示されるのか調べていきたい。特にコードブロック。

```ts
export const codeBlock = () => {
  const foo = "FOOOOOOO";
  return foo;
};
```

次に引用。

> こんな感じで引用をしてみましたが、いかがでしょう？

Xのポストのリンク。

https://x.com/okinawa__noodle/status/1754541465173467343?s=20

Xのポストの埋め込みHTMLも。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">gialogというのを導入した（GitHub Issueをブログ形式にしてくれる）<br><br>今後、雑記はこれに書こうかな。<a href="https://t.co/D1H6uNHs23">https://t.co/D1H6uNHs23</a></p>&mdash; タナイ (@okinawa__noodle) <a href="https://twitter.com/okinawa__noodle/status/1754541465173467343?ref_src=twsrc%5Etfw">February 5, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

当然ながらscriptタグは動かないだろうから、この部分は本体でなんとかしないといけなさそうだなあ。