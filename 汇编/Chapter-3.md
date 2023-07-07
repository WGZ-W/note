## BIOS 是由 IBM 公司开发的

## 通用寄存器
```
    8个通用寄存器都可以使用 mov 操作
```

## bochs 的 magic breakpoint
```
    xchg bx， bx
    
    自动在这一句设置断点
```

## makefile 的 .PHONY
```
    每次都执行？
```

## nasm 的一些语法
```
    db
    dw
    dd
    loop 和 cx 搭配， cx = 0 跳出循环，cx 代表循环的次数
    
    [org 0x7c00] 将逻辑地址转化为物理地址，和标号配对使用
                 使标号的逻辑地址加上 org 的地址
```