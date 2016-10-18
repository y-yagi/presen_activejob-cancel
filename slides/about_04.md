
## `activejob-cancel`

* `cancel`メソッドはActive Jobが発番しているジョブIDを使用するようにしている
* Active Jobが発番しているIDではなく、queuing system(`Sidekiq`、`DelayedJob`)が返すIDを使用したい場合は、`cancel_by`メソッドを使う必要がある

```ruby
HelloJob.cancel_by(provider_job_id: job.provider_job_id)
```
