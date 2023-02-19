# Task1
Number of distinct elements, Number of elements, min value , max value

import java.util.*;

public class Task1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Please enter a list of integers (separated by spaces):");
        String input = scanner.nextLine();

        String[] inputArray = input.split(" ");

        int[] intArray = new int[inputArray.length];

        for (int i = 0; i < inputArray.length; i++) {
            intArray[i] = Integer.parseInt(inputArray[i]);
        }

        Arrays.sort(intArray);

        int count = intArray.length;
        int distinctCount = 0;
        int min = intArray[0];
        int max = intArray[intArray.length - 1];

        System.out.print("Distinct elements: ");

        for (int i = 0; i < intArray.length; i++) {
            if (i == 0 || intArray[i] != intArray[i - 1]) {
                System.out.print(intArray[i] + " ");
                distinctCount++;
            }
        }

        System.out.println("\nNumber of elements: " + count);
        System.out.println("Number of distinct elements: " + distinctCount);
        System.out.println("Minimum value: " + min);
        System.out.println("Maximum value: " + max);

        scanner.close();
    }
}
