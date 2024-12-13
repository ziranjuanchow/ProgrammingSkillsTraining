python reload会把当前文件的变量清了呀!!!



## record
1. msys2->mingw64->python
   G:\msys64\mingw64\bin\python.exe -m venv
   不要用 python -m venv ,这样会默认linux的，而且pip和.exe有问题


import unreal
# 使用 ObjectIterator 遍历所有 ScriptStruct 类型
for obj in unreal.ObjectIterator(unreal.ScriptStruct):
    struct_name = obj.get_name()
    struct_path = obj.get_path_name()
    unreal.log("Struct Name: {}, Struct Path: {}".format(struct_name, struct_path))
    # 如果你只想查找特定名称的结构体，可以添加判断条件
    if struct_name == "MyStruct":
        unreal.log("Found MyStruct: {}".format(struct_path))
