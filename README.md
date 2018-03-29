# KotlinInAndroid
Kotlin在android中的应用

Kotlin 已经听说不是很久了是太久了，一直没时间学习，从本命年的今天开始，我将开始学习Kotlin在android中的应用。
已一款App为基础来学习Kotlin的用法，此文档记录我的学习路线

# **基本语法**

## **定义函数**

```
    /**
     * 有返回值的函数
     */
    fun total(a: Int, b: Int): Int {//a参数，Int类型
        return a + b
    }

    fun sum(a: Int, b: Int): Int = a + b
    public fun sum(a: Int, b: Int, c: Int): Int = a + b + c//public方法必须明确写出返回类型


    /**
     * 无返回值的函数
     * 如果返回值是Unit类型则可以省略，public方法一样
     */
    fun sum1(a: Int, b: Int): Unit {
        sum(2, 1)
    }

    public fun sum2(a: Int, b: Int) {
        sum(1, 3)
    }

    /**
     * 可变长参数函数
     */
    fun vars(vararg v: Int) {
        for (vt in v) {
            Log.e("打印", vt.toString())
        }
    }

    //测试
    fun text(text: Array<String>) {
        vars(1, 2, 3, 4, 5)//输出12345
    }

    /**
     * lambda匿名函数
     */
    fun lambdatext(args: Array<String>) {
        val sumLambda: (Int, Int) -> Int = { x, y -> x + y }
        Log.e("lambda匿名函数", sumLambda(1,3).toString())
    }
```

# **学习地址**

[Kotlin菜鸟教程](http://www.runoob.com/kotlin/kotlin-basic-syntax.html)