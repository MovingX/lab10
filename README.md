<h1 align="center"> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="center">Лабораторная работа №10</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="right">Выполнил: Морошкин Максим Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>
<br>
<br>
<br>
<br>
<br>
<br>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">Задачи на JavaScript</p>

<h2>Цели и задачи</h2>
Задачи:
1.	Напишите функцию, которая найдёт числа в массиве, которые делятся на заданное число. 
2.	Нужно написать функцию, которая проверяет, являются ли две строки анаграммами, причем регистр букв не имеет значения. Учитываются лишь символы; пробелы или знаки препинания в расчет не берутся.
3.	Нужно написать функцию, принимающую строку в качестве аргумента и возвращающую количество гласных, которые содержатся в строке.
Гласными являются «a», «e», «i», «o», «u».
4.	Треугольник. Напишите цикл,  выводит такой треугольник:
#
##
###
####
#####
######
#######
5.	FizzBuzz. Напишите программу, которая выводит через console.log все числа от 1 до 100, с двумя исключениями. Для чисел, нацело делящихся на 3, она должна выводить ‘Fizz’, а для чисел, делящихся на 5 (но не на 3) – ‘Buzz’.Когда сумеете – исправьте её так, чтобы она выводила «FizzBuzz» для всех чисел, которые делятся и на 3 и на 5.
6.	Шахматная доска. Напишите программу, создающую строку, содержащую решётку 8х8, в которой линии разделяются символами новой строки. На каждой позиции либо пробел, либо #. 
7.	Минимум. Напишите функцию min, принимающую два аргумента, и возвращающую минимальный из них.
8.	Рекурсия. Ноль чётный. Единица нечётная. У любого числа N чётность такая же, как у N-2. Напишите рекурсивную функцию isEven согласно этим правилам. Она должна принимать число и возвращать булевское значение. Потестируйте её на 50 и 75. Попробуйте задать ей -1. Почему она ведёт себя таким образом? Можно ли её как-то исправить?
9.	Считаем бобы. Символ номер N строки можно получить, добавив к ней .charAt(N) ( “строчка”.charAt(5) ) – схожим образом с получением длины строки при помощи .length. Возвращаемое значение будет строковым, состоящим из одного символа (к примеру, “к”). У первого символа строки позиция 0, что означает, что у последнего символа позиция будет string.length – 1. Другими словами, у строки из двух символов длина 2, а позиции её символов будут 0 и 1.Напишите функцию countBs, которая принимает строку в качестве аргумента, и возвращает количество символов “B”, содержащихся в строке.Затем напишите функцию countChar, которая работает примерно как countBs, только принимает второй параметр — символ, который мы будем искать в строке (вместо того, чтобы просто считать количество символов “B”). Для этого переделайте функцию countBs.
10.	Сумма диапазона.  Напишите функцию range, принимающую два аргумента, начало и конец диапазона, и возвращающую массив, который содержит все числа из него, включая начальное и конечное.Затем напишите функцию sum, принимающую массив чисел и возвращающую их сумму. Запустите указанную выше инструкцию и убедитесь, что она возвращает 55.В качестве бонуса дополните функцию range, чтобы она могла принимать необязательный третий аргумент – шаг для построения массива. Если он не задан, шаг равен единице. Вызов функции range(1, 10, 2) должен будет вернуть [1, 3, 5, 7, 9]. Убедитесь, что она работает с отрицательным шагом так, что вызов range(5, 2, -1) возвращает [5, 4, 3, 2].
11.	Обращаем массив вспять. Напишите две функции, reverseArray и reverseArrayInPlace. Первая получает массив как аргумент и выдаёт новый массив, с обратным порядком элементов. Вторая работает как оригинальный метод reverse – она меняет порядок элементов на обратный в том массиве, который был ей передан в качестве аргумента. Не используйте стандартный метод reverse.
12.	Глубокое сравнение. Оператор == сравнивает переменные объектов, проверяя, ссылаются ли они на один объект. Но иногда полезно было бы сравнить объекты по содержимому. Напишите функцию deepEqual, которая принимает два значения и возвращает true, только если это два одинаковых значения или это объекты, свойства которых имеют одинаковые значения, если их сравнивать рекурсивным вызовом deepEqual. Чтобы узнать, когда сравнивать величины через ===, а когда – объекты по содержимому, используйте оператор typeof. Если он выдаёт “object” для обеих величин, значит нужно делать глубокое сравнение. Не забудьте об одном дурацком исключении, случившемся из-за исторических причин: “typeof null” тоже возвращает “object”.
13.	Свертка. Используйте метод reduce в комбинации с concat для свёртки массива массивов в один массив, у которого есть все элементы входных массивов.





