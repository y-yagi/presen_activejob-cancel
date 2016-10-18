
## `activejob-cancel`

* キャンセル用(`cancel`)のメソッドをJob Classに追加している
  * クラスメソッドインスタントメソッド両方追加している

```ruby
# app/jobs/hello_job.rb
class HelloJob < ActiveJob::Base
  def perform
  end
end
```

```ruby
job = HelloJob.perform_later
job.cancel
```

or

```ruby
job = HelloJob.perform_later
HelloJob.cancel(job.job_id)
```

