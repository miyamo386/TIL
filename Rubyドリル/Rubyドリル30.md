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
- 「..」とは、数値や日付、「"a" から "z" まで」といった文字列など、始点から終点を含むすべての範囲を表すオブジェクトです。
- 「...」は、始点と終点の値を除いた範囲を表します。
