# 🪟 SWING


### [SwingUtilities](https://docs.oracle.com/javase/8/docs/api/javax/swing/SwingUtilities.html)
```java
/**
 * javax.swing.SwingUtilties
 */

.invokeLater(Runnable)    // asynchronously executes Runnable on awt event dispatching thread
.invokeAndWait(Runnable)  // synchronously executes Runnable on awt event dispatching thread
.isEventDispatchThread()  // returns true if current thread is an awt event dispatching thread
```


### [SwingWorker](https://docs.oracle.com/javase/8/docs/api/javax/swing/SwingWorker.html)
```java
/**
 * javax.swing.SwingWorker<T,V>
 *
 * Abstract class for running tasks on a background thread.
 *
 * T - type returned by .doInBackground() and .get()
 * V - type used for intermediate results by .publish() and .process()
 */

.doInBackground()  // returns T; executes once in a background thread
.done()     // executes on event dispatch thread after .doInBackground() is finished
.execute()  // schedules execution on a worker thread & returns immediately
```
