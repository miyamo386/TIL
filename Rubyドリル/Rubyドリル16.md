# Rubyドリル16（インスタンスの生成）
### 自己解答
```ruby
class Fruit
  def fresh
        puts "「採れたて新鮮な果実です」"
  end

  def initialize(name, price)
      end

  def introdube

  end
 end


 apple = Fruit.new
 orange = Fruit.new
 strawbery = Fruit.new

  puts fresh
```

### 模範解答
```ruby
class Fruit

 def self.fresh
   puts "採れたて新鮮な果実です"
 end

 def initialize(name, price)
   @name = name
   @price = price
 end

 def introduce
   puts "#{@name}は#{@price}円です"
 end
end

apple = Fruit.new("リンゴ", 120)
orange = Fruit.new("オレンジ", 200)
strawberry = Fruit.new("イチゴ", 60)

Fruit.fresh
apple.introduce
orange.introduce
strawberry.introduce
```

### 学んだこと
-  クラスメソッドとは、クラス全体で共通した処理を行うメソッドで、定義するとき「self.メソッド名」と記述します。
-  initializeとは、インスタンスを生成すると、initializeメソッドに定義した処理が自動的に実行されるメソッドです。
