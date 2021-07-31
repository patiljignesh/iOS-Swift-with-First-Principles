
# Grand Central Dispatch (GCD) framework

## GCD Framework built on top of theading

- Queue: FIFO
  - Serial Queue : Tasks in a queue are performed in order one at a time. 
  - Concurrent Queue  : All tasks begins in order but completion order is dependent on the tasks.
- By Default, every App gets:
  - 1 Serial Queue = 1 Thread only : Main queue
  - 4 Concurrent Queue: Background queue
  
> Main Thread: Keep it clean and speedy since UI runs in this thread.

## DispatchQueue
- This bring the loading of data from the background(Assume JSON from the internet) to the main thread by dispatching queue to the main thread. This is to make changes to the UI.
 
```
DispatchQueue.main.async {
  self.tableView.reloadData()
}

```

- This is to run the code in the background

```
DispatchQueue.global(qos: .background).async {
  //Code to run on the background.
}

```
