# Graph visualiser

Uses simulated annealing to draw nice looking draphs (or at least attempt to).
The algorithm is based on _Drawing Graphs Nicely Using Simulated Annealing_ by
Davidson and Harel.

Requires C++11 and cairo. The code is very experimental.

Some examples of drawn graphs can be found under the `examples` directory.

## Building

```bash
clang++ -Wall -O2 -std=c++11 main.cpp `pkg-config --cflags --libs cairo`
```

## TODO

1. [x] Upload some example images
2. [ ] More graph constructions.
    * [x] Consider some randomly generated graphs.
3. [ ] Interactive graphical user interface. Animate the SA process.
4. [ ] Faster energy evaluation. Needs some acceleration structure.
    * [ ] In most cases we don't have to check vertex against every other.
    * [ ] Maybe it's possible to avoid having to check edge against every other.
    * [ ] Alternatively, SIMD can offer near 4 fold speedup.
5. [ ] Thread safe and faster random numbers.
6. [ ] Structure the code better.
