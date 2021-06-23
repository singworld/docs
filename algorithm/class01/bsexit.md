# 二分查找
## 1.写一个二分查找
```java
   private static boolean exist(int[] arr, int value) {
        if(arr == null || arr.length ==0) return false;

        int L = 0;
        int R = arr.length-1;
        int mid = 0;

        while (L < R){
            // L + (R-L)/2  防止int溢出
            mid = L + ((R-L)>>1);
            if(arr[mid] == value){
                return true;
            }else if(arr[mid] > value){
                R = mid -1;
            }else{
                L = mid+1;
            }
        }

        return  arr[L] == value;
    }
```

## 2.写一个对数器
```java
    private static boolean testexit(int[] arr, int value) {

        for (int i :arr){
            if(i == value) return true;
        }
        return false;
    }
```

[点击查看执行结果](
https://ideone.com/IhAOAC)