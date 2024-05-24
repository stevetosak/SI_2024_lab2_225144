# Втора лабораториска вежба по Софтверско инженерство

## Stefan Toskovski 225144
Control Flow Graph
   -
<br>

___Во овој CFG, бројките на јазлите се соодветни на линијата код која што е обележана со коментар.___

<br>
<br>
  
![image](https://github.com/stevetosak/SI_2024_lab2_225144/assets/116950252/80c2edec-5e4f-4c8c-9e84-045a635b6846)


Цикломатска комплексност
   -
   Цикломатската комплексност на овој код е: 10.  
   Резултатот го добив така што изброив колку услови (гранења) има во кодот, користејќи ја формулата C = P + 1.
   
Every Branch Test Cases
   -
   [EveryBranch_TestCases - Sheet1-1.pdf](https://github.com/stevetosak/SI_2024_lab2_225144/files/15435369/EveryBranch_TestCases.-.Sheet1-1.pdf)

   ### _Вкупно се потребни 5 тест случаи._  
   **1. checkCart(null, 500)** - Прв тест случај е празна листа и фрла исклучок.  
   **2. checkCart(new List.of(new Item(Frutiko,0412315,350,0.05),new Item(null,5412315,1000,0)), 500)** - Oвој тест покрива повеќе случаеви:  
      - _кога името на производот е null_  
      - _кога името на производот е поставено_  
      - _првиот производ задоволува if условите - (13) и  (18) , а вториот не ги задоволува_  
   
   На крај, овој тест враќа false бидејќи sum=1302.5 а payment=500, т.е sum > payment.  
   
   **3. checkCart(new List.of(new Item(Frutiko,123512,350,0.05)), 500)** - Овој тест враќа true на крај  
   **4. checkCart(new List.of(new Item(Frutiko,null,350,0.05)), 500)** - Овој тест фрла исклучок бидејќи баркодот е null.(17)    
   **5. checkCart(new List.of(new Item(Frutiko,ASD1434125,350,0.05)), 500)** - Овој тест фрла исклучок бидејќи има невалидни карактери во баркодот. (11)  
 
Multiple Condition Test Cases
-

   ![image](https://github.com/stevetosak/SI_2024_lab2_225144/assets/116950252/044f61c2-1fcb-4154-92cf-596566c9fa17)
   
 _Бидејќи во if условот има 3 изрази врзани со логичко и, за да помине условот треба сите 3 изрази да се точни. Тоа значи дека ако за некој израз се добие false, резултатите на изразите после него не се битни, па затоа не мора да ги пишиме сите 8 комбинации, туку може со само 4 комбинации за а ги покриеме сите случаи._


   
