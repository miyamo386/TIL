- Thymeleafとは、Javaで使用されるSpring Bootと相性の良いテンプレートエンジンのこと

# 使い方
## **⒈ ライブラリを追加**

1. ルートディレクトリ「build.gradle」ファイル内のdependenciesブロックに記述

```java
plugins {
    id 'java'
    id 'org.springframework.boot' version '3.2.7'
    id 'io.spring.dependency-management' version '1.1.5'
}

group = 'in.techcamp'
version = '0.0.1-SNAPSHOT'

java {
    toolchain {
        languageVersion = JavaLanguageVersion.of(21)
    }
}

repositories {
    mavenCentral()
}

dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
    testRuntimeOnly 'org.junit.platform:junit-platform-launcher'
    implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
}

tasks.named('test') {
    useJUnitPlatform()
}
```

## **⒉  表示させるためのHTMLを作成**
1. 「firstapp」「src」「main」「resources」フォルダにある「templates」フォルダを右クリック
2. 「新規」「HTMLファイル」を選択
3. ファイル名を書く
4. **HTMLを編集**

```html
【src/main/resources/templates/hello.html】

<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org" lang="ja">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<h1>Hello World from Thymeleaf!</h1>
</body>
</html>
```

## **⒊ コントローラーから①のファイルを読み込めるようにする**
```java
@Controller
public class PostController {
    @GetMapping("/hello")
    public String showHello(){
        return "hello";
   }
}
```

- 「return "hello";」と記述することで「templates」フォルダにある「hello.html」を呼び出しています
