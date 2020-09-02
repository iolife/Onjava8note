1. java 不继承私有字段 https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html#:~:text=Private%20Members%20in%20a%20Superclass,be%20used%20by%20the%20subclass.
2. 可通过public protect 方法间接访问父类 private 字段
3. java 构造函数 先初始化 父类的成员 -> 父类 构造函数 ->子类
   在继承中 不要在父类的构造函数中调用 重载的方法 可调用final private 不可重载的方法
4. Arrays.asList() 的输出作为一个 List ，但是这里的底层实现是数组，没法调整大小。如果尝试在这个 List 上调用 add() 或 remove()，由于这两个方法会尝试修改数组大小，所以会在运行时得到“Unsupported Operation（不支持的操作）”错误：
   ```
        public static <T> List<T> asList(T... a) {
        return new ArrayList<>(a);
    }
    ```

