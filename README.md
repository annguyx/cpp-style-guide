# Style Guide

Foobar is a Python library for dealing with word pluralization.

## Header Files

Thường thì mọi file .cpp nên đi chung với một .h.

Sử dụng file .h đúng cách có thể giảm kích thước, tối ưu tốc độ.

Áp dụng các rule dưới đây để tối ưu tối đa chương trình.

## The #define guard

[Định nghĩa](https://en.wikipedia.org/wiki/Include_guard)

Mọi header file đều phải có #define guard. Format theo công thức \_(Tên Project)\_(path)\_(File)\_H\_

ví dụ file có đường dẫn /project/todolist/Classes/ui/button.h thì #define guard sẽ là:

```C++
#ifndef FOO_BAR_BAZ_H_
#define FOO_BAR_BAZ_H_

...

#endif  // FOO_BAR_BAZ_H_
```

## Self-contained Headers and include what you use

## Names and Order of Includes

Thứ tự include headers: Related header, C System Headers, C++ standard library headers, Cocos2dx Headers, project's headers. Ngăn cách giữa các nhóm headers này bằng 1 blank line.

Ví dụ:

File có đường dẫn foo/server/fooserver.cpp

```C++
//Đây là related header
#include "foo/server/fooserver.h"

//Đây là C System Headers
#include <sys/types.h>
#include <unistd.h>

//Đây là C++ standard library headers
#include <string>
#include <vector>

//Đây là những file project's headers
#include "base/basictypes.h"
#include "base/commandlineflags.h"
#include "foo/server/bar.h"
```
