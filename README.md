# マルチモーダル情報を扱う世界モデル

## Ominicampusでの実験の回し方

Ominicampusの実験環境は利用上限が100時間までと決まっているため, 利用完了したらすぐにインスタンスを削除する必要があります.
`/mnt/shared` はAWS S3へマウントしているためここに保存したデータは永続化しますが, それ以外のデータはインスタンス削除とともに削除されてしまいます.

Ominicampusの利用が必要なとき(GPUが必要なとき)はJupiterHubにログイン後以下のコマンドを叩いてレポジトリをクローンしてください.
GitHubとの連携に必要なsshの設定を`/mnt/shared`からホームディレクトリにコピーしてくることができます.

```
$ cd ~
$ cp -r /mnt/shared/.ssh ~/
$ chmod 600 /home/admin/.ssh/id_rsa
$ git clone git@github.com:meltyyyyy/multimodal-world-model.git
```

## メンバー

ここにぞれぞれ自己紹介をどうぞ

