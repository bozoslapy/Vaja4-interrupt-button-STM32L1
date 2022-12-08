# Vaja4-interrupt-button-STM32L1

ODGOVORI NA VPRAŠANJA -->

2.b) V Pinout % Configuraton pogledu glede na vašo razvojno ploščico ugotovite, ali lahko uporabite modro tipko za digitalni vhod kot interrupt (GPIO_EXT…). Če da, kateri pin je to?
--> PA0

2.c) Zapišite naslov izhodnih pinov za zeleno in modro LED --> 
--> ZELENA:PC9
--> MODRA:PC8

3.c) Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a)  --> c)HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_9);

3.d) Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala
Koliko znaša (v mili sekundah) zapisana zakasnitev, ki jo proizvede zanka for --> 9999 milisekund

3.e) V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a) --> HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);

3.f) V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a) --> HAL_Delay(500);

Komentar na delovanje --> Koda nama ni delala hujših preglavic vendar je moj partner pri ukazu void HAL_GPIO_EXTI_Callback(uint16_t GPIO_Pin) zamenjal črki in zato nama koda ni delovala. Tako nisva dobila odziva zelene ledice. Zamenjal je besedo EXTI v EXIT. 

Slika mikroprocesorja --> 

![Mikroprocesor](https://raw.githubusercontent.com/bozoslapy/Vaja4-interrupt-button-STM32L1/90ef2f4b70a8dd5ac03f4841e41f66e7447152b4/pinout%204.PNG)


Slika vezja -->

![Slika vezja](https://raw.githubusercontent.com/bozoslapy/Vaja4-interrupt-button-STM32L1/d9fa6cbd6677b1e56a2c8a92892f928637ae3a6d/IMG_0408.jpg)

![Posnetek delovanja](https://github.com/bozoslapy/Vaja4-interrupt-button-STM32L1/commit/feaf5b0ba0e6f112f633b9f08363b3ac9e7cf298)