<h2>Решение задач</h2>

```html
	<body>

		<style>
		td {
			width: 25px;
			height: 25px;
		}

		.white {
			background-color: #ffffff;
		}

		.black {
			background-color: #000000;
		}
		</style>
		
		<div class="Block1">
			<button onclick="task1(5)">Задача 1</button><br>
			<button onclick="task2('MaKs im', 'Kam Sim')"> Задача 2</button><br>
			<button onclick="task3('Hello, World!')">Задача 3</button><br>
			<button onclick="task4(7)">Задача 4</button><br>
			<button onclick="task5()">Задача 5</button><br>
			<button onclick="task6()">Задача 6</button><br>	
			<button onclick="task7(777, 7777)">Задача 7</button><br>

			<button onclick="task8(50)">Задача 8 - значение 50</button><br>
			<button onclick="task8(75)">Задача 8 - значение 75</button><br>
			<button onclick="task8(-1)">Задача 8 - значение -1</button><br>			
			
			<button onclick="countBs('BBC')">Задача 9 - 'BBC'</button><br>	
			<button onclick="countChar('kakkerlak', 'k')">Задача 9 - 'kakkerlak', 'k'</button><br>	
			
			<button onclick="alert(sum(range(1, 10)))">Задача 10 - sum(range(1, 10))</button><br>
			<button onclick="alert(range(1, 10, 2))">Задача 10 - range(1, 10, 2)</button><br>	
			<button onclick="alert(range(5, 2, -1))">Задача 10 - range(5, 2, -1)</button><br>
			
			<button onclick="alert(reverseArray(1, 2, 3, 4, 5))">Задача 11 - reverseArray(1, 2, 3, 4, 5)</button><br>
			<button onclick="alert(reverseArrayInPlace(1, 2, 3, 4, 5))">Задача 11 - reverseArrayInPlace(1, 2, 3, 4, 5)</button><br>
			
			<button onclick="alert(deepEqual({ a: 1, b: 2 },{ a: 1, b: 2 }))">Задача 12 - deepEqual({ a: 1, b: 2 },{ a: 1, b: 2 }))</button><br>			
			<button onclick="alert(deepEqual({ a: 1, b: 2 },{ a: 2, b: 2 }))">Задача 12 - deepEqual({ a: 1, b: 2 },{ a: 2, b: 2 })</button><br>
			
			<button onclick="alert(task13())">Задача 13</button><br>
			<div id="result">Тут будет ответ!!!</div>			
		</div>
		
		<script>
		function task1(n) {
		var arr = [10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,30];
		var result ="";
		for (var i = 0; i < arr.length; i++) {
			if (arr[i] % n === 0) {
			result += arr[i] + " ";
			}
		}
		document.getElementById('result').innerHTML = result;
		}
		
		function task2(str1, str2) {
			// Удаляем пробелы и приводим строки к нижнему регистру
			str1 = str1.replace(/[^\w]/g, "").toLowerCase();
			str2 = str2.replace(/[^\w]/g, "").toLowerCase();

			// Сортируем символы в обеих строках
			var sortedStr1 = str1.split("").sort().join("");
			var sortedStr2 = str2.split("").sort().join("");
	
			// Сравниваем отсортированные строки
			document.getElementById('result').innerHTML = sortedStr1 === sortedStr2 
		}
		
		function task3(str) {
		// Приводим строку к нижнему регистру для учета всех возможных вариантов гласных
		str = str.toLowerCase();

		var vowels = ['a', 'e', 'i', 'o', 'u'];
		var count = 0;

		for (var i = 0; i < str.length; i++) {
			if (vowels.includes(str[i])) {
				count++;
			}
		}

		document.getElementById('result').innerHTML = count;
		}
		
		function task4(rows) {
			var result = "";

			for (var i = 1; i <= rows; i++) {
				result += i + " ";
				for (var j = 1; j <= i; j++) {
					result += "#";
				}
				result += `<br>`;
			}

			document.getElementById('result').innerHTML = result;
		}
		
		function task5() {
			for (var i = 1; i <= 100; i++) {
				if (i % 3 === 0 && i % 5 === 0) {
					console.log('FizzBuzz');
				} else if (i % 3 === 0) {
					console.log('Fizz');
				} else if (i % 5 === 0) {
					console.log('Buzz');
				} else {
					console.log(i);
				}
			}
		}
		
		function task6() {
			var size = 8;
			var chessboard = '<table>';

			for (var row = 0; row < size; row++) {
				chessboard += '<tr>';
				for (var col = 0; col < size; col++) {
					// Проверяем четность суммы индексов строки и столбца
					if ((row + col) % 2 === 0) {
						chessboard += '<td class="white"> </td>';
					} else {
						chessboard += '<td class="black">#</td>';
					}	
				}
				chessboard += '</tr>';
			}
			chessboard += '</table>';
			document.getElementById('result').innerHTML = chessboard;
		}
		
		function task7(a, b) {
			document.getElementById('result').innerHTML = (a<b ? a : b)
		}
		
		function task8(number) {
			// Приведение числа к неотрицательному значению
			var num = Math.abs(number);

			// Базовые случаи
			if (num === 0) {
				document.getElementById('result').innerHTML = true;  // Ноль чётный
			}
			if (num === 1) {
				document.getElementById('result').innerHTML = false;  // Единица нечётная
			}

			// Рекурсивный вызов с уменьшением числа на 2
			document.getElementById('result').innerHTML = task8(num - 2);
		}
		
		//task 9
		function countBs(str) {
			let count = 0;
			for (let i = 0; i < str.length; i++) {
				if (str.charAt(i) === 'B') {
					count++;
				}
			}
			document.getElementById('result').innerHTML = count;
		}

		function countChar(str, char) {
			let count = 0;
			for (let i = 0; i < str.length; i++) {
				if (str.charAt(i) === char) {
					count++;
				}
			}
			document.getElementById('result').innerHTML = count;
		}
		
		//task 10
		
		function range(start, end, step = 1) {
			let arr = [];
			if (step > 0) {
				for (let i = start; i <= end; i += step) {
					arr.push(i);
				}
			} else {
				for (let i = start; i >= end; i += step) {
					arr.push(i);
				}
			}
			return arr;
		}

		function sum(arr) {
			let total = 0;
			for (let num of arr) {
				total += num;
			}
			return total;
		}
		
		//task 11
		
		function reverseArray(...arr) {
			let reversedArr = [];
			for (let i = arr.length - 1; i >= 0; i--) {
				reversedArr.push(arr[i]);
			}
			return reversedArr;
		}

		function reverseArrayInPlace(...arr) {
			for (let i = 0; i < Math.floor(arr.length / 2); i++) {
				let temp = arr[i];
				arr[i] = arr[arr.length - 1 - i];
				arr[arr.length - 1 - i] = temp;
			}
			return arr;
		}
		
		//task12
		function deepEqual(value1, value2) {
			if (value1 === value2) {
				return true;
			}
			
			if (typeof value1 !== "object" || value1 === null || typeof value2 !== "object" || value2 === null) {
				return false;
			}

			let keys1 = Object.keys(value1);
			let keys2 = Object.keys(value2);

			if (keys1.length !== keys2.length) {
				return false;
			}

			for (let key of keys1) {
				if (!keys2.includes(key) || !deepEqual(value1[key], value2[key])) {
					return false;
				}
			}

			return true;
		}
		
		
		function task13() {
			const arrays = [[1, 2, 3], [4, 5], [6]];
			return arrays.reduce((result, currentArray) => result.concat(currentArray), []);
		}

		
		</script>		


	</body>
```

<h2>Вывод</h2>
Я научился работать, с функциями, алгоритмами, методами в JS
