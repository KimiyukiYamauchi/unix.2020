# Java Exam 期末試験

### 問1

Javaのソースファイルをコンパイルするのに必要なコマンドは何ですか?

### 問2

Java EEの特徴は何ですか?

### 問3

以下の変数宣言がコンパイルエラーとなる場合はコンパイルが通るように修正してしてください

``` java
1. int avg = 0.0;
2. String a = "Hello";
3. int [] a = new int[3];
　System.out.println(a[3]);
4. Integer a = 100;
5. final String str;
```

### 問４

以下をコンパイル、実行した結果はどうなりますか？

``` java
class Test {
  public static void main(String[] args) {
    int x = 4;
    do {
      ++x;
      System.out.print(x + " ");
    } while ( x == 5);
    System.out.println();
  }
}
```

### 問５

以下のオブジェクト指向コンセプトに関する用語の説明は何についての説明ですか？

1. 影響範囲の特定に関する重要な設計原則。関係するデータをまとめ、さらいそのデータを使う処理をまとめて、１つのモジュールとして定義すること
2. 共通のインタフェースをもつ操作でも、実際にはオブジェクトごとに振る舞いや動作が異なること

### 問6

以下をコンパイル、実行した結果はどうなりますか？

``` java
class Test {
  String name = "hana";
  public static void main(String[] args) {
    String name = args[1];
    Test obj = new Test();
    System.out.println(obj.name);
  }
}
```
``` bash
java Test kei bill
```

### 問7

以下をコンパイル、実行した結果はどうなりますか？

``` java
class Test {
  static String lang = "C";
  public String operation = "Unix";
  Test() {}
  Test(String str) {
    operation = str;
  }
  public static void main(String[] args) {
    Test obj1 = new Test();
    Test obj2 = new Test("Solaris");
    obj2.lang = "Java";
    System.out.println(obj1.lang + "\t" + obj1.operation);
    System.out.println(obj2.lang + "\t" + obj2.operation);
  }
}
```

### 問8

以下をコンパイル、実行した結果はどうなりますか？

``` java
class A {
  static int num = 0;
  A() { num++; }
}
class B extends A {
  int num = 10;
  B() { num++; }
}
class Test {
  public static void main(String[] args) {
      A a1 = new A(); A a2 = new A(); A a3 = new A();
      B b1 = new B(); B b2 = new B(); B b3 = new B();
      A[] valA = {a1, a2, a3};
      B[] valB = {b1, b2, b3};
      for ( B obj : valB ) {
        System.out.print(obj.num + " ");
      }
  }
}
```

### 問9

以下をコンパイル、実行した結果はどうなりますか？

``` java
class Vehicle {
  Vehicle() {
    System.out.print("Vehicle ");
  }
}
class Bike extends Vehicle {
  Bike() {
    System.out.print("Bike ");
  }
}
class Bicycle extends Bike {
  Bicycle() {
    System.out.print("Bicycle ");
  }
  public static void main(String[] args) {
      Bicycle obj = new Bicycle();
  }
}
```

### 問10

以下をコンパイル、実行した結果はどうなりますか？
``` java
class Test {
  public static void main(String[] args) {
    int a = 5;
    int b = a++;
    int c = ++a;
    System.out.println(a + " " + b + " " + c);
  }
}
```