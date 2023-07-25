# C++

## vector

### 1、引入

```cpp
#include<vector>
```

### 2、创建数组

```cpp
vector <int> v(10,2)
vector <int> v(10)
vector <int> v
```

### 3、分配数组大小

```cpp
v.resize(length)
```

### 4、末尾添加新数据

```cpp
v.push_back(data);
```

### 5、迭代器

```cpp
for(auto p=c.begin();p!=c.end();p++)
{
	code...
}
```

注意要切换到C++11

## set

set是集合，它里面的元素各不相同，而且元素会按照从小到大顺序

### 1、引入

```c++
#include<set>
```

### 2、创建集合

```cpp
set <int> s;
```

s后面不可以加内容

### 3、处理

```cpp
s.insert(data);	//插入
s.find(data);	//返回一个指针
s.erase(data);	//删除
```

## map（键值对）

map是键值对，他会自动将所有的键值对从小到大排列

### 1、引入

```cpp
#include<map>;
```

### 2、创建

```cpp
map <string,int> m;
```

### 3、处理

```cpp
m["hello"] = 2;		//添加
cout<<m["world"];	//访问,如果有就返回值，否则返回0
迭代器，获取值时类似结构体指针//遍历
m.size();		//获取长度
```

#### 迭代器

```cpp
map <string,int> m;
m["hello"] = 2;
m["world"] = 3;
for(auto p=m.begin();p!=m.end();p++)
{

}
```

## stack（栈）

特点：先进后出

### 1、引入

```cpp
#include<stack>
```

### 2、创建栈

```cpp
stack <int> s;
```

### 3、处理

```cpp
s.push(i);	//压栈
m.pop();	//出栈
s.top();	//访问栈顶
m.size();	//获取长度
```

## queue（队列）

先进先出，后进后出

### 1、引入

```cpp
#include<queue>
```

### 2、创建栈

```cpp
queue <int> s;
```

### 3、处理

```cpp
s.push(i);	//压栈
m.pop();	//出栈
s.front();	//访问队首
s.back();	//访问队尾
m.size();	//获取长度
```

## unordered_map和unordered_set

### 1、特点

是不会排序的map和set

## Sort函数

### 1、引入

```cpp
#include<algorithm>
```

### 2、使用

```cpp
sort(m.begin(),m.end());
```

可将数组从小到大排序

### 3、定义cmp函数

```cpp
bool cmp(int x,int y)
{
	return x>y;
}
int main(){
	sort(v.begin(),v.end(),cmp);
}
```

如果cmp返回值为假，则交换两个数的顺序。

```cpp
struct stu
{
	string name;
	int age;
}
bool cmp(stu a,stu b)
{
	if(a.age != b.age)
		return a.age < b.age;
	else
		return a.name < b.name;
}
int main()
{
	stu s[3];
	for(int i=0;i<3;i++)
		cin >> s[i].name >> s[i].age;
	sort(s,s+3,cmp);
	for(int i=0;i<3;i++)
	{
		cout << s[i].name << " " << s[i].age << endl;
	}
}
```
