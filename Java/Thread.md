Thread Pool
1. If it has a task, use service().
2. find an idle worker in List.
3. 1. If found out, assign the task to the worker.
   2. If not found, create a new worker, put it in the List,
   and then assign the task to it.

Thread Worker
1. while( isContinue() ) wait();
2. if this worker is assigned a task, then notify(), that is to break waiting status.
3. when complete the task, set the task in the worker to null.
4. run step1 until the workerThread is removed.

Thread pool in JAVA:

1. newCacheThreadPool：執行緒 Pool 發現有執行緒執行完之後，會將資源回收重新的再使用。如果沒有回收的資源，那就會再去建立執行緒。

2. newFixThreadPool：執行緒 Pool 只會有固定數量的執行緒再執行，如果啟動的數量超過 pool 的數量那執行緒就會被放入 Queue 等待被執行。

3. newSingleThreadExecutor：執行緒 pool 只會有一個執行緒可以執行

4. newScheduledThreadPool：執行緒 pool 會按照排程去執行執行緒

5. newSingleThreadScheduledExecutor：執行緒 pool 只會有一個執行緒可以按照 scheduler 的排程去執行