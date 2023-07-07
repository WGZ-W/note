# 配置环境

## 在Linux上安装bochs（建议参考 bochs-install.md）
```
    $> sudo apt install bochs
    $> sudo apt install bochs-x
```

## 创建磁盘
```
    $> bximage
```

## 配置bochs
```
    display_library:x, options=“gui_debug”
    Ata0-master……
    Boot : disk
```

## 编译asm文件
```
    $> nasm hello.asm -o hello.bin 
```

## 将bin文件写入image文件，（写入硬盘）
```
    $> dd if=hello.bin of=master.img bs=512 count=1 conv=notrunc
```
## 安装qemu
```
    Sudo apt install qemu
    Sudo apt install qemu-utils
```
## 将image文件转化为VMware的vmdk文件
```
    $> qemu-img convert -O vmdk master.img master.vmdk
```

## 
## 
##

## hello.asm基本语法
```
    Mov ax, 0xb800
    Mov ds, ax
    
    Mov byte[0], ‘T’
    
    Halt:
        Jmp halt
        
    Times 510 - ($ - $$) db 0       // times 重复，db 填入一个字节
    Db 0x55, 0xaa                   // $表示当前行的字节数
                                    // $$表示当前段的开始位置 
```