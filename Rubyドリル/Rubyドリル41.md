# Rubyドリル
### 自己解答
```ruby
def close_far(a,b,c)
  x = (a - b).abs
  y = (a - c).abs
  z = (b - c).abs

  if x = 1 || z <= 2
    puts "True"
  elsif y = 1 || z <= 2
    puts "True"
  else
    puts "False"
  end
end

close_far(1, 2, 10)
close_far(1, 2, 3)
```

### 模範解答
```ruby
def close_far(a,b,c)
  x = (a-b).abs
  y = (a-c).abs
  z = (b-c).abs

  if (x == 1 && z >= 2)
    puts "True"
  elsif ( y == 1 && z >= 2)
    puts "True"
  else
    puts "False"
  end
end
```

### 学んだこと
- 「かつ」を表す演算子は「&&」を使用します。
- absとは、絶対値（-を除いた整数）を取得ができるメソッドです。
