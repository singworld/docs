# 选择排序

## 1. 写一个main方法 生成一些随机数组并打印

```Java
  //1. mian方法
  public static void main(String[] args) {

        int testTime = 50;
        int maxSize = 100;
        int maxValue = 100;
        boolean succeed = true;
        for (int i = 0; i < testTime; i++) {
//            生成随机数组
            int[] arr1 = generateRandomArray(maxSize, maxValue);
        }

        int[] arr = generateRandomArray(maxSize, maxValue);
        printArray(arr);
    }



    //2.生成随机数组的方法

    private static int[] generateRandomArray(int maxSize, int maxValue) {

        int[] arr = new int[(int) (Math.random()*(maxSize+1))];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = (int) (Math.random()*(maxValue+1)) - (int) (Math.random()*(maxValue+1));
        }
        return arr;

    }


    //3. 打印方法
    private static void printArray(int[] arr) {

        if(arr == null) return;

        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+" ");
        }
        System.out.println();

    }
````

执行打印结果
-35 30 -85 34 -40 -34 36 57 29 -11 22 71 -3 -3 -30 60 70 10 -14 
[点击查看执行结果](https://ideone.com/zgI5Su)

## 2.写选择排序
```java
   /**
     * 选择排序
     * @param arr
     */
    private static void selectionSort(int[] arr) {

        if(arr == null || arr.length <2) return;
        int n = arr.length;
//       // 0 ~ N-1  找到最小值，在哪，放到0位置上
//		// 1 ~ n-1  找到最小值，在哪，放到1 位置上
//		// 2 ~ n-1  找到最小值，在哪，放到2 位置上
        for (int i = 0; i < n-1; i++) {
            int minIndex = i;
            for (int J = i; J < n ; J++) {
                minIndex = arr[J] < arr[minIndex]?J:minIndex;
            }
            swap(arr,i,minIndex);

        }
    }

    private static void swap(int[] arr, int i, int minIndex) {
        int temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;

    }
```
执行结果
-25 -24 -26 -9 -19 -32 -3 -40 -78 0 21 49 -54 -27 -32 -19 -8 18 -43 77 12 -12 37 -69 24 87 6 -18 24 13 45 88 -90 19 -24 49 44 -50 34 22 -32 -37 12 -66 -47 -5 -14 -39 65 -15 6 -24 13 17 7 34 -85 -29 69 -9 -11 -27 
-90 -85 -78 -69 -66 -54 -50 -47 -43 -40 -39 -37 -32 -32 -32 -29 -27 -27 -26 -25 -24 -24 -24 -19 -19 -18 -15 -14 -12 -11 -9 -9 -8 -5 -3 0 6 6 7 12 12 13 13 17 18 19 21 22 24 24 34 34 37 44 45 49 49 65 69 77 87 88 


## 3.对数器
```java
 private static boolean isEqual(int[] arr1, int[] arr2) {
        if ((arr1 == null && arr2 != null) || (arr1 != null && arr2 == null)) {
            return false;
        }
        if (arr1 == null && arr2 == null) {
            return true;
        }
        if (arr1.length != arr2.length) {
            return false;
        }
        for (int i = 0; i < arr1.length; i++) {
            if (arr1[i] != arr2[i]) {
                return false;
            }
        }
        return true;

    }

    private static void comparator(int[] arr) {
        Arrays.sort(arr);
    }

    private static int[] copyArray(int[] arr) {
        if (arr == null) {
            return null;
        }
        int[] res = new int[arr.length];
        for (int i = 0; i < arr.length; i++) {
            res[i] = arr[i];
        }
        return res;
    }
```

执行结果
Nice!
[点击查看执行结果](https://ideone.com/TrATCq)