# Rubyドリル
### 自己解答
```ruby
def get_days(year, month)
  if year/4
    
  elsif 
    
  else
    
  end
end

puts "年を入力してください："
year = gets.to_i
puts "月を入力してください："
month = gets.to_i

days = get_days(year, month)
puts "#{year}年#{month}月は#{days}日間あります"
```

### 模範解答
```ruby
def get_days(year, month)
    month_days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
    if month == 2
      if year % 4 == 0
        if year % 100 == 0 && year % 400 != 0
          days = 28
        else
          days = 29
        end
      else
        days = 28
      end
    else
      days = month_days[month - 1]
    end

    return days
  end

  puts "年を入力してください："
  year = gets.to_i
  puts "月を入力してください："
  month = gets.to_i

  days = get_days(year, month)
  puts "#{year}年#{month}月は#{days}日間あります"
```

### 学んだこと
- %とは、計算を行う演算子の一つで、割り算した余りを計算します。
