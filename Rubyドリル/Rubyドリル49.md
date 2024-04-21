# Rubyドリル
### 自己解答
```ruby
def include_cat_and_dog?(str)
  if str.include?("catdog")
    puts "True"
  else
    puts "False"
  end
end

include_cat_and_dog?("catdog")
```

### 模範解答
```ruby
def include_cat_and_dog?(str)
  if str.include?("cat") && str.include?("dog")
    puts true
  else
    puts false
  end
end

# 呼び出し例
include_cat_and_dog?("catdog")
```

### 学んだこと
- &&とは、条件式が両方とも当てはまることを意味する演算子です。
