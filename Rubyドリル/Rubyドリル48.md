# Rubyドリル
### 自己解答
```ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end
end

class Student < Person
  def name
    puts "私の名前は#{@name}です。#{@age}です"
  end
end

pochi = Student.new("鈴木太郎", 20)
pochi.name
```

### 模範解答
```ruby
class Person
  def initialize(name, age)
    @name = name
    @age = age
  end
end

class Student < Person
  def introduce
    puts "私の名前は#{@name}です。#{@age}歳です"
  end
end
```

### 学んだこと
- クラスの継承とは、既にあるクラスを元に新しくクラスを作ることで、共通するコードを引き継げます。
- クラスの継承で、インスタンス変数とインスタンスメソッドを引き継げます。
