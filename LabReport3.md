# Lab Report 2 
## Aidan Rikic

**Part1**   
I'm choosing `reversedInPlace` in `ArrayExamples`  
1.  
`@Test 
  public void testReverseInPlace2(){
    int[] exArray = { 1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(exArray);
    assertArrayEquals(new int[]{5, 4, 3, 2, 1}, exArray);
  }`  
2.  
`@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}`  
3.  
![Image](labReport2_ss1.png)
![Image](labReport2_ss2.png)  
4.  
Failing code:  
`static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }`  
Working Code:  
`static void reverseInPlace(int[] arr) {
    int[] placeHolder = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = placeHolder[arr.length - i - 1];
    }
  }`  
5.  
The issue with the original code was that it was changing the array as it was iterating through the array. This changes the ints in the array before they are even swapped, and therefore messes up the back half of the array. In order to fix this, we create a placeholder array and swap the numbers there `arr` isn't affected while iterating through. 

  



