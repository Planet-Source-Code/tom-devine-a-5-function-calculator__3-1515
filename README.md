<div align="center">

## A 5 Function Calculator


</div>

### Description

Just a simple calculator that will add, subtract, multiply, divide, and it will also do powers like 5^3 = 125.
 
### More Info
 
Tested with Borland C++ 5.5, Borland Turbo C++ 1.01, DJGPP 2.03. Does not work with Digital Mars 8.12

Changes your prompt green.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tom Devine](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tom-devine.md)
**Level**          |Beginner
**User Rating**    |3.8 (23 globes from 6 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tom-devine-a-5-function-calculator__3-1515/archive/master.zip)

### API Declarations

```
#include <iostream.h>
#include <conio.h>
```


### Source Code

```
#include <iostream.h>
#include <conio.h>
float inputOne, inputTwo, answer;
char operator_, yn;
int main()
{
	textcolor(LIGHTGREEN);
	while (yn != 'n')
	{
		clrscr();
		cout << "First number + - / * ^ second number\n";
		cin >> inputOne >> operator_ >> inputTwo;
		if (operator_ == '+')
			answer = inputOne + inputTwo;
		if (operator_ == '-')
			answer = inputOne - inputTwo;
		if (operator_ == '*')
			answer = inputOne * inputTwo;
		if (operator_ == '/')
			{
			if (inputTwo == 0)
				{
				cout << "Cannot divide by 0";
				}
			else
				answer = inputOne / inputTwo;
			}
		if (operator_ == '^')
			{
			answer = inputOne;
			for (int i=2; i<=inputTwo; i++)
				answer = answer * inputOne;
			}
		cout << endl;
		cout << inputOne << " " << operator_ << " ";
		cout << inputTwo << " = " << answer;
		cout << "\n\nSolve another? <yn> ";
		cin >> yn;
		cout << "\n";
	}
	return 0;
}
```

