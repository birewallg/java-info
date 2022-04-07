>  

Simple loop thread

```groovy
import lombok.SneakyThrows;
import lombok.extern.slf4j.Slf4j;

import java.util.concurrent.TimeUnit;
import java.util.concurrent.atomic.AtomicBoolean;

@Slf4j
public class Service {
    private static final AtomicBoolean hook = new AtomicBoolean(false);
    
    public boolean initialize(boolean hook) {
        if (Service.hook.get() == hook) {
            return hook;
        }
        Service.hook.set(hook); 
        if (!Service.hook.get()) {
            return false;
        } 
        MainThread mainThread = new MainThread();
        Thread thread = new Thread(mainThread);
        thread.start();
        return true;
    }
    private static class MainThread implements Runnable {
        @SneakyThrows
        @Override
        public void run() {
            while (Service.hook.get()) {
                log.info("{}", this);
                TimeUnit.MILLISECONDS.sleep(1000);
            }
        }
    }
}
```
Initialize:
```groovy
    private boolean initialize = true;
    public void onReader() {
        Service service = new Service();
        service.initialize(initialize);
        initialize = !initialize;
    }
```