Node JS Open source, cross platfrom, JS run environment
open source -  source code is publicly available
cross platform - available on all platform windows mac linux

1993 - first web browser with user interface mosaic was released
1994 - devs of mosaic opened a company called Netscape and released Netscape Navigator
Problem was only static web pages to address this 1995 - they created javascript

Msft launched it's own internet explorer. However JS changed the way user interacted with web. So msft wanted to build their own language but there was no specification for them to follow.

1996 - msft reversed engineer and build JScript. However implementation was way different
This resulted in devs having difficulty to make website compatible with both browsers.


1996 - Netscape subitted JavaScript to ECMA international
ECMA called it ECMAscript as Oracle owned the trademark for Javascript.

ECMA-262 is language specification
ECMAscripts implements ECMA-262
JS builds on top of ECMAscript.

chrome's v8 engine - js engine by google. Every browser vendor have their own engine. It's written in C++.

You can embed v8 engine in your c++ program. So that essentially means you write c++ code with low level operations like handling file systems, network operations etc. and you can add all these to javascript. =====> creation of node js

![[Screenshot 2023-02-21 at 6.19.54 PM.png]]


![[Screenshot 2023-02-21 at 7.02.50 PM.png]]

All local modules  use iife under the hood.

![[Screenshot 2023-02-21 at 7.05.22 PM.png]]

**Module Caching:-**
![[Screenshot 2023-02-21 at 7.11.13 PM.png]]

functions are first class objects - function can be passed as argument to other function, it can be returned as value from other function

![[Screenshot 2023-02-21 at 10.59.57 PM.png]]

![[Screenshot 2023-02-22 at 1.00.40 PM.png]]

 ![[Screenshot 2023-02-22 at 5.16.52 PM.png]]

![[Screenshot 2023-02-27 at 1.18.44 PM.png]]

![[Screenshot 2023-02-27 at 1.19.07 PM.png]]

![[Screenshot 2023-02-27 at 1.21.54 PM.png]]![[Screenshot 2023-02-27 at 1.22.06 PM.png]]![[Screenshot 2023-02-27 at 1.22.20 PM.png]]

16 threads and 8 cores , os scheduler will schedule 2 threads per core and give them equal time by switching continuosly. So that's why 16 calls now take twice the time that 8 calls were taking as till 8 you can schedule one thread per core.![[Screenshot 2023-02-27 at 1.26.17 PM.png]]

![[Screenshot 2023-02-27 at 1.26.44 PM.png]]

**Event Loop:-**

![[Screenshot 2023-02-27 at 2.06.43 PM.png]]![[Screenshot 2023-02-27 at 2.14.28 PM.png]]

![[Screenshot 2023-02-28 at 12.27.34 AM.png]]

![[Screenshot 2023-02-28 at 12.27.51 AM.png]]

process.nextTick - goes to nextTick queue
Promise.resolve - goes to promise queue
setTimeout, setInterval - goes to timer queue

![[Screenshot 2023-02-28 at 12.30.34 AM.png]]

![[Screenshot 2023-02-28 at 12.32.09 AM.png]]

After every callback run in timer queue/ other queues controller again checks microtask queue for functions to execute.

Timer queue is actually a min heap ds.

i/o queue - many functions including readFile from fs module.

https://www.youtube.com/watch?v=RWCC4aWMlGw&list=PLC3y8-rFHvwh8shCMHFA5kWxD9PaPwxaY&index=45&ab_channel=Codevolution (important video)

setImmeditate - check queue

I/O queue keeps polling all operations and when they are finished then only it schedules the callbacks in i/o queue.

![[Screenshot 2023-02-28 at 12.44.18 AM.png]]

![[Screenshot 2023-02-28 at 12.51.53 AM.png]]


Clusture module enables creation of workers(child processes that run simultaneously) that share same server port.

Worker threads module - execute task parallel to main thread



**Working:** The way Libuv and the event loop work is based on the **Reactor Pattern**. In this pattern, **there is an Event queue and an Event demultiplexer**. The loop (i.e. the dispatcher) keeps listening for incoming I/O and for each new request, an event is emitted.

https://javascriptcentric.medium.com/top-50-nodejs-interview-questions-and-answers-for-2024-5e460dac7852
