# 答案

## 创建10条 "video1.mp4"

输入 'video1.mp4', 键入yy10p; 

## 使用命令将 video后面的数字修改为自增数字

在第二条数据中,使用 `ctrl+v`选中数字1,键入`9j`选择剩余所有数字; 键入`g`,`ctrl+a`,修改成功

## 使用宏命令将 videox.mp4 被双引号包含,并在结尾添加逗号

光标在第一条,输入 `qa`开始录入宏,使用寄存器`a`

使用`i`在行首插入`"`,`A`在行尾添加 `",`,返回NORMAL模式,按`q`结束录制

在第二行键入`V`选中行,`G`全选剩余行,在命令行模式输入`normal @a`使用宏命令,完成

## 使用宏命令，将每个video前面加上序号，eg: 1.

设置变量：命令模式设置变量i `:let i=1`, 设置成功后，可以在插入模式使用`ctrl+r=i`, 查看设置是否成功

录制宏：`qa`开始录制宏，在光标第一行首字母，`i`插入, `crtl+r =i`, 插入i，并加上`. `，`: let i+=1`, 让i自增 退出宏录制

批量操作：`V`,`G`选中第二行开始的剩余行，`:normal @a`执行宏命令

## 在练习打卡处,添加当天打卡结果,日期使用VIM命令插入

插入模式下,键入`ctrl-r`,输入`=strftime("%Y-%m-%d")`

## 将当前编辑文件目录下的文件列表、当前路径插入到当前编辑文件中
:r !ls
:r !pwd
:r ![linux command]

