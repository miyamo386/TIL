# Rubyドリル
### 自己解答
```ruby
def num(a, b, c)
  ab = a + b
  if ab >= 3
    ab / c
  else
    ab * c
  end
end

num(1,5,3) 
num(1,5,5)
```

### 模範解答
```ruby
def num(a, b, c)
  ab = a + b
  if c <= 3
    puts ab / c
  else
    puts ab * c
  end
end

num(1,5,3)
```

### 学んだこと
- 以上を表す比較演算子は「<=」で、例えば「a<=b」だと「aはb以上」を表します。
