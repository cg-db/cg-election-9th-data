# cg-election-9th-data
第9回総選挙・VAのデータです。

## データの見方
- data/general

第9回総選挙のデータです。ファイル名はYYYY-MM-DD-hh-mm-ssの形でネーミングされています。
データはcsvファイルです。次のようなデータになっています。

| アイドルID | アカウント数 | アカウント(only)数 | ツイート数 | いいね数 | リツイート数 |
| --- | --- | --- | --- | --- | --- |
| 72 | 29 | null | 46 | 127 | 16 |
| 144 | 17 | null | 23 | 44 | 6 |
| ︙ | ︙ | ︙ | ︙ | ︙ | ︙ |

※アカウント(only)数は最初のころ収集してなかったので最初のほうのデータはnullになっています。

ソートはされていないので各自でソートしてください。
- data/voice

第1回VAのデータです。仕様は総選挙のものと全く同じです。
- data/idol/[アイドル名]

ネーミング方式については上と同じですがこちらはjsonファイルになっています。仕様は以下の通りです。
```javascript
{
  // 総選挙でそのアイドルに投票したユーザーのプロフィールに記載されたアイドル
  "general_account_profile_idols" : {
    "アイドルID": 数字
  },
  // 上のVA版
  "voice_account_profile_idols": {
    "アイドルID": 数字
  }
  // 総選挙であるアイドルに投票したユーザーが他に投票したアイドル
  "general_other_voted_idols": {
    "アイドルID": 数字
  },
  // 上のVA版
  "voice_other_voted_idols": {
    "アイドルID": 数字
  }
}
```
