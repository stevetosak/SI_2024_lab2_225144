# Втора лабораториска вежба по Софтверско инженерство

## Stefan Toskovski 225144
Control Flow Graph
   -
Во овој CFG, бројките на јазлите се соодветни на линијата код која што е обележана со коментар. 
![image](https://github.com/stevetosak/SI_2024_lab2_225144/assets/116950252/66cc2601-a0b2-4c47-9531-fd7a225b62ae)

Цикломатска комплексност
   -
   Цикломатската комплексност на овој код е: 10.
   Резултатот го добив така што изброив колку услови (гранења) има во кодот, користејќи ја формулата C = P + 1.
   
Every Branch Test Cases
   -
   [EveryBranch_TestCases - Sheet1-1.pdf](https://github.com/stevetosak/SI_2024_lab2_225144/files/15435369/EveryBranch_TestCases.-.Sheet1-1.pdf)

   Вкупно се потребни 5 тест случаи.
   1. checkCart(null, 500) - Прв тест случај е празна листа и фрла исклучок.
   2. checkCart(new List.of(new Item(Frutiko,0412315,350,0.05),new Item(null,5412315,1000,0)), 500) - Oвој тест покрива повеќе случаеви:
      - кога името на производот е null
      - кога името на производот е поставено
      - првиот производ задоволува if условите - (13) и  (18) , а вториот не ги задоволува
   
   На крај, овој тест враќа false бидејќи sum=1302.5 а payment=500, т.е sum > payment.
   
   3. checkCart(new List.of(new Item(Frutiko,123512,350,0.05)), 500) - Овој тест враќа true на крај
   4. checkCart(new List.of(new Item(Frutiko,null,350,0.05)), 500) - Овој тест фрла исклучок бидејќи баркодот е null.(17)
   5. checkCart(new List.of(new Item(Frutiko,ASD1434125,350,0.05)), 500) - Овој тест фрла исклучок бидејќи има невалидни карактери во баркодот. (11)

Multiple Condition
-

   ![image](https://github.com/stevetosak/SI_2024_lab2_225144/assets/116950252/044f61c2-1fcb-4154-92cf-596566c9fa17)



   
