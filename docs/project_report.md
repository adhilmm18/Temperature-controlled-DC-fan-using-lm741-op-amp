# CONTENTS 

|ACKNOWLEDGEMENT|ii|
|---|---|
|ABSTRACT|iii|
|LIST OF FIGURES|v|
|1 INTRODUCTION<br>vi||
|2 LITERATURE REVIEW<br>viii||
|3 METHODOLOGY ix||
|3.1 SDG’s Addressed . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .<br>ix||
|3.2 BLOCK DIAGRAM<br>. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . x||
|3.3 COMPONENTS . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .<br>x||
|3.4 WORKING PRINCIPLE . . . . . . . . . . . . . . . . . . . . . . . . . . . . .<br>xi||
|4 IMPLEMENTAION xii||
|4.1 Circuit Diagram . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .<br>xii||
|4.2 Implmentation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .<br>xii||
|5 RESULTS<br>xiv||
|6 CONCLUSION<br>xv||
|REFERENCES|xvi|
|LISTOFFIGURES||
|3.1<br>Block Diagram of Temperature Controlled DC Fan Using NTC Thermistor|. .<br>x|
|4.1<br>Circuit Diagram of Temperature Controlled DC Fan Using Thermistor . . . . .|<br>xii|
|5.1<br>Temperature greater than 50 - 60 degree . . . . . . . . . . . . . . . . . .|. . . xiv|



i 

# CHAPTER1 

# INTRODUCTION 

In the modern era of rapid technological advancement, electronic devices and mechanical systems are becoming increasingly compact and powerful. A direct consequence of this increased power density is the generation of substantial amounts of heat during normal operation. Effective thermal management has therefore become a critical aspect of system design, as excessive heat can lead to diminished component performance, accelerated degradation, thermal runaway, and ultimately, catastrophic system failure. 

Traditionally, cooling systems such as DC exhaust fans are employed to continuously force airflow over heat-generating components. While effective at removing heat, running a fan continuously at full speed presents several significant drawbacks. Continuous operation leads to unnecessary power consumption, which is particularly detrimental in battery-operated or energy-conscious applications. Furthermore, it results in constant acoustic noise and accelerates the mechanical wear and tear on the fan’s bearings, significantly reducing its operational lifespan. 

To address these inefficiencies, automated temperature-controlled cooling systems have been developed. These intelligent systems monitor the ambient or component temperature in real-time and activate the cooling mechanism only when the temperature exceeds a predefined safe threshold. Once the system cools down, the fan is automatically powered off or its speed is reduced. This on-demand approach optimizes energy usage, minimizes noise pollution, and extends the longevity of the cooling hardware. 

This report focuses on the design and implementation of a simple, highly effective temperature-controlled DC fan utilizing a Negative Temperature Coefficient (NTC) thermistor. An NTC thermistor is a highly sensitive, low-cost thermal sensor whose electrical resistance decreases predictably as its operating temperature increases. By integrating this sensor into a voltage divider and control circuit, the system can autonomously detect temperature fluctuations and actuate the fan accordingly. 

The primary objective of this project is to construct a reliable, automated cooling circuit that demonstrates the practical application of thermistors in thermal management. The subsequent sections of this report will delve into the underlying principles of the NTC thermistor, the detailed circuit design, the selection of components, and an analysis of the system’s operational performance. 

iii 

# CHAPTER2 

# LITERATUREREVIEW 

Kavinbala, et al., ”Temperature based Fan Speed Controller,” International Research Journal on Advanced Science Hub (IRJASH), vol. 2, no. 7, pp. 160-164, July 2020 

- Kavinbala et al. proposed an automated ”Temperature based Fan Speed Controller” designed to optimize energy consumption and enhance user comfort by removing the need for manual intervention. The authors developed an embedded system that dynamically adjusts the speed of a cooling fan in direct response to real-time ambient temperature changes. Utilizing a temperature sensor interfaced with a central microcontroller, the system continuously monitors the environment and regulates the fan’s motor—typically through Pulse Width Modulation (PWM). This research demonstrates that automatically scaling fan speed according to thermal demand not only maintains optimal environmental conditions but also significantly reduces power wastage compared to traditional, manually operated binary (on/off) cooling systems. 

