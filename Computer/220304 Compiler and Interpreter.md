# Difference between compiler and interpreter

When I searched what the interpreter is, it was explained as "a computer program that directly executes instructions written in a programming or scripting language." But isn't it the same as a compiler? 

No, it's not. Both compilers and interpreters run programs after translating source codes written in advanced languages(that humans can understand) into machine languages, but it differs in the translating process.

A compiler takes a longer time in translating because it translates the entire program into machine languages at once. In the process it produces executive files using memories, so the execution time is faster than the interpreter. Used in C, C++, etc.

On the other hand, an interpreter translates only one statement at a time. This makes the time to translate much short, but the overall time to execute the process is much slower. Also, it doesn't generate an intermediary code or produces executive files. Hence, an interpreter is highly efficient in terms of its memory. Used in Python, Ruby, etc.
