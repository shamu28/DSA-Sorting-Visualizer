import java.util.Arrays;
public class SortingVisualizer {
    public static void main(String[] args) {
        int[] arr = {12, 11, 13, 5, 6};
        System.out.println("Original Array:");
        printArray(arr);
        insertionSort(arr);
        System.out.println("\nSorted Array:");
        printArray(arr);
    }
    static void insertionSort(int[] arr) {
        for (int i = 1; i < arr.length; i++) {
            int key = arr[i];
            int j = i - 1;
            System.out.println("\nStep " + i + ":");
            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j--;
                printArray(arr);
            }
            arr[j + 1] = key;
            printArray(arr);
        }
    }
    static void printArray(int[] arr) {
        System.out.println(Arrays.toString(arr));
    }
}
