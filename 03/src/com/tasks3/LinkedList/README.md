Створіть клас що описує зв'язний список. Клас повинен мати можливість додавання елементів та вилучення елементів. Додавання елементів відбувається в кінець списку, вилучення елементів відбувається за порядковим номером.Також створіть методи, що дозволяють отримати розмір списку та елемент за його порядковим номером.

Елементи списку повинні бути типу Node

class Node{
	private Node next;
	private Integer data;
	
	public Node() {
	}

	public Node getNext() {
		return next;
	}
	public void setNext(Node next) {
		this.next = next;
	}
	public Integer getData() {
		return data;
	}
	public void setData(Integer data) {
		this.data = data;
	}
}

Клас списку повинен мати наступну структуру:

public class LinkedList {
/* Конструктор без аргументів */
    public LinkedList() {}
/* Додати елемент в кінець списку */
    public void add(Integer data) {}
/* Отримати елемент по індексу, повертає null якщо такий елемент недоступний */
    public Integer get(int index) {}
/* Вилучення елементу за індексом, повертає true у разі успіху або false в іншому випадку */
    public boolean delete(int index) {}
/*Поверта розмір списку: якщо елементів в списку нема то повертає 0 (нуль)*/
    public int size() {}
}