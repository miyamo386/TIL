# Rubyドリル
### 自己解答
```ruby
def count_code(str)
  str.index("code", 0)
end

count_code("codexxcode")
count_code("aaacodebbb")
count_code("cozexxcode")
```

### 模範解答
```ruby
def count_code(str)
  puts str.index("code", 0) + 1
end
```

### 学んだこと
- indexとは、文字列や配列内で指定した要素（文字列）が、最初から何番目なのか整数で返すメソッドのこと。
- 注意点があり、最初の要素は0番目としてカウントされるため、＋１が必要となる。
