For this programming project checkpoint, you are to write a preemptive multithreading
package and a test case based on the single-buffer producer-consumer example.
Preemptive multithreading means the code for each thread does not need to explicitly do a
thread-yield (not to be confused with Python’s generator- yield ) in order to switch to
another thread, if any. Of course, it can also do ThreadYield() if it wants.
Also, depending on your implementation, you may or may not use a separate thread for the
thread manager. If so, then you may want to define your MAXTHREADS accordingly. All
other API should be the same. Actually, the ThreadYield() function should be available
for preemptive threads, too, because even though the OS can always preempt a thread, a
thread should still be able to voluntarily give up control.