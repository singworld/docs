## 1.写一个插入排序
```java
	 /**
     * 插入排序
     * @param arr
     */
    private static void insertionSort(int[] arr) {

        if(arr == null || arr.length <2) return;
        int n = arr.length;
//        0-i 上有序
        for (int i = 1; i < n; i++) {
            for (int j = i-1; j>=0 && arr[j] >arr[j+1] ; j--) {
                swap(arr,j,j+1);
            }

        }
    }
```



[点击查看执行结果](
https://ideone.com/5V6T2E)