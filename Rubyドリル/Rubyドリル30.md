# Rubyドリル
### 自己解答
```ruby
def fizzbuzz(max_num)
  (1..max_num).each do |num|
    if 
      puts
    elsif
      puts
    elsif
      puts
    else
      puts
    end
  end
end

puts 'いくつまで数えますか？'
num = gets.to_i
fizzbuzz(num)
```

### 模範解答
```ruby
def fizzbuzz(max_num)

  (1..max_num).each do |num|
    if num % 15 == 0
      puts "FizzBuzz"
    elsif num % 5 == 0
      puts "Buzz"
    elsif num % 3 == 0
      puts "Fizz"
    else
      puts num
    end
  end
end

puts 'いくつまで数えますか？'
num = gets.to_i
fizzbuzz(num)
```

### 学んだこと
- 範囲演算子..とは、
