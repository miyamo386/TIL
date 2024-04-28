# Rubyドリル５５
### 自己解答
```ruby
def register_data
  puts "見たい人の番号を選択してください"

end

def show_data
  
end

while true
  puts "選択してください"
  puts "[0]登録する"
  puts "[1]データを確認する"
  puts "[2]終了する"
  input = gets.to_i

  if input == 0
    register_data
  elsif input == 1
   show_data
  elsif input == 2
    exit
  else
    puts "無効な値です"
  end
end
```

### 模範解答
```ruby
def register_data(data)
  puts "名前を入力してください"
  name = gets.chomp
  puts "年齢を入力してください"
  age = gets.chomp
  puts "身長を入力してください（m単位）"
  tall = gets.to_f
  puts "体重を入力してください"
  weight = gets.to_f
  person = { name: name, age: age, tall: tall, weight: weight}
  data << person
end

def show_data_list(data)
  puts "見たい人の番号を選択してください"
  data.each_with_index do |person, index|
    puts "#{index + 1}: #{person[:name]}"
  end
  input = gets.to_i - 1
  show_data(data[input])
end

def show_data(data)
  puts "名前:#{data[:name]}"
  puts "年齢:#{data[:age]}"
  puts "身長:#{data[:tall]}"
  puts "体重:#{data[:weight]}"
end

data = []
while true
  puts "選択してください"
  puts "[0]登録する"
  puts "[1]データを確認する"
  puts "[2]終了する"
  input = gets.to_i

  if input == 0
    register_data(data)
  elsif input == 1
    show_data_list(data)
  elsif input == 2
    exit
  else
    puts "無効な値です"
  end
end

```

### 学んだこと
- to_fとは、小数点以下を表示するメソッドです。
- each_with_indexとは、eachで繰り返しながら、それぞれのデータに番号を振るメソッドです。
