# Rubyドリル28（ポイント付与を計算するプログラム）
### 自己解答
```ruby
def calculate_points(amount, is_birthday)
  if amount <= 999 && is_birthday == false
    puts "ポイントは#{}点です"
  elsif amount >= 1000 && is_birthday == false
    puts "ポイントは#{}点です"
  else 
    puts "ポイントは#{}点です"
  end

end

calculate_points(500, false)
calculate_points(2000, false)
calculate_points(3000, true)
```

### 模範解答
```ruby
def calculate_points(amount, is_birthday)
  if amount <= 999
    point = amount * 0.03
  else
    point = amount * 0.05
  end
  if is_birthday
    point = point * 5
  end
  puts "ポイントは#{point.floor}点です"
end
```

### 学んだこと
- 購入金額が999円以下か、購入金額が1000円以上なのかで、if文で言い換えると「購入金額が999円以下か、それ以外」となります。
- floorとは、小数点以下を切り捨てるRubyのメソッドです。
