# Gemini Write

文章の執筆・リライト・校正をGeminiに委譲する、Codex／Claude Code向けスキルです。原稿の作業用コピーを編集し、実行結果と競合を確認してから反映します。対象はMarkdownなどのUTF-8テキストです。

## インストール

インストールにはNode.js 22.20以降とnpm、利用にはログイン済みのAntigravity CLI（`agy`）が必要です。

```bash
npx skills add laiso/gemini-write --skill gemini-write -g
```

表示される案内に従って利用するエージェントを選択します。特定のエージェントへ直接導入する場合：

```bash
# Codex
npx skills add laiso/gemini-write --skill gemini-write -g -a codex

# Claude Code
npx skills add laiso/gemini-write --skill gemini-write -g -a claude-code
```

## 使い方

Codex：

```text
$gemini-write draft.mdを、内容と口調を保ったまま読みやすくして
```

Claude Code：

```text
/gemini-write draft.mdの誤字と文法だけ直して
```

`agy` のモデル一覧から指定したモデルを使用します。指定がなければ、利用可能な最新のGemini Flash（Medium）を選びます。処理に失敗した場合は反映せず、理由を報告します。
