# What is this?

This is a lightweight wrap for [Google's Brotli compression library](https://github.com/google/brotli), in C++ style.

# How to use?

It is very simple. Just see the example.

```c++
# include <brotli-cpp.hpp>
# include <iostream>
int main()
{
    std::string origin = "hello world!";
    std::string compressed = brotli::compress(origin);
    std::string decompressed = brotli::decompress(compressed);
    std::cout << std::boolalpha << (origin == decompressed);
    return 0;
}
```

When compile, do not forget to add `-lbrotlienc -lbrotlidec`.
