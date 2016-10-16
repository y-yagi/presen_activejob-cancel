
## 補足

* Active Jobにおける"ジョブID"とは、Active Job内で発番しているIDの事
  * `SecureRandom.uuid`メソッドを使って発番している(UUID version 4）
  * 厳密には衝突の可能性がある
* それとは別に、queuing systemによってはqueuing system側でIDを発番している(`Sidekiq`、`DelayedJob`等)
