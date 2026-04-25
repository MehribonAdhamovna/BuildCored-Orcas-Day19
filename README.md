# BuildCored-Orcas-Day19
I2CPlayground — BUILDCORED ORCAS Day 19

What it does. This code acts like a digital translator that turns numbers and commands into the specific language of electrical pulses (SDA and SCL signals) so a sensor can understand them. It then draws those pulses on a graph so you can actually see the data traveling through the wires in real time.

Hardware concept. The I2C protocol is a synchronous, multislave serial communication bus that utilizes two bidirectional lines Serial Data (SDA) and Serial Clock (SCL) to facilitate data exchange. It relies on a masterdriven clock and unique 7 bit device addressing to enable communication between a central processor and multiple peripheral sensors over a shared physical medium.

Screen Recording. https://drive.google.com/file/d/1FB1JYAy7DiFK6Du-uOE5fyWpEH9QX2G8/view?usp=sharing

What I would do differently. I’d add a "timeout" safety switch so the code doesn't freeze forever if a slave chip gets stuck while stretching the clock. I'd also probably organize the data into a "Class" structure to make it easier to swap between different sensors, like a thermometer or a GPS, without rewriting the main logic.

Run it. python day19_starter.py
