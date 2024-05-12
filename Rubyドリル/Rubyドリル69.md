# Rubyドリル
### 自己解答
```ruby
class Food
  def food_calorie
    cooking_name =

  end
end

while true do
  puts "[0]:カロリーを入力する"
  puts "[1]:カロリーの合計を見る"
  input = gets.to_i

  if input == 0
    Food.input           # カロリーの入力
  elsif input == 1
    Food.show_all_calory # カロリーの合計を表示
    exit
  end
end
```

### 模範解答
```ruby
class Food
    @@foods = []

    def self.input
      puts "料理名を入力してください:"
      name = gets.chomp
      puts "カロリーを入力してください:"
      calory = gets.to_i

      food = Food.new(name, calory)
      @@foods << food
    end

    def self.show_all_calory
      all_calory = 0
      line = "-----------------------------"
      puts line

      @@foods.each do |food|
        puts "#{food.name}  :#{food.calory}kcal"
        all_calory = all_calory + food.calory
      end

      puts line
      puts "カロリー合計  :#{all_calory}kcal"
    end

    def initialize(name, calory)
      @name = name
      @calory = calory
    end

    def name
      return @name
    end

    def calory
      return @calory
    end
  end

  while true do
    puts "[0]:カロリーを入力する"
    puts "[1]:カロリーの合計を見る"
    input = gets.to_i

    if input == 0
      Food.input           # カロリーの入力
    elsif input == 1
      Food.show_all_calory # カロリーの合計を表示
      exit
    end
  end
```

### 学んだこと
- クラス変数とは、クラス内に定義される変数で頭に@@が付きます。
