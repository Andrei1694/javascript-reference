# Java
#### Access modifiers
![Image of Yaktocat](./Java/modif.png)
* A private member (i) is only accessible within the same class as it is declared.
* A member with no access modifier (j) is only accessible within classes in the same package.
* A protected member (k) is accessible within all classes in the same package and within subclasses in other packages.
* A public member (l) is accessible to all classes (unless it resides in a module that does not export the package it is declared in).
### Design Patterns
#### Singleton
* https://www.journaldev.com/1377/java-singleton-design-pattern-best-practices-examples

```java
public class Main {

class SingletonExample {

    private static SingletonExample INSTANCE = null;

    private SingletonExample() {
        System.out.println("Singleton Created");
        System.out.println(this.hashCode());
    }

    public static SingletonExample getInstance(){
        if(INSTANCE == null){
            INSTANCE = new SingletonExample();
            
            return INSTANCE;
        }
        return INSTANCE;
    }
}
```
#### Thread Safe Bill Pugh Singleton Implementation

```java
public class BillPughSingleton {

    private BillPughSingleton(){}
    
    private static class SingletonHelper{
        private static final BillPughSingleton INSTANCE = new BillPughSingleton();
    }
    
    public static BillPughSingleton getInstance(){
        return SingletonHelper.INSTANCE;
    }
}
```
#### 

    
