---
title: "Resources on CUDA programming"
date: 2018-07-06
---

# Resources on CUDA programming

Here is a list of resources for CUDA programming, in particular, in C. 

# Basic

Perhaps the best beginning guide is written by [Mark Harris, ](https://devblogs.nvidia.com/author/mharris/)currently spot 10 articles. They start from simple HelloWorld-type of example. But goes deeper and deeper into important topic such as data transfer optimization, as well as shared memory. The final 3 articles focus on optimizing real-life applications such as matrix transpose and finite-difference method. 
1. [An Easy Introduction to CUDA C and C++](https://devblogs.nvidia.com/easy-introduction-cuda-c-and-c/)
2. [How to Implement Performance Metrics in CUDA C/C++](https://devblogs.nvidia.com/how-implement-performance-metrics-cuda-cc/)
3. [How to Query Device Properties and Handle Errors in CUDA C/C++](https://devblogs.nvidia.com/how-query-device-properties-and-handle-errors-cuda-cc/)
4. [How to Optimize Data Transfers in CUDA C/C++](https://devblogs.nvidia.com/how-optimize-data-transfers-cuda-cc/)
5. [How to Overlap Data Transfers in CUDA C/C++](https://devblogs.nvidia.com/how-overlap-data-transfers-cuda-cc/)
6. [An Even Easier Introduction to CUDA](https://devblogs.nvidia.com/even-easier-introduction-cuda/)
7. [Unified Memory for CUDA Beginners](https://devblogs.nvidia.com/using-shared-memory-cuda-cc/)
8. [An Efficient Matrix Transpose in CUDA C/C++](https://devblogs.nvidia.com/efficient-matrix-transpose-cuda-cc/)
9. [Finite Difference Methods in CUDA C/C++, Part 1](https://devblogs.nvidia.com/finite-difference-methods-cuda-cc-part-1/)
10. [Finite Difference Methods in CUDA C/C++, Part 2](https://devblogs.nvidia.com/finite-difference-methods-cuda-c-part-2/)

## Intermediate

A very important document on the internal of Nvidia chips as well as CUDA programming models would be [CUDA C Programming Guide.](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#hardware-implementation)

In version 9, the document has around 90 pages of content with the rest of 210 pages to be appendices. I found it very helpful to read through the content and look up the appendices from time to time.

The next document which is useful is[CUDA Best Practice Guide](https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/index.html#abstract). You will find a lot of performance tuning tips there in the guide.

If you want to profile a CUDA application, you must use nvprof and the Visual profiler, you can find their manuals [here](https://docs.nvidia.com/cuda/profiler-users-guide/). Two other very good links to read are [here](https://people.maths.ox.ac.uk/gilesm/cuda/lecs/NV_Profiling_lowres.pdf) and [this one by Mark Harris](https://devblogs.nvidia.com/cuda-pro-tip-nvprof-your-handy-universal-gpu-profiler/).

If you want to read a very good textbook, consider to read "[Professional CUDA C Programming](https://www.amazon.com/Professional-CUDA-Programming-John-Cheng/dp/1118739329)" which I think is the best book on the topic. You will learn what the author called "profile-based programming" which is perhaps the best way to proceed in CUDA programming. 

## Others

[PTX ISA](https://docs.nvidia.com/cuda/parallel-thread-execution/index.html)

[Inline PTX Assembly ](https://docs.nvidia.com/cuda/inline-ptx-assembly/index.html)

[CuBLAS: ](https://docs.nvidia.com/cuda/cublas/index.html#abstract)indispensible for linear algebra. The original Nvidia documentation is good. But you may also find this little gem on "[cuBLAS by example](https://developer.nvidia.com/sites/default/files/akamai/cuda/files/Misc/mygpu.pdf)" useful. 

##
