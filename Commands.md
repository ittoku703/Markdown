# Command各種

### ffmpeg

> mp4 -> mp3

`ffmpeg -i hoge.mp4 -acodec libmp3lame -ab 256k foo.mp3`

> 音量を上げる

`ffmpeg -i hoge.mp4 -af "volume=20dB" foo.mp3`

> 動画切り出し

`ffmpeg -ss starttime -i hoge1.mp4 -t endtime hoge2.mp4`

### youtube-dl

> 音声のみ抽出

`youtube-dl -x "URL"`

### npm

> npmをアップグレード

`npm install -g npm@latest`

### tree

> 特定のディレクトリを無視

`tree -I node_modules`

### svn

> github.comのソースコードを一部だけクローン
>
> URLの`tree/master`の部分を`trunk`に置き換えること

`svn checkout https://github.com/XXX/YYY/trunk/ZZZ`

### nバイトのファイルを生成

> bs x cバイトのfilenameを生成する

`dd if=/dev/zero of=filename bs=n count=c`

### Curlコマンド

> 進捗状況やエラーを表示しない

`curl -s -o Path URL`

> ただし、エラーは表示したい

`curl -sS -o Path URL`

> SSL接続の証明書エラーをスキップ

`curl -k URL`

> URLのファイル名でダウンロード

`curl -O URL/save.html`

> リダイレクト有効

`curl -L URL`

> HTTPレスポンスヘッダー取得

`curl -I URL`

### Git

> untracked filesを消去

`git clean -df`

> addをリセット

`git reset HEAD .`

> commitをリセット

`git reset --soft HEAD^`

> 1回目のcommitをリセット

`git update-ref -d HEAD`

> push前に戻す(logに残る)

`git revert [<commit>]`

> 設定を確認

`git config -l`
`git config --global -l`

> file_nameを変更してもを無視

`git update-index --assume-unchanged file_name`