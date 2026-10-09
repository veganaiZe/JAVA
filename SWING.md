# 🪟 [SWING](https://docs.oracle.com/javase/8/docs/technotes/guides/swing/index.html)


### [JFrame](https://docs.oracle.com/javase/8/docs/api/javax/swing/JFrame.html)
```java
/**
 * javax.swing.JFrame
 *
 * Top-level container which can optionally have a menu bar (outside of its content pane).
 */

new JFrame([String title][, GraphicsConfiguration])

.add(Component[, constraints][, index])
.pack()  // sizes Window to fit subcomponents and enlarges it to meet .setMinimumSize()
.setDefaultCloseOperation(int)  // action when user closes frame; EXIT_ON_CLOSE, DISPOSE_ON_CLOSE, etc.
.setIconImage(Image)            // frame.setIconImage(new ImageIcon("icon.png").getImage());
.setJMenuBar(JMenuBar)
.setLocationRelativeTo(Component)  // Centers frame on screen if null
.setResizable(boolean)
.setSize(width, height)
```


### [SwingUtilities](https://docs.oracle.com/javase/8/docs/api/javax/swing/SwingUtilities.html)
```java
/**
 * javax.swing.SwingUtilities
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
