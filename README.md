# sort_012

package elclipse;
import java.util.*;
public class sort_012 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		int a[]= {0,1,2,0,1,0,1,2,1,1,0,2,0,0};
		int low=0;
		int mid=0;
		int high=a.length-1;

		while(mid<high) {
			switch(a[mid]) {
			case 0:
				swap(a,low,mid);      //swapping the elements
				low++;
				mid++;
				break;
			case 1:
				mid++;
				break;
			case 2:
				swap(a,mid,high);     ///swapping the elements
				high--;
				break;}
		}

		System.out.print(Arrays.toString(a));   ///conveerting arrays to string
	}
	public static void swap(int a[],int low,int high) {
		int temp;
		temp=a[low];
		a[low]=a[high];
		a[high]=temp;
	}
}


//  time complexity of the program O(n);
