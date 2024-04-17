# Rubyドリル４６（運勢の表示プログラム）
### 自己解答
```ruby
def today_fortune

  num = rand(1232)

end
```

### 模範解答
```ruby
def result_of_uranai(birthday)
  results = ["凶", "中吉", "吉", "大吉"].shuffle
  num = birthday * rand(10) % 4
  puts "今日のあなたの運勢は、#{results[num]}だよ！"
end

puts "誕生日を入力してください！"

birthday = gets.to_i
result_of_uranai(birthday)
```

### 学んだこと
- randとは、指定された数値の範囲内でランダムに生成するメソッドです。
- shuffleとは、配列の要素をシャッフルし、結果を配列で返すメソッドです。
