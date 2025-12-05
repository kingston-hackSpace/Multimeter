# Multimeter

A multimeter is an instrument for measuring **voltage, current or resistance for low voltage projects** (up to 12V).

At our hackSpace, we use the [RS Multimeter model](https://uk.rs-online.com/web/p/multimeters/1231938)

More about multimeter: [How to use a multimeter to measure voltage and current in a circuit?](https://arduinofactory.com/the-multimeter/)

----
# Warning!

⚠️  DO NOT USE IT ON MAINS ELECTRICITY (wall sockets)

It is safe to test Arduino circuits, LEDs, sensors, and batteries, but using it on household mains can be extremely dangerous.

----
# When to use it

We will mostly use it to troubleshoot problems with our circuit, such as:

- Check if a component is receiving power

- Test if wires or connections are continuous

- Detect short circuits before they cause damage

- Measure voltage or current from batteries, unusual power sources, or sensors

At our hackSpace, we use the [RS Multimeter model](https://uk.rs-online.com/web/p/multimeters/1231938)

More about multimeter: [How to use a multimeter to measure voltage and current in a circuit?](https://arduinofactory.com/the-multimeter/)

----
# Why to use it

Mostly to troubleshoot problems with our circuit

----
### TUTORIAL
----
# When to Check for Continuity

Whenever something in your circuit isn’t working as expected or electricity is flowing where it shouldn’t. For example: 

- A component (LED, sensor, motor) doesn’t turn on

- A wire might be loose, broken, or incorrectly connected

- A solder joint may be cracked

- A breadboard or connector strip may not be making contact

- An accidental short circuit, causing power to flow where it shouldn’t


# Checking Continuity: “Testing the Chain”

When a component isn’t working as expected you can use continuity-testing to check each link in the circuit. Think of your circuit as a chain: electricity travels from connection to connection, and every link must be intact for the circuit to work. For example, point A should be connected to point B—but is it? Let’s check using the multimeter.

**Step-by-Step Guide:**

- Turn off the power. Always disconnect the Arduino, battery, or power supply before testing.

- Set the multimeter: Turn the dial to continuity mode (sound/beep icon).

- Identify the points to test

    - Pick two points that should be connected, e.g., Arduino 5V pin → LED anode.
      
    - Place the probes: One probe on A, one on B.
      
    - Does it beep?
      
        - Beep → Connection is complete; electricity can flow
          
        - No beep → Broken link; check wire, component, breadboard, or solder join
          
  - Move along the chain and test each segment of the circuit. If continuity is correct along the whole path, the problem lies elsewhere.


