# Rubyドリル18（2つの条件を組み合わせた条件式）
### 自己解答
```ruby
def police_trouble(a, b)
  if a && b
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
police_trouble(true, true) 
police_trouble(false, false)
police_trouble(true, false)
```

### 模範解答
```ruby
def police_trouble(a, b)
  if (a && b) || (!a && !b)
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
police_trouble(true, true) 
police_trouble(false, false)
police_trouble(true, false) 
```

### 学んだこと
- not演算子とは、エクスクラメーションマーク（！）のことで、否定を表す演算子です。例えば「!a」の場合、aはtureで無いとなります。
