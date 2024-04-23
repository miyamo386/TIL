# Rubyドリル
### 自己解答
```ruby
puts "[0]:カロリーを表示する、[1]:終了する"
calorie = gets.to_i

while 条件式 do
  処理するアクション
end
```

### 模範解答
```ruby
while true do
  puts "[0]:カロリーを表示する"
  puts "[1]:終了する"
  input = gets.to_i

  if input == 0
    puts "500kcal"
  elsif input == 1
    exit
  end
end
```

### 学んだこと
- whileとは、指定した条件式がtureの間処理を繰り返すRubyの構文です。
