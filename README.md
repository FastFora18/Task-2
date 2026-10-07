## Практическая работа №2: Операторы языка C#

### | Программа 1. Операции деления и остатка
```csharp
int x = 17 / 5;
int y = 17 % 5;
Console.WriteLine("x = " + x);
Console.WriteLine("y = " + y);
```
#### Результат выполнения:
<img width="1901" height="996" alt="image" src="https://github.com/user-attachments/assets/b7b45223-cf02-41af-a5fb-cc1fc2d4c619" />



### | Программа 2. Префиксный инкремент
```csharp
int a1 = 5;
int res1 = ++a1 * 2;
Console.WriteLine(\$" {res1} ({a1})");
```
#### Результат выполнения:
<img src="SCRN/(2).png" alt="Результат 2" width="600"/>


### | Программа 3. Постфиксный инкремент
```csharp
int a2 = 5;
int res2 = a2++ * 2;
Console.WriteLine(\$" {res2} ({a2})");
```
#### Результат выполнения:
<img src="SCRN/(3).png" alt="Результат 3" width="600"/>
