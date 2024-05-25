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
   Исто така, биејќи овој граф е планарен, може да се изброи колку региони има графот, и ке се добие истиот резултат, 10.
   
Every Branch Test Cases
-
   ### _Вкупно се потребни 5 тест случаи._  
   1. checkCart(**null, 500**) - Прв тест случај е празна листа и фрла исклучок.  
   2. checkCart(List.of(new Item(**"Frutiko",null,350,0.05F)), 500**)) - Овој тест фрла исклучок бидејќи баркодот е null.(17)    
   3. checkCart(List.of(new Item(**"Frutiko,"ASD1434125",350,0.05F), 500**)) - Овој тест фрла исклучок бидејќи има невалидни карактери во баркодот. (11) 
   4. checkCart(List.of(new Item(**"Frutiko","0412315",350,0.05F**),new Item(**null,5412315,1000,0), 500**)) - Oвој тест покрива повеќе случаеви:  
      - _кога името на производот е null_  
      - _кога името на производот е поставено_  
      - _првиот производ задоволува if условите - (13) и  (18) , а вториот не ги задоволува_  
   
   На крај, овој тест враќа false бидејќи sum=1302.5 а payment=500, т.е sum > payment.  
   5. checkCart(List.of(new Item(**"Frutiko","123512",350,0.05F), 500)**) - Овој тест враќа true на крај  

   За подетални информации околу тест случаите, во прилог е табела во која детално е прикажано за соодветен тест случај кој јазли ги посетува.
    [EveryBranch_TestCases - Sheet1-2.pdf](https://github.com/stevetosak/SI_2024_lab2_225144/files/15438232/EveryBranch_TestCases.-.Sheet1-2.pdf)
  
 
Multiple Condition Test Cases
-

   ![image](https://github.com/stevetosak/SI_2024_lab2_225144/assets/116950252/044f61c2-1fcb-4154-92cf-596566c9fa17)
   
 _Бидејќи во if условот има 3 изрази врзани со логичко и, за да помине условот треба сите 3 изрази да се точни. Тоа значи дека ако за некој израз се добие false, резултатите на изразите после него не се битни, па затоа не мора да ги пишиме сите 8 комбинации, туку може со само 4 комбинации за да ги покриеме сите случаи._

 Unit Tests
 -

 Првиот unit test се состои од 5 тестови кои тестираат според every branch критериумот. Се користи assertThrows за првите 3 тест случаи во кој се очекува да завршат со Runtime исклучок.За тестовите 4 и 5 се користат assertTrue и assertFalse во кој се очекува програмата да врати true односно false.
 Вториот unit test се состои од 4 тестови за секоја комбинација во if условот (18) според Multiple Case критериумот.

 Тестовите се извршуваат со користење на gradlew или gradle.bat зависно од оперативниот систем.(Ке илустирам со gradlew бидејќи користам linux).

 Со ./gradlew test се извршуваат сите тестови така што gradle ги бара сите функции означени со анотацијата @Test и ги извршува еден по еден. Ако сите пројдат се јавува BUILD SUCCESSFUL.
 Алтернативно може само да се изврши класата SILab2Test во Intelij и да се прикаже резултатот таму.


   
