# gemini-discord-bot

これは簡易的なDiscordチャットボットです。Geminiとの会話機能が実装されています。
@konoka-iori が個人的に使用するために作成されました。主に小規模なDiscordサーバーでの利用を想定しています。
Gemini APIを使ったDiscordのチャットボット作ってみたいよという人はぜひ参考にしてみてくださいね。

# コマンド一覧(機能一覧)

- `/about`: BOTの説明を表示します。
- `/chat`: Geminiとチャットができます。一問一答方式で、会話履歴はBOT側で保存されません。
- `Gemini replies to message`: すでに送信されているメッセージを選択してこのコマンドを使用すると、選択されたメッセージにBOTが返信します。一問一答形式で、会話はBOT側で保存されません。

# 使い方

1. このリポジトリをクローンします。
2. `.env.sample` を `.env` にリネームします。
3. `.env` の `DISCORD_TOKEN` にDiscordのBOTのトークンを入力します。
4. `.env` の `GEMINI_API_KEY` にGeminiのAPI Keyを入力します。
5. `.env` の `DISCORD_SERVER_ID` にBOTを使用したいDiscordサーバーのIDを入力します。
6. `pipenv install` を実行します。（pipenvを使わない場合は `pip install -r Requirements.txt` など。）
7. `pipenv run bot.py` を実行します。（pipenvを使わない場合は `python bot.py` など。）
8. コマンドラインに `COMMAND SYNCED` と表示され、BOTがオンラインになったらDiscordで `/about` と入力してみましょう！( `/chat` も動くはず！)

## Discordの権限設定

このBOTを正常に動作させるには以下の権限が必須です。

SCOPES: bot

BOT PERMISSIONS:

- Send Messages
- Send Messages in Threads (スレッド内でもBOTを利用したい場合は必須)
- Embed Links
- Read Message History

# ブランチ命名規則

- `main`: 動作確認済みのブランチです。
- `develop`: 開発用のブランチです。こちらは動作確認が行われていません。
- `add/`: New Featureブランチです。新機能などの追加に使用します。`develop` から派生。
- `improvement/`: Improvement用ブランチです。既存の機能の改善に使用します。`develop` から派生。

# 注意事項

- このBOTは個人利用を想定して作成されています。
- このBOTはDiscordで動くものです。DiscordのアカウントやBOTの作成方法、利用規約、サーバーの作成方法などについては公式サイト等を確認してください。
- このBOTはGemini APIを利用しています。Geminiの概要、利用規約、APIの利用方法・API Keyの取得などについては公式サイト等を確認してください。
- 会話の内容が @konoka-iori に送信されることはありませんが、Gemini側で保存されて学習等に利用される場合があります。詳細は公式サイトを確認してください。
- このプロジェクトはみんな大好きMITライセンスです。BOTを使うときは自己責任で、かつこのリポジトリのURLを明記してください。詳細はLICENSEをご覧ください。
- 不具合報告、機能追加要望などはIssueください。Pull Requestも歓迎です！
