## Java Predefined-Functional Interfaces

<details><summary>Java Predefined-Functional Interfaces</summary>

|        Interface        |  Params   | Return  |                                                       Description                                                       |
|:-----------------------:|:---------:|:-------:|:-----------------------------------------------------------------------------------------------------------------------:|
|     BiConsumer<T,U>     |    T,U    |    -    |             Представляет собой операцию, которая принимает два входных аргумента и не возвращает результат.             |
|       Consumer<T>       |     T     |    -    |                 Представляет собой операцию, которая принимает один аргумент и не возвращает результат.                 |
|      Function<T,R>      |     T     |    R    |                   Представляет собой функцию, которая принимает один аргумент и возвращает результат.                   |
|      Predicate<T>       |     T     | Boolean |                           Представляет собой предикат (логическую функцию) одного аргумента.                            |
|    BiFunction<T,U,R>    |    T,U    |    R    |                   Представляет собой функцию, которая принимает два аргумента и возвращает результат.                   |
|    BinaryOperator<T>    |    T,T    |    T    | Представляет собой операцию над двумя операндами одного типа данных. Возвращает результат того же типа, что и операнды. |
|    BiPredicate<T,U>     |    T,U    | Boolean |                            Представляет собой предикат (логическую функцию) двух аргументов.                            |
|     BooleanSupplier     |     -     | Boolean |                                     Представляет поставщика логических результатов.                                     |
|  DoubleBinaryOperator   |  Double   | Double  |             Представляет собой операцию над двумя операндами типа Double и возвращает значение типа Double.             |
|     DoubleConsumer      |  Double   |    -    |           Представляет собой операцию, которая принимает один аргумент типа Double и не возвращает результат.           |
|    DoubleFunction<R>    |  Double   |    R    |                 Представляет собой функцию, которая принимает аргумент типа Double и выдает результат.                  |
|     DoublePredicate     |  Double   | Boolean |                     Представляет собой предикат (логическую функцию) одного аргумента типа Double.                      |
|     DoubleSupplier      |     -     | Double  |                                    Представляет поставщика результатов типа Double.                                     |
|   DoubleToIntFunction   |  Double   | Integer |         Представляет собой функцию, которая принимает аргумент типа Double и возвращает результат типа Integer.         |
|  DoubleToLongFunction   |  Double   |  Long   |          Представляет собой функцию, которая принимает аргумент типа Double и возвращает результат типа Long.           |
|   DoubleUnaryOperator   |  Double   | Double  |            Представляет собой операцию над одним операндом типа Double, которая дает результат типа Double.             |
|    IntBinaryOperator    |  Integer  | Integer |           Представляет собой операцию над двумя операндами типа Integer и возвращает результат типа Integer.            |
|       IntConsumer       |  Integer  |    -    |            Представляет собой операцию, которая принимает аргумент типа Integer и не возвращает результата.             |
|     IntFunction<R>      |  Integer  |    R    |               Представляет собой функцию, которая принимает аргумент типа Integer и возвращает результат.               |
|      IntPredicate       |  Integer  | Boolean |                     Представляет собой предикат (логическую функцию) одного аргумента типа Integer.                     |
|       IntSupplier       |     -     | Integer |                                       Представляет собой поставщика типа Integer.                                       |
|   IntToDoubleFunction   |  Integer  | Double  |         Представляет собой функцию, которая принимает аргумент типа Integer и возвращает результат типа Double.         |
|    IntToLongFunction    |  Integer  |  Long   |          Представляет собой функцию, которая принимает аргумент типа Integer и возвращает результат типа Long.          |
|    IntUnaryOperator     |  Integer  | Integer |           Представляет собой операцию над одним операндом типа Integer, которая дает результат типа Integer.            |
|   LongBinaryOperator    |   Long    |  Long   |              Представляет собой операцию над двумя операндами типа Long и возвращает результат типа Long.               |
|      LongConsumer       |   Long    |    -    |           Представляет собой операцию, которая принимает один аргумент типа Long и не возвращает результата.            |
|     LongFunction<R>     |   Long    |    R    |                Представляет собой функцию, которая принимает аргумент типа Long и возвращает результат.                 |
|      LongPredicate      |   Long    | Boolean |                Представляет собой предикат (функция с логическим значением) одного аргумента типа Long.                 |
|      LongSupplier       |     -     |  Long   |                                     Представляет поставщика результатов типа Long.                                      |
|  LongToDoubleFunction   |   Long    | Double  |          Представляет собой функцию, которая принимает аргумент типа Long и возвращает результат типа Double.           |
|    LongToIntFunction    |   Long    | Integer |          Представляет собой функцию, которая принимает аргумент типа Long и возвращает результат типа Integer.          |
|    LongUnaryOperator    |   Long    |  Long   |           Представляет собой операцию над одним операндом типа Long, которая возвращает результат типа Long.            |
|  ObjDoubleConsumer<T>   | T,Double  |    -    |    Представляет собой операцию, которая принимает объект и аргумент типа Double и не возвращает никакого результата.    |
|    ObjIntConsumer<T>    | T,Integer |    -    |         Представляет собой операцию, которая принимает объект и аргумент типа Integer. Не возвращает результат.         |
|   ObjLongConsumer<T>    |  T,Long   |    -    |        Представляет собой операцию, которая принимает объект и аргумент типа Long, но не возвращает результата.         |
|       Supplier<T>       |     -     |    T    |                                          Представляет поставщика результатов.                                           |
| ToDoubleBiFunction<T,U> |    T,U    | Double  |             Представляет собой функцию, которая принимает два аргумента и возвращает результат типа Double.             |
|   ToDoubleFunction<T>   |     T     | Double  |             Представляет собой функцию, которая принимает один аргумент и возвращает результат типа Double.             |
|  ToIntBiFunction<T,U>   |    T,U    | Integer |              Представляет собой функцию, которая принимает два аргумента и возвращает число типа Integer.               |
|    ToIntFunction<T>     |     T     | Integer |                        Представляет собой функцию, которая возвращает целое число типа Integer.                         |
|  ToLongBiFunction<T,U>  |    T,U    |  Long   |              Представляет собой функцию, которая принимает два аргумента и возвращает результат типа Long.              |
|    ToLongFunction<T>    |     T     |  Long   |                           Представляет собой функцию, которая возвращает результат типа Long.                           |
|    UnaryOperator<T>     |     T     |    T    |       Представляет собой операцию с одним операндом, которая возвращает результат того же типа, что и ее операнд.       |
    
