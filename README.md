# ogpiler

Og to C++17 transpiler.

## Requirements

* `og` in the path, from https://github.com/Champii/og
* `go2cpp` in the path, from https://github.com/xyproto/go2cpp

## Usage example

    ogpiler -o main.cpp main.og

## Installation

    install -Dm755 ogpiler /usr/bin/ogpiler

## Example transformation

Og
```
!main

import fmt

fn main -> fmt.Println("Hello, World!")
```

C++17
```cpp
#include <iostream>

auto main() -> int
{
    std::cout << "Hello, World!" << std::endl;
    return 0;
}

```

## General info

* Version: 0.0.0
* License: MIT
* Author: Alexander F. Rødseth &lt;xyproto@archlinux.org&gt;
