# Multimeter

A multimeter is an instrument for measuring **voltage, current or resistance for low voltage projects** (up to 12V).

At our hackSpace, we use the [RS Multimeter model](https://uk.rs-online.com/web/p/multimeters/1231938)

More about multimeter: [How to use a multimeter to measure voltage and current in a circuit?](https://arduinofactory.com/the-multimeter/)

----
### Warning!

⚠️  DO NOT USE IT ON MAINS ELECTRICITY (wall sockets)

It is safe to test Arduino circuits, LEDs, sensors, and batteries, but using it on household mains can be extremely dangerous.

----
### Why and how to use a multimeter

You’ll mostly use it to troubleshoot problems in your circuit—for example, a sensor that isn’t responding, or an LED that won’t light.

The typical workflow is:

1. **Measure voltage first** to check if the component is receiving power.

2. If you are getting incorrect voltage, use **continuity testing** to find the specific connection or component causing the problem.

3. If all hardware appears fine, the issue may lie in the **code**.

----
# TUTORIAL: Testing Voltage

Measuring voltage helps you check whether a component or section of your circuit is receiving power as expected. This is especially useful when an LED, sensor, or motor isn’t working. 

POTATO/PLANT Voltage: You can also use it in experimental projects to measure how much electrical potential these sources produce and whether it’s enough to power your components.

**Step-by-Step Guide:**

- Turn off the power. Always disconnect the Arduino, battery, or power supply before testing.

- Set the multimeter: Turn the dial to **DC Voltage (V—)**.

- Measure the voltage
  - Start from the power source and move along the circuit to isolate the problem.
  - The red probe goes to the positive side, black to ground.  
  - Read the value on the display.  
  - Compare it with the expected voltage (e.g., 5 V from Arduino, 3 V from a battery).  

- Interpret the result:
  - **Correct voltage** → component is receiving power; check other parts if it still doesn’t work.  
  - **No or low voltage** → power isn’t reaching the component; check wiring, connections, or the power source.
 
If the voltage is correct, you know the power supply and the immediate connections are fine — the problem is elsewhere (wiring to signal pins, code, or the component itself).

If the voltage is missing or low, you know the problem is in the power path, and you can then check each connection (continuity) to find the broken link.


  - 
----
# TUTORIAL: Checking Continuity

When a component isn’t working as expected you, can use a Multimeter in CONTINUITY MODE to check electrical continuity at each link in your circuit. This helps you locate any broken links that might be causing the problem.

Think of your circuit as a chain: electricity travels from connection to connection, and every link must be intact for the circuit to work. For example, point (A) should be connected to point (B) —but is it? Let’s check using the multimeter.

**Step-by-Step Guide:**

- Turn off the power. Always disconnect the Arduino, battery, or power supply before testing.

- Set the multimeter: Turn the dial to continuity mode (sound/beep icon).

- Identify the points to test

    - Pick two points that should be connected, e.g., Arduino 5V pin → LED anode.
      
    - Place the probes
      
    - Does it beep?
      
        - Beep → Connection is complete; electricity can flow. Link is working properly. 
          
        - No beep → Broken link. Check wires, component, breadboard, or solder join.
          
  - Move along the chain and test each segment of the circuit. If continuity is correct along the whole path, the problem lies elsewhere.