Reddy, N., ”Automatic Temperature Based Fan Controller,” Journal of Engineering Sciences, vol. 14, no. 5, 2023 

- Reddy evaluated an ”Automatic Temperature Based Fan Controller” designed to optimize energy consumption and enhance user comfort in modern engineering applications. The study details an embedded system that dynamically adjusts the speed of a cooling fan in direct response to real-time ambient temperature changes. By utilizing a temperature sensor interfaced with a central microcontroller, the system continuously monitors the environment and regulates the fan’s motor, typically through Pulse Width Modulation (PWM). Reddy’s findings emphasize recent advancements in component efficiency and validate the long-term reliability and necessity of such automated hardware in contemporary energy conservation 

iv 

strategies, proving that scaling fan speed to thermal demand significantly reduces power wastage compared to manually operated systems. 

# CHAPTER3 

# METHODOLOGY 

- Sensing Stage: The core component is the NTC Thermistor (10k). An NTC thermistor’s resistance decreases as the temperature increases. It is placed in a voltage divider configuration with a fixed resistor (R1). 

- Comparison Stage: The varying voltage from the sensor stage is fed into the Inverting Input (Pin 2) of the LM741 Operational Amplifier. A Potentiometer (RV1) sets a fixed reference voltage at the NonInverting Input (Pin 3). 

- Switching/Driver Stage: The High output from the Op-Amp is fed through a base resistor (R2) to the base of an NPN Transistor (BC547). The transistor acts as a switch, completing the circuit foe the DC Fan. 

- Protection Stage: A Diode (1N4007) is connected in parallel with the fan to acting as a flywheel diode, protecting the transistor from back EMF voltage spikes generated by the fan motor when it turns off. 

## 3.1 SDG’s Addressed 

- SDG 7 – Affordable and Clean Energy. 

   - This project supports SDG 7 by reducing unnecessary electrical power consumption through automatic fan control based on temperature sensing, thereby improving energy 

efficiency 

- SDG 9 – Industry, Innovation and Infrastructure. 

v 

This project aligns with SDG 9 by demonstrating a low-cost,innovative temperature control system using a thermistor and 741 operational amplifier, which forms the basis of industrial automation and smart infrastructure. 

- SDG 11 – Sustainable Cities and Communities. 

This project contributes to SDG 11 by enhancing indoor comfort and safety through automatic temperature regulation, reducing manual intervention in residential and workplace environments. 

- SDG 12 – Responsible Consumption and Production 

   - This project addresses SDG 12 by ensuring responsible consumption of electrical energy, as the DC fan operates only when required, minimizing energy wastage. 

- SDG 13 – Climate Action 

This project supports SDG 13 by indirectly reducing carbon emissions through optimized energy usage and promoting environmentally conscious electronic system design. 

## 3.2 BLOCK DIAGRAM 



<!-- Start of picture text -->
Automatic Fan Speed Controller — Block Diagram<br>|<br>|<br>|<br>|_——<br>SSSaar!eeeee)<br><!-- End of picture text -->

Figure 3.1: Block Diagram of Temperature Controlled DC Fan Using NTC Thermistor 

vi 

## 3.3 COMPONENTS 

- Thermistor NTC 10 

- Operational Amplifier IC LM741 

- DC Fan 9V 

- Transistor BC140 PNP 

- Resistors 4.7K, 39 each one 

- Variable Resistor 10K 

- Diode 1N4007 

- Battery 9V 

## 3.4 WORKING PRINCIPLE 

- Sensing (Voltage Divider): An NTC thermistor acts as the core sensor in a voltage divider network. As ambient temperature rises, the thermistor’s resistance decreases exponentially, which dynamically alters the output voltage. 

- Comparison (Control Logic): An operational amplifier (e.g., LM358) serves as a comparator. It continuously compares the variable sensor voltage against a fixed reference voltage (the temperature threshold), which is manually set using a potentiometer. 

