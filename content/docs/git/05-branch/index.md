---
title: ブランチ
type: docs
prev: docs/git/04-stage-co
next: docs/git/06-remote
weight: 5
---

## ブランチとは

```mermaid
gitGraph

commit
commit
branch dev
commit
```

Git は複数人での開発を想定しています。複数人がそれぞれ別のコミットをすると、リモートに上げる際に干渉してしまいます。[^commit-remote]

```mermaid
gitGraph

commit id: "a"
commit id: "b"
branch main/human1
branch main/human2
checkout main/human1
commit id: "c1"
checkout main/human2
commit id: "c2"
```

そこで、**ブランチ**という機能が重要になります。

[^commit-remote]: そのまま開発することもできますが、手動で分離したほうが後から見た際にわかりやすいです

**ブランチ** (枝) を作成することによって、
