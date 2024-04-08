# Rubyドリル
### 自己解答
```ruby
def binary_search()
  if 
    
  else
    
  end
  number_of_elements = 
  
  center =
end

array = [1,3,5,6,9,10,13,20,26,31]
binary_search(array)
```

### 模範解答
```ruby
def binary_search(array, right, target)
  left = 0
  while left <= right
    center = (left + right) / 2
    if array[center] == target
      return center
    elsif array[center] < target
      left = center + 1
    else
      right = center - 1
    end
  end
  return -1 
end

array=[1,3,5,6,9,10,13,20,26,31]

puts "検索したい数字を入力してください"
target = gets.to_i
number_of_elements = array.length

result = binary_search(array, number_of_elements, target)

if result == -1
  puts "#{target}は配列内に存在しません"
else
  puts "#{target}は配列の#{result}番目に存在します "
end
```

### 学んだこと
- バイナリサーチとは、順番に並べられた配列を前半と後半に区切る処理を繰り返すことで探索範囲を狭め、目的の結果にたどり着くアルゴリズムです。
