# Rubyドリル
### 自己解答
```ruby
def missing_char(str, n)
  string = "#{str}"
  string.slice!(n)

puts string
  # 処理を記述
end
```

### 模範解答
```ruby
def missing_char(str, n)
  str.slice!(n - 1)
  puts str
end

# 呼び出し例
missing_char('kitten', 1)
```

### 学んだこと
- 文字列の順番は、配列と同じく、先頭は「０」からカウントされます。
- slice!とは、配列や文字列から、指定した値を削除して、変更された値を返すメソッドです。
- 破壊的メソッドとは、メソッド名あとに「！」がつき、配列や文字列を変更するメソッドの総称です。
