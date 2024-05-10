# Rubyドリル
### 自己解答
```ruby
now = Time.new
puts now"現在は西暦#{now.year}年#{now.month}月#{now.day}日
#{}です"
```

### 模範解答
```ruby
now = Time.new
puts "現在は西暦#{now.year}年#{now.month}月#{now.day}日"
week = ["日","月","火","水","木","金","土"]
puts week[now.wday] + '曜日です'
```

### 学んだこと
- %w記法とは、配列作成時に[ ](ブラケット)や” “(ダブルクォーテーション)を省略できるRubyの書き方です。
