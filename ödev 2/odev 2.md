Teknik özet ve hesaplamalar.

Hedef PWM frekansı 1 kHz, TIM1 timer clock’u 16 MHz seçildi. Sayaç clock’unu 1 MHz yapmak için prescaler değeri:

`f_CNT = f_TIM / (PSC + 1) = 16 MHz / (15 + 1) = 1 MHz`

Bir PWM periyodunda 1000 sayaç adımı bulunması için:

`ARR = f_CNT / f_PWM - 1 = 1 MHz / 1 kHz - 1 = 999`

Böylece PWM periyodu 1 ms, frekansı 1 kHz olur.

Faz gecikmeleri 250 sayaç adımı aralıklarla ayarlandı. 1 MHz sayaç clock’unda her adım 1 µs olduğundan 250 adım = 250 µs = periyodun %25’i = 90° fazdır.