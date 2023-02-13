# Cpp_Concurrent_Programming_Wait_For
The wait_for method is a member function of the std::condition_variable class in the C++ Standard Library, used for waiting for a condition to be met with a timeout.

The wait_for function takes three arguments:

A reference to a std::unique_lock on the mutex that protects the shared data.
A std::chrono::duration that specifies the maximum amount of time to wait for the condition.
A callable object (such as a lambda expression) that returns a value that can be converted to bool, which represents the condition being waited for.
The function atomically releases the lock on the mutex, waits for the condition to be notified, 
and then reacquires the lock. If the condition is notified within the specified timeout, wait_for returns std::cv_status::no_timeout. 
If the timeout expires before the condition is notified, wait_for returns std::cv_status::timeout.
