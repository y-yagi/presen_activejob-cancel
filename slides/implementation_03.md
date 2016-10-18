## とすると性能的にどうなのか

* `LREM`の計算時間はO(N) なので大量のjobがあるようなシステムだとつらい
  * 検索処理も同様
* これは`sidekiq`使ってても同じ
* `sidekiq pro`だと find処理が早いらしい
  * https://github.com/mperham/sidekiq/blob/72fe3289eabb5e4b01165d3e4e61b1ee08869223/lib/sidekiq/api.rb#L253..L259
  * 別実装があるのか?
