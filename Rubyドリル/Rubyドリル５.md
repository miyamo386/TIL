# Rubyドリル５
### 自己解答
```ruby
def calculate_price_with_tax(price)
  tax = 0.1
  return price + price * tax
end

price = 300
result = calculate_price_with_tax(price)
puts result
```

### 正解
```ruby
price = 300

def calculate_price_with_tax(price)
  tax = 0.1
  return price + price * tax
end

calculate_price_with_tax(price)
```

### 学んだこと
- スコープとは、定義した変数が使える範囲の事で、メソッド内の変数は外では使えず、反対にメソッドが外の変数を使用できない。
- 引数とは、メソッドに入れる（渡す）値のこと。
- 戻り値とは、メソッドで処理され変数から出てくる値のこと。
