# ruby_drill_10（配列を利用したrubyプログラムの作成）
### 自己解答
```ruby
def search(target_num, input)
  input.each_with_index do |item, i|
    puts "#{i}番目にあります"
   end
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]

search(11, input)
```

### 模範解答
```ruby
def search(target_num, input)

  input.each_with_index do |num, index|
    if num == target_num
      puts "#{index + 1}番目にあります"
      return
    end
  end
  puts "その数は含まれていません"
end

input = [3, 5, 9 ,12, 15, 21, 29, 35, 42, 51, 62, 78, 81, 87, 92, 93]
search(11, input)
```

### 学んだこと
- 配列は0番目から始まるので、＋１する必要がある。
- each_with_indexメソッドとは、繰り返し処理と要素が処理された順番を表す、Ruby標準メソッドです。
