# dishwasher
Automatisering af opvasker/Automation of dishwasher

Forudsætning:
- Opvaske- eller vaksemaskine er integreret i Home Connect i Home Assistant.
- Billigste el-pris er givet via en sensor (min sensor indeholder billigste pris for en dobbelt-time)

![image](https://user-images.githubusercontent.com/103023823/223043170-354f9fc6-b945-4371-899b-570230649db8.png)

Automatiseringer kører når der er tændt for strømmet og når låge er lukket. Så beregnes antal sekunder til starttidspunkt, og vaske-program vælges fra input_select: "opvaskemaskine_program:". På display'et viser antal hele timer til start.
