# Multimeter

A multimeter is an instrument for measuring **voltage, current or resistance for low voltage projects** (up to 12V).

At our hackSpace, we use the [RS Multimeter model](https://uk.rs-online.com/web/p/multimeters/1231938)

More about multimeter: [How to use a multimeter to measure voltage and current in a circuit?](https://arduinofactory.com/the-multimeter/)

----
### Warning!

⚠️  DO NOT USE IT ON MAINS ELECTRICITY (wall sockets)

It is safe to test Arduino circuits, LEDs, sensors, and batteries, but using it on household mains can be extremely dangerous.

----
## TUTORIAL: Workflow

You’ll mostly use it to troubleshoot problems in your circuit—for example, a sensor that isn’t responding, or an LED that won’t light.

**The typical workflow is:**

1. Use *continuity-testing* to find the specific connection or component causing the problem.
  
2. Measure *voltage* to check if the component is receiving power.

3. If all hardware appears fine, the issue may lie in the *code*.

----
## TUTORIAL: Testing Continuity

When a component isn’t working as expected you, can use a Multimeter in CONTINUITY MODE to check electrical continuity at each link in your circuit. This helps you locate any broken links that might be causing the problem.

Think of your circuit as a chain: electricity travels from connection to connection, and every link must be intact for the circuit to work. For example, point (A) should be connected to point (B) —but is it? Let’s check using the multimeter.

**Step-by-Step Guide:**

- Turn off the power. Always disconnect the Arduino, battery, or power supply before performing continuity-testing.

- Set the multimeter: Turn the dial to *continuity mode* (sound/beep icon).

- Identify the points to test

    - Pick two points that should be connected, e.g., Arduino 5V pin → LED anode.
      
    - Place the probes
      
    - Does it beep?
      
        - Beep → Connection is complete; electricity can flow. Link is working properly. 
          
        - No beep → Broken link. Check wires, component, breadboard, or solder join.
          
  - Move along the chain and test each segment of the circuit. If continuity is correct along the whole path, the problem lies elsewhere.

----
## TUTORIAL: Testing Voltage

Measuring voltage helps you check whether a component or section of your circuit is receiving power as expected. 

For example: You have performed continuity testing and confirmed that all connections are working properly, however, your sensor/LED/motor still doesn't work. In this case, measuring voltage can show whether the component is receiving the correct power — too much, too little, or none at all.


*Measuring bio-electricity*: In projects that involve bio-electrical sources—such as plants, tomatoes, potatoes, or mushrooms—using a multimeter to measure voltage will help you understand their electrical potential and determine whether it is sufficient to power your components.

**Step-by-Step Guide:**

- Power your circuit (up to 12V only). Connect the Arduino to USB or a battery pack. Make sure the circuit is powered.

- Set the multimeter: Turn the dial to **DC Voltage (V—)**.

- Measuring voltage:
  - Start from the power source and move along the circuit to isolate the problem.
    
  - The red probe goes to the positive side, black to ground.  
  
  - Read the value on the display.  

  - Compare it with the expected voltage (e.g., 5 V from Arduino, 3 V from a battery).  

- Results:
  - **Correct voltage** → Component is receiving power; check other parts if it still doesn’t work. If the voltage is correct in all parts, you know the problem is elsewhere. Now you can:
        - Replace component. It might be that the component itself is faulty.
        - Check your code. It might be that the problem is in the code. Start ensuring that pin designations match the wiring you’ve built.
    
  - **No or low voltage** → Power isn’t reaching the component. If the voltage is missing or low, the problem is in the power path. Check wiring, connections, or the power source.
 

**Sensor example**
Testing that a sensor in your circuit is receiving the correct power:

**- Black probe → GND pin of the sensor**

**- Red probe → VCC pin of the sensor**

- Results:
    - The display should show close to 5V (if powered from Arduino 5V) or 3.3V (if using 3.3V power). Instead, it shows 0V, then your sensor is not getting the power. Check proper wiring.

   - If the sensor *is* receiving the correct voltage but still doesn’t work, the sensor may be faulty. You should try replacing the sensor and/or checking your code.
 