- Actuation (Driving the Fan): Once the sensor voltage crosses the reference threshold indicating high heat, the comparator outputs a logic HIGH. This signal drives a switching transistor into saturation, completing the circuit and turning on the DC fan. 

- Reset: As the fan cools the environment, the thermistor’s resistance increases. When the temperature falls below the threshold, the comparator outputs a logic LOW, switching off the transistor and stopping the fan. 

vii 

# CHAPTER4 

# IMPLEMENTAION 

## 4.1 Circuit Diagram 



<!-- Start of picture text -->
Neca uit<br>Uhnte titan<br>Pe<br>> RI4700HM J 5p140<br>Tav R3<br>104:<br>[ lez, 7<br>2 7KOHM k he -<br>XD Fan aut<br><!-- End of picture text -->

Figure 4.1: Circuit Diagram of Temperature Controlled DC Fan Using Thermistor 

- 4.2 Implmentation 

   - The circuit was initially designed, tested, and verified on a breadboard before finalimplementation. 

   - The circuit is then implemented on a general-purpose PCB using an NTC thermistor,resistor network, LM741 operational amplifier, transistor, and a DC fan. 

   - The thermistor and resistor form a voltage divider to convert temperature changes intocorresponding voltage variations. 

   - The LM741 op-amp is configured as a comparator to compare the sensed voltage with apreset reference voltage set using a potentiometer. 

viii 

- When the temperature exceeds the threshold, the comparator output turns ON thetransistor, which drives the DC fan. 

- A flyback diode is connected across the fan to protect the circuit from back EMF. 

- The circuit is powered using a 12V supply for practical operation. 

ix 

# CHAPTER5 

# RESULTS 

- The temperature-controlled DC fan circuit was successfully implemented and tested ona general-purpose PCB. 

- The LED remains continuously ON, indicating that the power supply to the circuit is active. 

- The threshold temperature is set using a potentiometer, allowing adjustment of theswitching point. 

- The DC fan starts rotating when the temperature exceeds the preset threshold ofapproximately 40°C to 60°C. 

- Below the threshold temperature, the fan remains OFF, and above it, the fan operates automatically. 

- The system demonstrates reliable and effective temperature-based automatic control ofthe DC fan. 



Figure 5.1: Temperature greater than 50 - 60 degree 

x 

# CHAPTER6 

# CONCLUSION 

In conclusion, the design and implementation of a temperature-controlled DC fan using an NTC thermistor provides a highly effective and practical solution for thermal management in electronic systems. By leveraging the inverse resistance-temperature relationship of the NTC thermistor, the circuit successfully automates the cooling process, ensuring that the fan is activated only when predefined thermal thresholds are exceeded. This on-demand cooling approach offers significant advantages over traditional continuous-operation cooling methods. Notably, it drastically reduces unnecessary power consumption, minimizes acoustic noise, and extends the mechanical lifespan of the cooling fan. While the system does present certain inherent challenges—such as the non-linear response of the thermistor, the potential for component self-heating, and the necessity for manual calibration—these factors can be effectively managed through careful circuit design and component selection. Ultimately, this project demonstrates that an analog, thermistor-based control circuit remains a robust, costeffective, and reliable method for protecting heat-sensitive components. Its simplicity, combined with its high sensitivity near threshold temperatures, makes it an ideal and accessible thermal management strategy for a wide array of applications, ranging from basic power supplies to consumer electronics and industrial control panels. 

# REFERENCES 

- [1] Kavinbala, et al., ”Temperature based Fan Speed Controller,” International Research Journal on Advanced Science Hub (IRJASH), vol. 2, no. 7, pp. 160-164, July 2020 

- [2] Reddy, N., ”Automatic Temperature Based Fan Controller,” Journal of Engineering Sciences, vol. 14, no. 5, 2023. 

xi 

- [3] Kumar, R., ”Design and Fabrication of Temperature based DC Fan Speed Control System using Microcontroller and Pulse Width Modulation Technique,” International Journal of Innovative Research in Science, Engineering and Technology (IJIRSET), vol. 4, no. 7, July 2015 

xii 

