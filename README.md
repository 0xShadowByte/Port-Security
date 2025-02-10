# Switch Port Security - CISCO

### Objective
  
Understand the importance of switch Port Security in safeguarding networks from unauthorized access.
Learn how to implement best practices for Port Security in a workplace environment.
Familiarize with Cisco commands for enabling and configuring Port Security.
Gain knowledge of different security modes and MAC address configuration methods.
Learn how to verify Port Security settings and monitor for violations.

### Skills Learned

- Ability to disable unused ports to enhance network security.
- Proficiency in configuring Port Security features such as MAC filtering and port lockdown.
- Understanding of the three security modes: shutdown, protect, and restrict.
- Capability to set MAC addresses statically, dynamically, or using the sticky method.
- Competence in using verification commands to check Port Security status and troubleshoot issues.

### Tools Used

- CISCO Packet Tracer

### Steps

*Ref 1: Setting up an example of switch port security with 3 PCs, 1 switch and 1 laptop in a workplace.*

It's important to implement network port security in the workplace to prevent unauthorized access and rogue devices forom compromising network security. A fundamental practice is to disable unused poorts, especially in vacant offices or during guest access point setups. There are three security modes: shutdown (default), protect and restrict. Each mode has different responses to unauthorized devices. The shutdown mode disables the port upon a violatioon, while protect and restrict modes allow known MAC addresses but differ in notification handling. MAC addresses can be configured statically, dynamically, or using MAC address sticky with sticky being preferred for ease of management. Static addresses require manual entry, while dynamic addresses are learned automatically but not retained after a reboot. 

![image](https://github.com/user-attachments/assets/45fea850-cda8-4504-ac69-d9ba64863f44)

*Ref 2: Using the CLI command to see if there are port security on any of the switch ports.*

We use the statement "en" - to enable privilage exact mode, and "sh port-security" to show if port security has been set up for the switch ports. Nothing showed up then we use "sh port-security interface fa0/1" to give us more information on the port security provided. As we look closely port security is disabled and violation mode is set to shutdown, which is the default violation mode.

![image](https://github.com/user-attachments/assets/d7416e7c-4744-46d9-8a38-a0049d752da3)

### 1st Scenario - MAC address: Static, violation mode: Protect 

For the first scenario we are going to set up the device MAC addresses as static and then the violation mode to oprotect. Take note before we start configuring the switch with port security that it is disabled by default so you have to manually enable it by using commands and also you can only configure port security on access ports you can't do this on trunk ports or eitehr channel ports.

*Ref 3: MAC address for PC3 is "0002.1769.5791" (click on PC3 > Config > FastEthernet0)*

![image](https://github.com/user-attachments/assets/ccd658aa-87de-49ef-9ffc-5629ddcbe652)


