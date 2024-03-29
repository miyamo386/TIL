# Rubyドリル
### 自己解答
```ruby
def fizz_buzz(num)
  if num % 3
    puts "Fizz"
  elsif num % 5
    puts "Buzz"
  else
    
  end
  
end

num = gets.to_i
fizz_buzz(num)
```

### 模範解答
```ruby
def fizz_buzz
    num = 1
    while (num <= 100) do
      if (num % 3 == 0) && (num % 5 == 0)
        puts "FizzBuzz"
      elsif (num % 3) == 0
        puts "Fizz"
      elsif (num % 5) == 0
        puts "Buzz"
      else
        puts num
      end

      num = num + 1
    end
  end

  fizz_buzz
```

### 学んだこと
- (num % 3 == 0)とは、整数を3で割った余りと０が等しいを表します。
- while文とは、条件がtureの間は処理を繰り返すRubyの構文です。
- while文は、「while 条件式 do 処理 end」と記述するが、「do end」は省略できる。
