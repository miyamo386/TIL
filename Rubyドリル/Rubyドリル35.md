# Rubyドリル35（10の倍数からの差が2以内であるかを判別するプログラム）
### 自己解答
```ruby
def near_ten(num)
  if 
    puts "True"
  else
    puts "False"
  end
end

near_ten(12)
```

### 模範解答
```ruby
def near_ten(num)
  quotient = num % 10
  if quotient  <= 2 || quotient >= 8
    puts "True"
  else
    puts "False"
  end
end
```

### 学んだこと
- 初めに、整数を余剰計算した値を変数に代入します。
- 余剰計算した値が２以下かつ８以下であるかを条件式を記述する。
