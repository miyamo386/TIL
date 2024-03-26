# Rubyドリル26（末尾の文字列を3回出力するプログラム）
### 自己解答
```ruby
def extra_end(str)
  string = str.slice(4..5)
  string.times do |i|
    puts "#{i}"
  end
end

extra_end('Hello')
```

### 模範解答
```ruby
def extra_end(str)
  right2 = str.slice(- 2, 2)
  puts right2 * 3
end

# 呼び出し例
extra_end('Hello') 
```

### 学んだこと
- sliceメソッドを用いて文字列から指定した要素を取り出すには、第１引数に基準点を指定し、第２引数で何文字取得するかを指定します。
- 文字列が格納された変数に、* 3すると3連続で出力される。
