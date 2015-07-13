# fs.cpp

string interpolation (c++11 udl)

```c++
fs::set("name", "park");
fs::set("robot", "annoying-o-tron");

std::cout<< "#{name}안녕 #{robot}로봇"_fs
// park안녕 annoying-o-tron로봇
```

```c++
std::string name = "park";
fs::watch("name", &name);

std::cout<< "#{name}"_fs
// park

name = "cho";

std::cout<< "#{name}"_fs
// cho

fs::unwatch("name");
```

non-string values
```c++
// using 'to_string.cpp'
fs::watch("level", 5);

std::cout<< "lv. #{level}"_fs
// lv. 5
```
