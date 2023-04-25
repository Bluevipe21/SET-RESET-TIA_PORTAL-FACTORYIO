# Ejemplo de un set y reset utilizando TIA PORTAL y Factoryio

This is an example of the use of the set and reset functions in a PLC. The code was created using the ladder language in the tia portal software v15. To verify the operation, the factoryio 3D simulation software was used. Factoryio works as training software for different PLC platforms.  ( [Click here for more information](https://docs.factoryio.com/) ). 

---

## Utilización de factoryio con tia portal

To connect Factory IO with TIA Portal, you can download the templates depending on the version of TIA Portal you are using at the following [link](https://docs.factoryio.com/tutorials/siemens/setting-up-s7-plcsim-v13/#tia-portal-template-projects). These templates contain a file, in this case called __MHJ-PLC-Lab-Function-S71200__, which is responsible for establishing the connection with TIA Portal as if it were physically connected. We will copy this file into our project and call it within our main block. To ensure that the addressing is consistent with that of Factory IO, we must change the properties of our project. To do this, follow these steps:

- Right-click on the folder of our PLC (where it says something like: PLC_1 [CPU 1212C AC/DC/RLY]) and click on Properties.
- Then in the General tab, click on the I/O Addresses section and change the Initial Addressing to 10.
- Then navigate to the Protection and Security tab and go to the section that says Connection Mechanisms. Check the box that says Allow access via remote interlocutor's PUT/GET communication.

With the above steps, we will have enabled communication with Factory IO. Finally, we just need to verify that the input and output addressing is correct, meaning that it matches that established in the PLC ladder program.


### [Scene created in Factory IO](https://drive.google.com/file/d/1YXIbnCdtQzOsWUAxKyq5qBdlVM4UxTAd/view?usp=sharing)
