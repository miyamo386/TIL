# Rubyドリル
### 自己解答
```ruby
def xyz_there(str)
  if str.include?("xyz") ||
    puts "True"
  elsif str.include?("xyz") ||
    puts "False"
  else
    puts "False"
  end
end

xyz_there('abcxyz')
xyz_there('abc.xyz')
```

### 模範解答
```ruby
def xyz_there(str) 
  if str.include?(".xyz")
    puts "False"
  elsif str.include?("xyz")
    puts "True"
  else
    puts "False"
  end
end

# 呼び出し例
xyz_there('abcxyz')
```

### 学んだこと
- include?とは、指定された値が文字列に含まれているのかを判定するメソッドのことです。
- 「.」が含まれているのかを判別する際は、「.」を含めて指定します。
