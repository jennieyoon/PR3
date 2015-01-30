/**
 * Provide a set of Array functions on an Array of ints
 * @author Jennie Yoon
 * @version CSE11-Winter2015-PR3
 */
public class IntArray11
{
  private int n, nElem, temp;
  private int[] smarsArray;
   
   
  /** 
   * 0-argument constructor. Valid instance of an Array of int,
   * no ints are stored in the array.
   */
  public IntArray11()
  {
    nElem = 0;
    n = 0;
    smarsArray = new int [0];
  }
   
  /** 
   * Store an array of size n. Initialize contents of the array to 
   * be 1..n 
   * @param size the number of elements to store in the array
   */
  public IntArray11(int size)
  {
    n = size;
    nElem = 0; //although we know what n is, don't know how many elements there actually are
               //so set it to 0
    smarsArray = new int[n];
  }
   
  /** 
   * Create an array of size n and store a copy of the contents of the
   * input argument
   * @param intArray array of elements to copy 
   */
  public IntArray11(int[] intArray)
  {
    n = intArray.length;
    smarsArray = new int[n];
    for (int i = 0; i < n; i++) {
      smarsArray[i] = intArray[i];
     }
  }
   
  /* Make a string representation */
  /**
   * Pretty Print  -- Empty String "[]"
   *                  else "[e1, e2, ..., en]"
   */
  @Override
  public String toString()
  {
    String result = "";
     
    for (int i = 0; i < n; i++) { //uses array length; different from number of elements!
      result += smarsArray[i];
      if (i < n - 1)
        result += ", ";
    }
     
    return "[" + result + "]";
  }
   
  /* Getters and Setters */
   
  /** get the number of elements stored in the array  
    * @return number of elements in the array
    */
  public int getNelem()
  {
    return nElem; //other class can access private variable nElem by "getting" it
  }
  /** get the Element at index  
    * @param index of data to retrieve 
    * @return element if index is valid else return 
    *   Integer.MIN_VALUE
    */
  public int getElement(int index)
  {
    if (index < 0 || index > n){
      return Integer.MIN_VALUE;
    }
    return smarsArray[index]; //index will come from user input in ArrayPlay
  }
   
  /** retrieve a copy of the stored Array
    * @return a deep copy of the Array. A new int array should be
    *   constructed of the correct size and values should
    *   copied into it.  
    */
  public int[] getArray()
  {
    int[] copyArray = new int[n];
     for (int i = 0; i < n; i++) {
      copyArray[i] = smarsArray[i];
     }
    return copyArray;
  }
   
  /** set the value of an element in the stored array
    * @param index of element to store. Must be a valid index 
    * @param element the data to insert in the array
    * @return true if element set was successful
    */
  public boolean setElement(int index, int element)
  {
    if(index < 0 || index >= n){
      System.out.println("BAD INPUT");
      return false;
    }
     
    smarsArray[index] = element;
     
    return true;
  }
   
  /** Insert an element at index in the array
    * @param index where to insert. Must be between 0 and number of
    *              elements in the array
    * @param element the data to insert in the array
    * @return true if element insertion was successful
    */
  public boolean insert(int index, int element)
  {
    if(index < 0 || index >= n){ 
      System.out.println("BAD INPUT");
      return false;
    }
     
    for (int i = n - 1; i > index; i--){
      smarsArray[i]=smarsArray[i - 1];
      //put element in index
    }
    return true;
   
   
  /** Delete an element at index
    * @param index of element to delete 
    * @return true if element deletion was successful, false otherwise
    */
  public boolean delete(int index)
  {
    n = smarsArray.length;
    for (int i = index; i < n - 1; i++){
      smarsArray[i] = smarsArray[i + 1];
    }
    return true;
  }
   
  /** reverse the order of the elements in the array 
    */
  public void reverse()
  {
    n = smarsArray.length;
    for (int i = 0; i < n / 2; ++i){
      int temp = smarsArray[i];
      smarsArray[i] = smarsArray[(n - 1) - i];
      smarsArray[(n - 1) - i] = temp;
    }
  }
   
  /** reverse the order of the elements in the array from start to
    *   end index 
    *   @param start beginning index of to start the reverse
    *   @param end ending index to end the reverse
    *   @return true if start and end index are valid, false otherwise
    *
    */
  public boolean reverse(int start, int end) //custom start and end points
  {
    n = smarsArray.length;
    if(0 > start || n < end){
      System.out.println("BAD INPUT");
    }
      
    for(int i = end - 1; i >= start; --i){
      smarsArray = new int[n];
    }
    return true;
  }
   
  /** swap two elements in the array 
    *   @param index1 index of first element 
    *   @param index2 index of second element
    *   @return true if index1 and index2 are valid, false otherwise
    *
    */
  public boolean swap(int index1, int index2)
  {
    temp = index1;
    index1 = index2;
    index2 = temp;
    return true;
  }
}
// vim: ts=4:sw=4:tw=78:
