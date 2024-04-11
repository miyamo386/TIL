# Rubyドリル
### 自己解答
```ruby
def argument_test(num1, num2)
  nums = num1 * num2
  puts "5と6をかけた答えは#{nums}です！"
end

puts "最初の数字を入力してください"
num1 = gets.to_i
puts "2番目の数字を入力してください"
num2 = gets.to_i
argument_test(num1, num2)
```

### 模範解答
```ruby
def multiplication(num1, num2)
  puts "#{num1}と#{num2}をかけた答えは#{num1 * num2}です！"
end

puts "最初の数字を入力してください"

num1 = gets.to_i

puts "2番目の数字を入力してください"

num2 = gets.to_i

multiplication(num1, num2)
```

### 学んだこと
- 引数の仮引数の命名は何でも良いが、実引数を不自然に違う名前にするなら、同じ名前の方が分かりやすくなる。
