public class Main {
    public static void main(String[] args) {
        int[] arr = {4, 1, 7, 7, 5};
        int firstMax = Integer.MIN_VALUE;
        int secondMax = Integer.MIN_VALUE;

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] > firstMax) {
                secondMax = firstMax;
                firstMax = arr[i];
            } else if (arr[i] > secondMax && arr[i] < firstMax) {
                secondMax = arr[i];
            }
        }

        System.out.println("Second largest: " + secondMax);
    }
}
