无论是C语言还是C++, static变量的访问都需要加锁，但是在C语言中，static 变量的初始化在变异的时候就进行，所以函数内部不需要加锁去判断是否已经初始化。
但是CPP中，可以初始化为运行时的值，这个时候就需要加锁来保证这个变量初始化出来的值是安全的。

但是即使是在C+++中，只有初始化的时候是一个运行中的值的时候，才需要__cxa_guard_acquire() 来保证初始化多线程安全，如果是编译期间能确认的值那么就不要这个机制。