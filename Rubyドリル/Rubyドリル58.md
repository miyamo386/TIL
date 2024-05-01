# Rubyドリル
### 自己解答
```ruby
def register_data
  puts "名前を入力してください"
  name = gets.chomp
  puts "パンチ力を入力してください(0 ~ 100)"
  punch = gets.to_i
  puts "キック力を入力してください(0 ~ 100)"
  kick = gets.to_i
  puts "ジャンプ力を入力してください(0 ~ 100)"
  jump = gets.to_i

  register = { name: name, punch: punch, kick: kick, jump: jump}
  data << register
end

def show_data_list
  puts '見たい人の番号を選択してください'
  data.each_with_index do |register, index|
    puts "#{index + 1}: #{register[:name]}"
  end
  input = gets.to_i - 1
  show_data(data[input])
end

while true
  puts '選択してください'
  puts '[0]登録する'
  puts '[1]データを確認する'
  puts '[2]終了する'
  input = gets.to_i

  if input == 0
    register_data
  elsif input == 1
    show_data_list
  elsif input == 2
    exit
  else
    puts '無効な値です'
  end
end
```

### 模範解答
```ruby
def register_data(data)

  puts '名前を入力してください'
  name = gets.chomp
  puts 'パンチ力を入力してください(0 ~ 100)'
  punch = power(gets.to_i)
  puts 'キック力を入力してください(0 ~ 100)'
  kick = power(gets.to_i)
  puts 'ジャンプ力を入力してください(0 ~ 100)'
  jump = power(gets.to_i)

  person = {name: name, punch: punch, kick: kick, jump: jump}
  data << person

end

def power(power)
    while power > 100
      puts '100以下の数字を入力してください'
        power = gets.to_i
    end
    return power
end

def show_data_list(data)
  puts '見たい人の番号を選択してください'
  data.each_with_index do |person, index|
    puts "#{index + 1}: #{person[:name]}"
  end
  input = gets.to_i - 1
  person = data[input]
  puts "名前: #{person[:name]}"
  puts "パンチ力: #{person[:punch]}"
  puts "キック力: #{person[:kick]}"
  puts "ジャンプ力: #{person[:jump]}"

end

data = []

while true
  puts '選択してください'
  puts '[0]登録する'
  puts '[1]データを確認する'
  puts '[2]終了する'
  input = gets.to_i

  if input == 0
    register_data(data)
  elsif input == 1
    show_data_list(data)
  elsif input == 2
    exit
  else
    puts '無効な値です'
  end
end
```

### 学んだこと
- returnとは、「return」の後にある要素がメソッドの戻り値となるRubyの文法です。
- getsで入力した値を引数内に記述することもできる。