</details>

### Function
Функциональный интерфейс ```Function<T,R>``` представляет функцию перехода от объекта типа T к объекту типа R:
```java
public interface Function<T, R> {
    R apply(T t);
}
```
<details><summary><b>Demo Function</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        Function<Double, Long> function = d -> Math.round(d);
        System.out.println(function.apply(5.7));
    }
}
```
</details>


### Predicate
Функциональный интерфейс ```Predicate<T>``` проверяет соблюдение некоторого условия. Если оно соблюдается, то возвращается значение true. <br>
В качестве параметра лямбда-выражение принимает объект типа T:
```java
public interface Predicate<T> {
    boolean test(T t);
}
```
<details><summary><b>Demo Predicate</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        Predicate<Integer> negative = i -> i < 0;
        System.out.println(negative.test(-6));
        System.out.println(negative.test(6)); 
    }
}
```
</details>


### BinaryOperator
```BinaryOperator<T>``` принимает в качестве параметра два объекта типа T, выполняет над ними бинарную операцию и возвращает ее результат также в виде объекта типа T:
```java
public interface BinaryOperator<T> {
    T apply(T t1, T t2);
}
```
<details><summary><b>Demo BinaryOperator</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        BinaryOperator<String> uo = (s1, s2) -> s1.concat(s2);
        System.out.print(uo.apply("Java ",  "8"));
    }
}
```
</details>


### UnaryOperator
```UnaryOperator<T>``` принимает в качестве параметра объект типа T, выполняет над ними операции и возвращает результат операций в виде объекта типа T:
```java
public interface UnaryOperator<T> {
    T apply(T t);
}
```
<details><summary><b>Demo UnaryOperator</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        UnaryOperator<String> uo = s -> s.toUpperCase();
        System.out.print(uo.apply("Java"));
    }
}
```
</details>


