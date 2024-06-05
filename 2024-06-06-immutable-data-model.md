title: イミュータブルデータモデル、論理削除
==========
date: 2024-06-06 00:20
tags: []
categories: []
- - -

# 雑記
- RDBMSだと追記型のWALとやることがかぶるのでアプリケーションレベルでそれをやるとかぶってしまってスジが良くないという趣旨の意見を見かけた
- 過去の状態に対する参照、復元可能性を考慮した結果[too much]なことも当然あると思う
- イミュータブルデータモデリング[* 風]になっている、履歴を表すテーブルが更新日時のカラムを持っており、「正しい履歴」であるという保証のないデータになっているという悪夢を見た。
- アプリケーションのコード見りゃいいじゃん？
  - 過去のコードも含め「正しい履歴」を反映する実装になっているかを確認するの、メチャクチャ大変。

# 参考
- [増田亨さんによる「設計の考え方とやり方」勉強会 - connpass](https://asken.connpass.com/event/254709/ )
- [/kawasima/イミュータブルデータモデル](https://scrapbox.io/kawasima/%E3%82%A4%E3%83%9F%E3%83%A5%E3%83%BC%E3%82%BF%E3%83%96%E3%83%AB%E3%83%87%E3%83%BC%E3%82%BF%E3%83%A2%E3%83%87%E3%83%AB)
- [イミュータブルデータモデル(入門編) | PPT](https://www.slideshare.net/kawasima/ss-40471672 )
- [イミュータブルデータモデル(世代編) | PPT](https://www.slideshare.net/kawasima/ss-44958468)
- [イミュータブルデータモデルの極意 | PPT](https://www.slideshare.net/kawasima/ss-250716400)
- とりあえず削除フラグ、論理削除
  - [http://blog.kazuhooku.com/2015/03/blog-post_26.html](論理削除はなぜ「筋が悪い」か)
  - [SQLアンチパターン 幻の第26章「とりあえず削除フラグ」 | PPT](https://www.slideshare.net/t_wada/ronsakucasual)
  - [論理削除が云々について - mike-neckのブログ](https://mike-neck.hatenadiary.com/entry/2015/03/24/231422)
