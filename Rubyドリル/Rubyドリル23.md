# Rubyドリル23（特定の数字を検知するプログラムの実装）
### 自己解答
```ruby
def array123(nums)
  puts nums.include?(1, 2, 3)
end
```

### 模範解答
```ruby
def array123(nums)
  if nums.include?(1) && nums.include?(2) && nums.include?(3)
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
array123([1, 1, 2, 3, 1])
```

### 学んだこと
- &&演算子を追加する事で、条件式の条件を複数設定できる。
- include?メソッドとは、指定した値が配列内や文字列にあるのか？判別し、tureかfalseで返します。
