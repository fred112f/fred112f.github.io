# I is good
```package arraysandloops;
import java.util.Random;

public class ArraysAndLoops {
    public static void main(String[] args) {
        System.out.println("The code has started executing…");
        int [] numbers= new int[17];
        populateArray(numbers);
	printArray(numbers);
        System.out.println("Sum of the list is:" +sumOfList(numbers));
        System.out.println("Max number in the list is:" +maxNumber(numbers));
        System.out.println("These numbers are duplicated: "+duplicatedValues(numbers));
        System.out.println("Palindrome or not? "+palindromeTest(numbers));
        printArray(find(numbers,1));}
    
    static void printArray(int [] list){
        String numberList;
	for(int i=0;i<list.length;i++){
            if(i==0){
		System.out.print("[");}
            System.out.print(list[i]+",");
            if(i==list.length-1){
                System.out.print("]");}}
            System.out.println("");}
    
    static void populateArray(int[] list){
        Random randomNumber=new Random();
            for(int i=0;i<list.length;i++){
		list[i]=randomNumber.nextInt(5)+1;}}
    
    static int sumOfList(int[]list){
        int sum=list[0];
        for(int i=1;i<list.length;i++){
            sum+=list[i];}
        return sum;}
    
    static int maxNumber(int[]list){
        int tempMax=list[0];
        for(int i=1;i<list.length;i++){
            if(list[i]>tempMax){
                tempMax=list[i];}}
        return tempMax;}
    
    static Boolean duplicatedValues(int[]list){
        for(int i=0;i<list.length;i++){
            for(int a=0;a<list.length;a++){
                if(i!=a){
                    if(list[i]==list[a]){
                        return true;}}}}
        return false;}
    
    static boolean palindromeTest(int[]list){
        boolean palindrome=true;
        for(int i=0;i<list.length/2;i++){
            if(list[i]!=list[list.length-1-i]){
                palindrome=false;}}
        return palindrome;}

    static int[] find(int[] list, int value){
        int count=0;
        int []index=new int[list.length];
        for(int i=0;i<list.length;i++){
            index[i]=-1;}
        for(int i=0;i<list.length;i++){
            if(value==list[i]){
                index[count]=i;
                count++;}}
        return index;}
}
```
    