### Consumer
```Consumer<T>``` выполняет некоторое действие над объектом типа T, при этом ничего не возвращая:
```java
public interface Consumer<T> {
    void accept(T t);
}
```
<details><summary><b>Demo Consumer</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        Consumer<String> printUpperCase = str -> System.out.println(str.toUpperCase());
        printUpperCase.accept("hello");
    }
}
```
</details>


### Supplier
```Supplier<T>``` не принимает никаких аргументов, но должен возвращать объект типа T:
```java
public interface Supplier<T> {
    T get();
}
```
<details><summary><b>Demo Supplier</b></summary>

```java
public class Demo {
    public static void main(String[] args) {
        String t = "One";
        Supplier<String> supplierStr = () -> t.toUpperCase();
        System.out.println(supplierStr.get());
    }
}
```
</details>
    

### @FunctionalInterface
 
```java
@FunctionalInterface
public interface Function5<T, U, V, W, X> {
    public X accept(T t, U u, V v, W w);
}
    
public static void main(String[] args) throws Exception {
    Function5<String, Integer, Void, List<Float>, Character> func = (a, b, c, d) -> 'с';
}
``` 

    
## Взаимозаменяемые интерфейсы:

<details><summary>Возможна следующая замена:</summary>

|    Текущий интерфейс     | Предпочтительный интерфейс |
|:------------------------:|:--------------------------:|
|   Function<Integer, R>   |       IntFunction<R>       |
|    Function<Long, R>     |      LongFunction<R>       |
|   Function<Double, R>    |     DoubleFunction<R>      |
| Function<Double,Integer> |    DoubleToIntFunction     |
|  Function<Double,Long>   |    DoubleToLongFunction    |
|  Function<Long,Double>   |    LongToDoubleFunction    |
|  Function<Long,Integer>  |     LongToIntFunction      |
|   Function<R,Integer>    |      ToIntFunction<R>      |
|     Function<R,Long>     |     ToLongFunction<R>      |
|    Function<R,Double>    |    ToDoubleFunction<R>     |
|      Function<T,T>       |      UnaryOperator<T>      |
|    BiFunction<T,T,T>     |     BinaryOperator<T>      |
|    Consumer<Integer>     |        IntConsumer         |
|     Consumer<Double>     |       DoubleConsumer       |
|      Consumer<Long>      |        LongConsumer        |
|  BiConsumer<T,Integer>   |     ObjIntConsumer<T>      |
|    BiConsumer<T,Long>    |     ObjLongConsumer<T>     |
|   BiConsumer<T,Double>   |    ObjDoubleConsumer<T>    |
|    Predicate<Integer>    |        IntPredicate        |
|    Predicate<Double>     |      DoublePredicate       |
|     Predicate<Long>      |       LongPredicate        |
|    Supplier<Integer>     |        IntSupplier         |
|     Supplier<Double>     |       DoubleSupplier       |
|      Supplier<Long>      |        LongSupplier        |
|    Supplier<Boolean>     |      BooleanSupplier       |
|  UnaryOperator<Integer>  |      IntUnaryOperator      |
|  UnaryOperator<Double>   |    DoubleUnaryOperator     |
|   UnaryOperator<Long>    |     LongUnaryOperator      |
| BinaryOperator<Integer>  |     IntBinaryOperator      |
|   BinaryOperator<Long>   |     LongBinaryOperator     |
|  BinaryOperator<Double>  |    DoubleBinaryOperator    |
|   Function<T, Boolean>   |        Predicate<T>        |
| BiFunction<T,U,Boolean>  |      BiPredicate<T,U>      |

</details>


<br><br>
