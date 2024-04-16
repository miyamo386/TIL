# Rubyドリル45（randメソッド）
### 自己解答
```ruby
def rand_num
  num = rand(10)
  if num => 5
    puts "#{num}は4より大きい！"
  else
    puts "#{num}は5より小さい！"
  end
end
```

### 模範解答
```ruby
num = rand(10)
if num >= 5
  puts "#{num}は4より大きい！"
else
  puts "#{num}は5より小さい！"
end
```

### 学んだこと
- randとは、指定した数値以下の数字をランダムに出力するメソッドです。
