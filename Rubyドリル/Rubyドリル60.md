# Rubyドリル
### 自己解答
```ruby
class Dog
  # ここにクラスの定義を書き加えてください

  def say_type
    puts "わたしは「クラス変数#{}」です"
  end

  def self_introduction
    puts "わたしの名前は「インスタンス変数#{}」です"
  end
end

# クラスの外でメソッドを呼び出してください
```

### 模範解答
```ruby
class Dog
    @@type = "犬"

    def initialize
      @name = "マロン"
      @dog_type = "トイプードル"
    end

    def self.say
      puts "ワンワン"
    end

    def say_type
      puts "わたしは#{@@type}です"
    end

    def self_introduction
      puts "わたしの名前は#{@name}で種類は#{@dog_type}です"
    end
  end

 dog = Dog.new
 Dog.say
 dog.say_type
 dog.self_introduction
```

### 学んだこと
- クラス変数とは、@@から始まる変数でクラスから作成されたすべてのインスタンスで共有できる変数のことです。
