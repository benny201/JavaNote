# Java Review － 1

## 数据类型大小
* byte: 8 bit
* short: 16 bit
* int: 32 bit
* long: 64 bit
* doubleL 64 bit
* java数据类型的大小不已系统而变，强移植能力
* 封装类／基本类

## bitwise operation
* << 左移几位就是乘几次2


## 堆内存 heap／栈内存 stack
### 栈内存
* 局部变量都放在栈内存中;
* 存储引用对象

### 堆内存
* 存储对象的实际内容；
* 没有对象指向它时会被回收；

## 主方法
```java
public static void mian(String[] args) {

}
```

## 再写一次选择排序

```java
public class Solution{
	public void solution(int[] nums) {
		if (nums == null) {
			return null;
		}

		for (int i = 0; i < nums.length; i++) {
			for (int j = 0; j <= i; j++) {
				if (nums[i] > nums[j]) {
					int temp = nums[i];
					nums[i] = nums[j];
					nums[j] = temp;
				}
			}
		}

	}
}
```

## 再写一次冒泡排序
```java
public class Solution{
	public void solution(int[] nums) {
		if (nums == null) {
			return ;
		}

		for (int i = 0; i < nums.length; i++) {
			for (int j = 0; j < nums.length - i - 1; j++) {
				if (nums[j] > nums[j + 1]) {
					int temp = nums[j + 1];
					nums[j + 1] = nums[j];
					nums[j] = nums[j + 1];
				}
			}
		}
	}
}
```
