# Домашнее задание к работе 13
## Условие задачи

определяет число слов в нем, написанных с большой
буквы.

   
### Блок-схема

![Uploading {D5040E60-F2DB-476C-A74F-1EE5C0B6AA97}.png…]()




## 2. Реализация программы

```
#define _CRT_SECURE_NO_WARNINGS
#define _USE_MATH_DEFINES
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h> 
#include <conio.h>
#include <math.h>
int main() {
    setlocale(LC_ALL, "RUS");
    printf("Напишите предложение:\n");
    char str[200];
    fgets(str, sizeof(str), stdin);
    int k = 0;
    int inWord = 0;  
    for (int i = 0; str[i] != '\0'; i++) {
        if (!isspace((unsigned char)str[i])) {
            if (!inWord) {                    
                inWord = 1;
                if (isupper((unsigned char)str[i])) {
                    k++;  
                }
            }
        }
        else {
            inWord = 0; 
        }
    }
    printf("Кол-во заглавных букв: %d", k);
   
}
```


## 3. Результаты работы программы

```
Напишите предложение:
HeLLo PolinAAA RudneVa
Кол-во заглавных букв: 3
```


<img width="1181" height="232" alt="{418E8159-0290-48BB-9D41-359ACFC93ACF}" src="https://github.com/user-attachments/assets/a9766482-ecf1-4db7-bd0a-746f599b0be1" />
