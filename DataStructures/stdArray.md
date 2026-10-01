## std::array

This is C++’s standard library, souped‑up version of the classic C‑style array you get with [].
It behaves like a normal array in memory a contiguous block of elements but wrapped in a modern interface that plays nicely with the rest of the language.

It’s still a fixed‑size container, so you don’t get any resizing or dynamic growth.  In exchange you get a bunch of quality of life improvements over the raw C array.

The biggest upgrade is that std::array doesn’t decay into a pointer when you pass it around. It stays a real object, which means it knows its own size, it can be copied and assigned, and it works with iterators. You also get convenience functions like front(), back(), data(), and full compatibility with STL algorithms.

There is no additional runtime overhead It’s essentially a thin wrapper around a raw array but it does add a bit more syntactic weight. Because of that, you use std::array when the array needs to be passed around to multiple functions or integrated with other parts of your codebase. Raw C arrays still make sense when the array is tiny, local to a single function, and you’re laser‑focused on minimal syntax.