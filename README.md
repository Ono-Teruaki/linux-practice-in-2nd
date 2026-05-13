# linux-practice-in-2nd

『Linuxのしくみ 増補改訂版』(武内覚 著) の学習用リポジトリ。

書籍の実験コードを取り込み、章ごとに学習サマリーを書き、Claude Code の skill で定期的にレビューを受ける構成。

## 出典

実験コードは公式リポジトリ [satoru-takeuchi/linux-in-practice-2nd](https://github.com/satoru-takeuchi/linux-in-practice-2nd) (MIT License) から取り込んでいる。詳細は `LICENSE` 参照。

## 構成

```
.
├── 01-operating-system-overview/
│   ├── (書籍の実験コード)
│   ├── summary.md       # この章の学習ノート
│   └── review.md        # /review-summary によるレビュー履歴
├── 02-process-management-1/
│   ├── ...
├── ...
├── 12-cgroups/
│   ├── ...
├── .claude/
│   └── skills/
│       └── review-summary/
│           └── SKILL.md  # レビュー skill 本体
└── README.md
```

書籍の章番号と一致 (6章と11章はコード無し)。

## 運用フロー

1. 該当章の `summary.md` を編集して学習内容を追記
2. Claude Code 上でリポジトリを開き、章ディレクトリで `/review-summary` を実行 (または `/review-summary 03` のように章を指定)
3. 該当章の `review.md` の末尾に新しいレビューが追記される
4. review を読んで自分で summary.md を直す (skill は summary.md を書き換えない設計)
5. `git push`

## 実験環境

実験コードは Linux (Ubuntu 20.04 前提) でのみ動作する。macOS では動かないので Lima/VM 等の Ubuntu 環境で実行する。詳細は上流リポジトリの README 参照。
