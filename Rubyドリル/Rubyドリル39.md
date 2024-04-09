# Rubyドリル３９（条件演算子）
### 自己解答
```ruby
def near_ten(num)
  quotient = num % 10
  if quotient  <= 2
    puts "True"
  else
    puts "10の倍数との差は#{}です"
  end
end

near_ten(117)
near_ten(123)
```

### 模範解答
```ruby
def near_ten(num)
  total = (num/100) + (num/10 % 10) + (num % 10)
  remainder = total % 10
  if remainder <= 2 || remainder >= 8
    puts "True"
  elsif remainder <= 5
    puts "10の倍数との差は#{remainder}です"
  else 
    puts "10の倍数との差は#{10 - remainder}です"
  end
end
```

### 学んだこと
- 整数で百の位を取得する方法は、３桁の数字を１００で割ると、Rubyでは、小数点以下は切り捨てられるため取得できます。
