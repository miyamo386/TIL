# Rubyドリル
### 自己解答
```ruby
def count_hi(str)
  str.scan("hi")
end

count_hi('abc hi ho')
count_hi('ABChi hi')
count_hi('hihi')
```

### 模範解答
```ruby
def count_hi(str)
  puts str.scan("hi").length
end

# 呼び出し例
count_hi('abc hi ho')
```

### 学んだこと
- lengthとは、文字列の文字数をカウントするメソッドのこと。
- 「.」は、要素とメソッドなどを連結し１つの式を表します。
- scanとは、引数で指定した値（要素）を配列として返すメソッドのこと。
