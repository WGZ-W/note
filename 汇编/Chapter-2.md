# Hello world

    bios将启动引导区代码加载到 0x7c00 的位置
    0x7c00 - 0x7dff 是加载主引导扇区的位置
    
    0xb8000 是文本显示区域

##
## 8086的访问内存方式
```
    Ds << 4 + eax(偏移量)
    
    默认访问内存为取数据，访问数据段，使用ds段寄存器
```
## 实现hello world代码
```
    Mov ax, 3
    Int 0x10            // 设置显示模式为文本显示
    
    mov ax, 0xb800
    Mov ds, ax
    
    Mov byte[0], ‘h’
    Mov byte[2], ‘e’
    ……
                        // 显示文本为两个字节，第一个字节显示字符，
                        // 第二个字符显示字符的样式
    
```
