# Sparkproject Failureaccess
guava failureaccess for spark project
- Spark 3.5.0
- Scala 2.12
- OpenJDK8
- CentOS 7.6 with wsl2
```
23/10/24 12:00:42 ERROR Inbox: An error happened while processing message in the inbox for Executor
java.lang.NoClassDefFoundError: org/sparkproject/guava/util/concurrent/internal/InternalFutureFailureAccess
	at java.lang.ClassLoader.defineClass1(Native Method)
	at java.lang.ClassLoader.defineClass(ClassLoader.java:756)
	at java.security.SecureClassLoader.defineClass(SecureClassLoader.java:142)
	at java.net.URLClassLoader.defineClass(URLClassLoader.java:473)
	at java.net.URLClassLoader.access$100(URLClassLoader.java:74)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:369)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:363)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:362)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	at java.lang.ClassLoader.defineClass1(Native Method)
	at java.lang.ClassLoader.defineClass(ClassLoader.java:756)
	at java.security.SecureClassLoader.defineClass(SecureClassLoader.java:142)
	at java.net.URLClassLoader.defineClass(URLClassLoader.java:473)
	at java.net.URLClassLoader.access$100(URLClassLoader.java:74)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:369)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:363)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:362)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	at java.lang.ClassLoader.defineClass1(Native Method)
	at java.lang.ClassLoader.defineClass(ClassLoader.java:756)
	at java.security.SecureClassLoader.defineClass(SecureClassLoader.java:142)
	at java.net.URLClassLoader.defineClass(URLClassLoader.java:473)
	at java.net.URLClassLoader.access$100(URLClassLoader.java:74)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:369)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:363)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:362)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	at org.sparkproject.guava.cache.LocalCache$LoadingValueReference.<init>(LocalCache.java:3511)
	at org.sparkproject.guava.cache.LocalCache$LoadingValueReference.<init>(LocalCache.java:3515)
	at org.sparkproject.guava.cache.LocalCache$Segment.lockedGetOrLoad(LocalCache.java:2168)
	at org.sparkproject.guava.cache.LocalCache$Segment.get(LocalCache.java:2079)
	at org.sparkproject.guava.cache.LocalCache.get(LocalCache.java:4011)
	at org.sparkproject.guava.cache.LocalCache.getOrLoad(LocalCache.java:4034)
	at org.sparkproject.guava.cache.LocalCache$LocalLoadingCache.get(LocalCache.java:5010)
	at org.apache.spark.storage.BlockManagerId$.getCachedBlockManagerId(BlockManagerId.scala:146)
	at org.apache.spark.storage.BlockManagerId$.apply(BlockManagerId.scala:127)
	at org.apache.spark.storage.BlockManager.initialize(BlockManager.scala:536)
	at org.apache.spark.executor.Executor.<init>(Executor.scala:151)
	at org.apache.spark.executor.CoarseGrainedExecutorBackend$$anonfun$receive$1.applyOrElse(CoarseGrainedExecutorBackend.scala:174)
	at org.apache.spark.rpc.netty.Inbox.$anonfun$process$1(Inbox.scala:115)
	at org.apache.spark.rpc.netty.Inbox.safelyCall(Inbox.scala:213)
	at org.apache.spark.rpc.netty.Inbox.process(Inbox.scala:100)
	at org.apache.spark.rpc.netty.MessageLoop.org$apache$spark$rpc$netty$MessageLoop$$receiveLoop(MessageLoop.scala:75)
	at org.apache.spark.rpc.netty.MessageLoop$$anon$1.run(MessageLoop.scala:41)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: java.lang.ClassNotFoundException: org.sparkproject.guava.util.concurrent.internal.InternalFutureFailureAccess
	at java.net.URLClassLoader.findClass(URLClassLoader.java:387)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:352)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	... 56 more
```

# Build
```bash
mvn package
```
