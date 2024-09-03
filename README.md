# Cyber-security-dataset-of-EDS

## Attack Model
The types of attacks and implementation criteria designed by attackers with different capabilities are presented as below. The experimental platform allows for the design of attack types that cover all aspects of digital inputs, control parameters and analog inputs. The level of attack increases gradually, starting with network access and progressively acquiring the knowledge required for the attack to realize advanced stealth attacks.
<div align=center>  
  <img src="images/Attacker_capabilities.png" alt="Attacker capabilities and corresponding attack types" width="50%">  
</div>  

1. Access to ICS network
   - Attackers focus on gathering information about the topology and devices in the industrial control network. 
     - Information Leakage: Use scanning tools to obtain critical information such as IP addresses, device models, and operating systems of the devices on the industrial control network.  
     - Replay Attack: Resend the eavesdropped data to the receiver without knowing the exact meaning of the specific data being replayed.

2. Understand Physical Processes
   - Attackers conduct in-depth research on control programs and relevant materials to understand the physical significance of each point in the PLC.
     - Command Injection: Manipulate system behavior or gain unauthorized access by inserting malicious commands into the input. 
     - Sensor Data Tampering: Maliciously manipulate the parameters of sensors to deceive the system.

3. Understand Control Logic
   - Attackers possess higher technical skills.
     - Control Parameter Tampering: Collect and analyze extensive normal data to gain an in-depth understanding of the system’s operational patterns and the logical relationships between different points, so as to achieve control parameter tampering.
     - Multi-Point Attack: Adopt more covert attack methods, design multiple control commands to execute coordinated attacks, aiming to control and disrupt the system without arousing excessive suspicion.

4. Access to Field Devices
   - Unlike the previous categories that are limited to network penetration, physical attackers can directly access the location of the control equipment through social engineering means.
     - Physical Attack: Including damaging equipment, manipulating operations, or exploiting the help of internal employees to execute attacks.

## Cyber-security Testbed
To construct a testbed that better aligns with real-world scenarios and reduces the sim-to-real gap, we employ a real EDS prototype as depicted in Fig. 4. The system is scaled down yet fully functional, capable of achieving both cold startup and normal operation scenarios.
### Process Flow of the EDS
The control system of the EDS testbed is shown in Fig. 4(a), where the PLC serves as the central control device responsible for monitoring and controlling parameters such as temperature, flow rate, and liquid level. HMI provides operation options for the operator, including start and stop operation, change working conditions, change target parameters, also monitor the condition of EDS. As shown in Fig. 4(b), physical experimental setup of EDS is physically applicable for the separation of ethanol and water mixtures. The process flow of the EDS, as shown in Fig. 4(c), involves 3 control loops working in synergy: Loop 1 - Temperature controller (TC), Loop 2 - Flow controller (FC), Loop 3 - Liquid level controller (LC). These control loops collectively guarantee the efficient and stable operation of the Ethanol distillation process. By precisely controlling temperature, flow rate, and liquid level, the system achieves the desired separation of Ethanol and water, ultimately producing high-purity Ethanol.
### Attack Implemention
Attacks are implemented using a combination of snap7 libraries and self-built packets. Different methods and tools were used to implement the attacks for different types of attacks, such as information leakage, sensor tampering, actuator data tampering and control parameter tampering, which were obtained by repeating five trials for each attack. For the attacks on information leakage, the man-in-the-middle attack tool of Ettercap and the information acquisition function of snap7 were used. For sensor tampering, actuator data tampering, and control parameter tampering attacks, point coercion packets were created after communication was established using snap7. Physical attacks are realized by artificially opening normally closed valves, causing liquid leakage from the reactor.
### Communications
The cybersecurity dataset is collected using the snap7 library in Python through communication scripts that interact with the PLC at regular intervals.
## Dataset Description

# Citation
Please cite the following paper if you use this dataset: Y. Xue, J. Pan, Y. Geng, Z. Yang, M. Liu and R. Deng, "Real-Time Intrusion Detection Based on Decision Fusion in Industrial Control Systems," in IEEE Transactions on Industrial Cyber-Physical Systems, vol. 2, pp. 143-153, 2024, doi: 10.1109/TICPS.2024.3406505.


```
@ARTICLE{10540291,
  author={Xue, Yawen and Pan, Jie and Geng, Yangyang and Yang, Zeyu and Liu, Mengxiang and Deng, Ruilong},
  journal={IEEE Transactions on Industrial Cyber-Physical Systems}, 
  title={Real-Time Intrusion Detection Based on Decision Fusion in Industrial Control Systems}, 
  year={2024},
  volume={2},
  number={},
  pages={143-153},
  keywords={Security;Intrusion detection;Integrated circuit modeling;Real-time systems;Data models;Computer security;Production;Cybersecurity datasets;decision fusion;industrial control systems;intrusion detection},
  doi={10.1109/TICPS.2024.3406505}}
```
