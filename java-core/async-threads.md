## Java Async Threads
 
### FutureTask
 
```java
public class Main {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newCachedThreadPool();
        Future<Long> task = executor.submit(
                () -> exec()); 
        while (!task.isDone()) {
            System.out.println(".");
        }
        long time = task.get();
        executor.shutdown();
    }

    private static Long exec() {
        TimeUnit.MILLISECONDS.sleep(500);
        return System.nanoTime();
    }
}
```

### CompletableFuture

```java
public class Main {
    public static void main(String[] args) {
        CompletableFuture<Long> completableFuture = CompletableFuture.supplyAsync(
                () -> exec());
        while (!completableFuture.isDone()) {
            System.out.println(".");
        } 
        long time = completableFuture.get();
    }
    
    private static Long exec() {
        TimeUnit.MILLISECONDS.sleep(500);
        return System.nanoTime();
    }
}
```

<br><br>
