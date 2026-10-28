# Gemini Write

文章の執筆・リライト・校正をGeminiに任せる、Codex／Claude Code向けスキルです。Markdownなどのテキストファイルを扱います。原稿のコピーを編集し、結果を確認してから元のファイルへ反映します。

## セットアップ

### 1. Antigravity CLIをインストールする

macOS／Linux：

```bash
curl -fsSL https://antigravity.google/cli/install.sh | bash
```

Windows（PowerShell）：

```powershell
irm https://antigravity.google/cli/install.ps1 | iex
```

インストール後はターミナルを開き直し、次を実行します。

```bash
agy
```

画面の案内に従ってログインし、`/exit`で終了します。次のコマンドでモデル一覧が表示されれば準備完了です。

```bash
agy models
```

詳しくは[公式のインストール手順](https://antigravity.google/docs/getting-started#download-and-install)と[ログイン方法](https://antigravity.google/docs/install?tab=cli)を参照してください。

### 2. このスキルをインストールする

この導入コマンドにはNode.js 22.20以降とnpmが必要です。

```bash
npx skills add laiso/gemini-write --skill gemini-write -g
```

表示される案内に従って、利用するエージェントを選択します。

## 使い方

Codex：

```text
$gemini-write draft.mdを、内容と口調を保ったまま読みやすくして
```

Claude Code：

```text
/gemini-write draft.mdの誤字と文法だけ直して
```

モデルを指定しない場合は、利用可能な最新のGemini Flash（Medium）を選びます。処理に失敗した場合は反映せず、理由を報告します。
