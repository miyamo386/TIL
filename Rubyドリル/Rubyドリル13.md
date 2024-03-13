# Rubyドリル１３
### 自己解答
```ruby
ruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]


fruits_price.each do |key, value|
  puts "#{key}の合計金額は#{value}です"
end
```

### 模範解答
```ruby
fruits_price = [["apple", [200, 250, 220]], ["orange", [100, 120, 80]], ["melon", [1200, 1500]]]

fruits_price.each do |fruit|
  sum = 0
  fruit[1].each do |price|
    sum += price
  end
  puts "#{fruit[0]}の合計金額は#{sum}円です"
end
```

### 学んだこと
- eachとは、配列やハッシュの複数ある値に対して、値の数だけ繰り返し処理を行うメソッドです。
- 変数sumに０を代入してから、配列の１番目である金額を自己代入を繰り返します。
