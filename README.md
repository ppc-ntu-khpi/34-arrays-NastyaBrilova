# Практична робота "Масиви, вирази, керування виконанням програми"

## Завдання: Знайти в масиві число, яке повторюється найбільшу кількість разів

### Методи классу ```Exercise```
<details>
  <summary>reveal</summary>
	
  ```java
/**
	 * Знаходить в массиві число, яке повторюється найбільшу кількість разів
	 * 
	 * @param arr массив
	 * @return Повертає число, яке в массиві повторюються найбільшу кількість разів
	 */
	public static int reveal(int[] arr) 
   {
		Map<Integer, Integer> nums = new HashMap<>();
		for (int number : arr) 
      {
			Integer i = nums.get(number);
			nums.put(number, i == null ? 1 : i+1);
		}	
		int max = Collections.max(nums.values());
		for (Map.Entry<Integer, Integer> number : nums.entrySet()) 
      {
			if (number.getValue() == max)
				return number.getKey();
		}
		return -1;
	}
  ```
  
</details>
<details>
  <summary>creature</summary>
	
  ```java
	private static final ThreadLocalRandom rnd = ThreadLocalRandom.current();
	
	/**
	 * Створює массив за вказаною довжиною і генерує його значення
	 * @param size довжина массива
	 * @return массив
	 */
	public static int[] creature(int size) 
   {
		int[] array = new int[size];
		for (int i = 0; i < size; i++) 
      {
			array[i] = rnd.nextInt(10);
		}
		return array;
	}
  ```
  
</details>

Результат:
----

![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-NastyaBrilova/blob/master/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%201.PNG)<br><br>
![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-coldbeatz/blob/master/Screenshot_18.png)<br><br>
![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-coldbeatz/blob/master/Screenshot_20.png)<br>
