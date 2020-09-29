A simplified version of the saadc example in the nrf5 SDK.
In this example the Saadc is set to sample 10 times at 100 ms each, with 14bit as a resolution.

### The Analog voltage can be read using this equation :

RESULT = [V(P) – V(N) ] x GAIN / REFERENCE x 2^(RESOLUTION - m)
>(m=0) if CONFIG.MODE=SE, or (m=1) if CONFIG.MODE=Diff.

[**Source**](https://infocenter.nordicsemi.com/index.jsp?topic=%2Fps_nrf52840%2Fsaadc.html&cp=4_0_0_5_22_2&anchor=saadc_digital_output)

### nRF5_SDK version supported :
Versions starting from **v15.3**.

### Supported Development kits : 
* The nRF52-DK (PCA10040).
* The nRF52840-DK (PCA10056).
* The nRF52833-DK (PCA10100).

### Toolchain :
**SEGGER**. 

### How to test :
1. Clone or download the repository into the ``$nRF5_SDK_Location\examples\peripheral\`` folder.

2. You can use a potentiometer to test it. 
The example is set to use the analog pin AIN1 **(P0.03)**.

The middle pin of the potentiometer should be connected to the analog pin, and the other pins to **vdd** and **gnd**.
> **Note:** Do not connect the potentiomter to the **5V** pin instead of the **VDD** pin. the maximum supported voltage on the analog pins is **VDD**.
> Connecting it directly to 5V may damage the SOC.

1. Open your prefered Terminal emulator.

### Analog inputs  :
| Analog Input | GPIO |
|-------|--------------|
|AIN0 | P0.02|
|AIN1 | P0.03|
|AIN2 | P0.04|
|AIN3 | P0.05|
|AIN4 | P0.28|
|AIN5 | P0.29|
|AIN6 | P0.30|
|AIN7 | P0.31|
