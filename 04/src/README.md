Використовуючи наведені нижче класи змініть порядок сортування на зворотній.

Наведений нижче код виводить:

0 1 2 3 4 5 6 10 10

Потрібно щоб він вивів:
10 10 6 5 4 3 2 1 0

Дозволено змінювати лише код між рядками

//Change your code here

//Change your code here
Порівняння відбувається за допомогою класу:

public class Comparator {
	public int compare(int a, int b){
		if (a>b) {
			return 1;
		} else if (a == b){
			return 0;
		} else {
			return -1;
		}
	}
}

public class Sort {
	private static void sort(int[] array, Comparator comp) {
		for (int gap = array.length / 2; gap > 0; gap /= 2) {
			for (int i = gap; i < array.length; i++) {
				int val = array[i];
				int j;
				for (j = i; j >= gap && comp.compare(array[j - gap], val) > 0; j -= gap) {
					array[j] = array[j - gap];
				}
				array[j] = val;
			}
		}
	}

	public static void main(String[] args){
		int[] array = {1,5,2,4,10,6,0,3,10};
		Comparator comp = new Comparator();
		
		//Change your code here
		sort(array, comp);
		//Change your code here
		
		for (int i = 0; i < array.length; i++) {
			System.out.print(array[i] + " ");
		}
	}
	
}  