# Rubyドリル32（クラスとインスタンスを使用したエラー問題）
### 自己解答
```ruby
class Student
  def set_name(name)
    @name = name
  end

  def self.introduce
    puts "私の名前は#{@name}です。"
  end
end

student = Student.new
student.set_name("山田太郎")
student.introduce
```

### 模範解答
```ruby
class Student
  def set_name(name)
    @name = name
  end

  def introduce
    puts "私の名前は#{@name}です。"
  end
end

student = Student.new
student.set_name("山田太郎")
student.introduce
```

### 学んだこと
- classメソッドとは、classで共通する情報を扱う際に定義されます。
- classメソッドは、class内でしか使用できなく、しかもインスタンス変数は扱えない。
