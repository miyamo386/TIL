# Rubyドリル
### 自己解答
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
  puts "車種:#{car[:type]}"
  puts "1Lあたりの走行可能距離:#{car[:fuel_economy]}km/l"
  puts "乗車人数:#{car[:capacity]}人"

  puts "これから走る距離(km)を入力して下さい。"
  input_distance = gets.to_f

  calculate_fuel_consumption(car, input_distance)
end

def calculate_fuel_consumption(car, distance)
  fuel_consumption = distance / car[:fuel_economy]
  puts "その目的地までは、ガソリンを#{fuel_consumption.round(1)}L消費します。"
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
  puts "車種:#{car[:type]}"
  puts "1Lあたりの走行可能距離:#{car[:fuel_economy]}km/l"
  puts "乗車人数:#{car[:capacity]}人"

  puts "これから走る距離(km)を入力して下さい。"
  input_distance = gets.to_f

  puts "これから乗る人数を入力して下さい。"
  input_capacity = gets.to_i

  calculate_fuel_consumption(car, input_distance)
  car_capacity(car, input_capacity)
end

def calculate_fuel_consumption(car, distance)
  fuel_consumption = distance / car[:fuel_economy]
  puts "その目的地までは、ガソリンを#{fuel_consumption.round(1)}L消費します。"
end

def car_capacity(car, capacity)
  capacity = car[:capacity] - capacity

  if capacity == 0
    puts "車の定員丁度です。"
  elsif capacity > 0
    puts "後、車には#{capacity}人乗ることができます。"
  else
    puts "#{capacity.abs}人定員オーバーです。"
  end
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
-　absとは、数値がー（マイナス）の場合にーを除くメソッドのことです。
