#  剑指offer---面试题2

Singleton单例模式Java实现

==C++中其他几种实现方式暂时待定==

1. 饿汉式单例模式
```
public class S1 {
	
    private static final S1 instance=new S1();  
    //私有构造函数  
    private S1() {}  
    public static S1 getInstance() {  
        return instance;  
    }  
}
```

2. 懒汉式单例模式
```

public class SingletonClass {  
    private static SingletonClass instance=null;  
//私有构造函数  
    private SingletonClass() {}  
    public synchronized static SingletonClass getInstance() {  
        if(instance==null) {  
            instance=new SingletonClass();  
        }  
        return instance;  
    }  
}
```
