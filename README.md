# Solar + Wind Hybrid EV Wireless Charging System  

This project demonstrates a **wireless electric vehicle (EV) charging system** powered by a **hybrid solar and wind energy source**. The system integrates renewable energy harvesting, intelligent source switching, and wireless energy transfer to enable sustainable EV charging without physical connectors.  

---

## Project Overview  

The system uses **transmitter coils** placed on a charging platform and **receiver coils** embedded in a model EV (fiber body car). Power is harvested through **solar panels** and a **wind turbine**, which are regulated and stored in **solid-state batteries**.  

A **microcontroller (Arduino/8051)** plays a critical role in **automatically switching between solar power and wind power** depending on the environment:  
- **Daytime / Sunny** → Solar power is the primary charging source.  
- **Night / Cloudy** → Wind turbine power is prioritized.  

This ensures that the EV can be charged round-the-clock using clean energy sources.  

---

## Key Features  

- **Hybrid Power Source with Smart Switching**  
  - Arduino-controlled source selection (solar → wind, based on conditions)  
  - MPPT control for solar efficiency  
  - Hybrid inverter for stable conversion  
  - Solid-state batteries for storage  

- **Wireless EV Charging**  
  - Coil-based transmission and reception of energy  
  - Electromagnetic induction-based operation  

- **Two Main PCBs**  
  - **PCB1 (Transmitter platform)**: Power regulation, transmission coils, battery interface  
  - **PCB2 (Receiver in EV)**: Captures power, controlled by microcontroller, displays system status  

- **Embedded Control System**  
  - Arduino monitors input from solar and wind  
  - Automatically switches power source when solar is insufficient  
  - LCD interface for real-time updates (charging status, source in use)  

---

## Intelligent Power Switching  

The **Arduino/microcontroller logic** ensures uninterrupted charging:  
1. **Reads solar voltage/current levels** via sensors (LDRs, voltage dividers, current sensors).  
2. If the solar panel is underperforming (low sunlight or night), it switches the input to the **wind turbine**.  
3. The selected source charges the battery, which then powers the transmitter coils.  
4. The EV (receiver side) continues charging without interruption.  

This hybrid control makes the system resilient and reliable against weather conditions.  

---

## Components Used  

### Hardware  
- Solar panel  
- Wind turbine  
- Hybrid inverter  
- Solid-state batteries  
- Step-down transformer  
- Transmitter & receiver wireless coils  
- Arduino / 8051-family microcontroller  
- 16x2 LCD Display  

### Electronic Components (PCBs)  
- Voltage regulators: LM7805, LM7812, LM317  
- Diodes (rectifiers, polarity protection)  
- Capacitors (filtering and stabilization)  
- Potentiometers (voltage/current tuning)  
- Fuses for protection  
- Crystal oscillator for MCU clock  
- Push buttons and indicators (LEDs)  

---

## Working Flow  

1. **Solar/Wind Energy Harvesting**  
   - Solar → via MPPT controller  
   - Wind → direct turbine regulation  
   - Both feed into hybrid inverter + batteries  

2. **Microcontroller Control (Smart Switching)**  
   - Arduino measures solar input  
   - If solar < threshold → switch to wind  
   - Automatically chooses best source without user intervention  

3. **Wireless Transmission**  
   - Power delivered to **transmitter coil** from chosen source  
   - Receiver coil under the EV captures energy  
   - PCB2 regulates and displays system parameters on LCD  

---

## Advantages  

- Contactless EV charging for convenience and safety  
- Utilizes solar + wind energy for continuous operation  
- Solid-state batteries ensure stability and long-term storage  
- Overcomes solar panel limitations (night/cloudy conditions)  
- Modular PCB design for easy extension and upgrades  

---

## Future Enhancements  

- Adaptive switching based on not just light but *load demand*  
- AI-based prediction (weather forecast + expected usage)  
- IoT integration for remote monitoring via mobile app  
- High-frequency coil design to improve transmission efficiency  

---

## Repository Structure  

