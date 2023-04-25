import static java.util.Arrays.sort;

public class StatsCalculator {
    /**
     * @description Instance variables for the constructor
     */
    private double[] array;
    private double[] sortedArray;
    private double[] outliers;
    /**
     * @description The default constructor makes an array with length 20
     */
    public StatsCalculator() {
        array = new double[20];
    }

    /**
     * @description constructor changes the values to custom ones
     */

    public StatsCalculator(double[] newValues) {

        array = newValues;
    }

    /**
     * @description Assigns the value of arr to sortedArray and then sorts that array least to greatest
     */
    public void sortData() {
        sortedArray = array;
        sort(sortedArray);

    }

    /**
     * @description Sort method to rearrange then find the max
     * @return Max value of array
     */
    public double calculateMax() {
        sortData();
        return sortedArray[array.length - 1];
    }

    /**
     * @description Sort method then finds the min
     * @return Min value of array
     */
    public double calculateMin() {
        sortData();
        return sortedArray[0];
    }

    /**
     * @description First quartile of array
     * @return the values of the first quartile
     */
    public double calculateFirstQuartile() {
        sortData();
        if (array.length % 4 <= 1) {
            double Quartile1 = ((sortedArray[(array.length / 2) / 2] + sortedArray[(array.length / 2) / 2 - 1]) / 2);
            return Quartile1;
        }
        return sortedArray[(array.length / 2) / 2];
    }

    /**
     * @description calculates the third quartile of the array
     * @return Third quartile value
     */
    public double calculateThirdQuartile() {
        sortData();
        if (array.length % 4 <= 1) {
            return ((sortedArray[array.length - 1 - (array.length / 2) / 2] + sortedArray[array.length - 1 - (array.length / 2) / 2 + 1]) / 2);
        }
        return sortedArray[array.length - 1 - (array.length / 2) / 2];
    }

    /**
     * @description Sort method then finds the median
     * @return The median
     */
    public double calculateMedian() {
        sortData();
        if (array.length % 2 == 0) {
            return (sortedArray[array.length / 2] + sortedArray[array.length / 2 - 1]) / 2;
        } else {
            return sortedArray[array.length / 2];
        }
    }

    /**
     * @description Sum of all values of the array
     * @return The sum
     */
    public double calculateSum() {
        double sum = 0;
        for (double added : array) {
            sum += added;
        }
        return sum;
    }

    /**
     * @description Divides the sum by the length of the array
     * @return The average value
     */
    public double calculateMean() {
        return (calculateSum() / array.length);
    }


    /**
     * @description Prints the value of the array at each element
     */
    public void print() {
        System.out.print("Data: ");
        for (int i = 0; i < array.length; i++){
            System.out.print(array[i] + " ");
        }
        System.out.println();
    }

    /**
     * @description Prints the value of the array at each element in ascending order
     */
    public void printSorted() {
        System.out.print("Sorted Data: ");
        sortData();
        for (int i = 0; i < array.length; i++){
            System.out.print(sortedArray[i] + " ");
        }
        System.out.println();
    }

    /**
     * @description Prints the minimum, first quartile, median, third quartile, maximum,to the console
     */
    public void printFiveNumberSummary() {
        System.out.println("The five number summary is: ");
        System.out.println("Minimum is: " + calculateMin());
        System.out.println("First Quartile is: " + calculateFirstQuartile());
        System.out.println("Median is: " + calculateMedian());
        System.out.println("Third Quartile is: " + calculateThirdQuartile());
        System.out.print("Maximum is: " + calculateMax()+"\n\t");

    }
}

