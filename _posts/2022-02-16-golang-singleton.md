# 单例模式

- 懒汉模式：指全局的单例实例在第一次被使用时构建

```jsx
1  type singleton struct{}
 2  var ins *singleton
 3  var mu sync.Mutex
 4  func GetIns() *singleton{  
 5  　　if ins == nil {
 6     　　mu.Lock()
 7        defer mu.Unlock()
 8        if ins == nil {
 9       　　ins = &singleton{}
10        }
11     }
12     return ins
13 }

// 双重加锁，避免每次加锁
```

- 饿汉模式：指全局的单例实例在类装载时构建

```jsx
1 type singleton struct{}
2 var ins *singleton = &singleton{}
3 func GetIns() *singleton{
4     return ins
5 }
```

- sync.Once实现

```jsx
1 type singleton struct{}
2 var ins *singleton
3 var once sync.Once
4 func GetIns() *singleton {
5     once.Do(func(){
6         ins = &singleton{}
7     })
8     return ins
9 }
```
