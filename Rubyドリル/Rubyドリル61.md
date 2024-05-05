# Rubyドリル
### 自己解答
```ruby
def car_data(data)

  car = {name: name, }
  data << car

end

def show_data_list(data)

  puts '見たい人の番号を選択してください'
  data.each_with_index do |car, index|
    puts "#{index + 1}: #{person[:name]}"
  end

  input = gets.to_i - 1
  car = data[input]
  puts 

end


data = []

while true
  puts '選択してください'
  puts '[0]データの登録'
  puts '[1]データの確認'
  puts '[2]プログラムの終了'
  input = gets.to_i

  if input == 0
    car_data(data)
  elsif input == 1
    show_data_list(data)
  elsif input == 2
    exit
  else
    puts '無効な値です'
  end
end
```

### 模範解答
```ruby
def register_data(cars)
  puts "車種の入力をして下さい。"
  type = gets.chomp
  puts "1Lあたりの走行可能距離(km/l)を入力して下さい。"
  fuel_economy = gets.to_f
  puts "乗車可能人数を入力して下さい。"
  capacity = gets.to_i
  car = { type: type, fuel_economy: fuel_economy, capacity: capacity }
  cars << car
end

def show_cars(cars)
  cars.each_with_index do |car, index|
    puts "[#{index}]: #{car[:type]}"
  end
  puts "確認したい番号を入力して下さい。"
  input = gets.to_i
  car = cars[input]
  if car
    show_data(car)
  else
    puts "該当する番号はありません。"
  end
end

def show_data(car)
  puts car[:type]
  puts "1Lあたりの走行可能距離:#{car[:fuel_economy]}km/l"
  puts "乗車人数:#{car[:capacity]}人"
end

cars = []

while true do
  puts "番号を入力して下さい"
  puts "[0]:登録をする"
  puts "[1]:データを確認する"
  puts "[2]:終了する"
  input = gets.chomp

  case input
  when "0"
    register_data(cars)
  when "1"
    show_cars(cars)
  when "2"
    exit
  else
    puts "無効な値です"
  end
end
```

### 学んだこと
- caseとは、比較する値を、whenで指定した条件に該当するとその処理を行う、Rubyの構文です。
