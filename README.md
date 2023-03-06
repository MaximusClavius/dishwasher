# dishwasher
Automatisering af opvasker/Automation of dishwasher

Forudsætning:
- Opvaske- eller vaksemaskine er integreret i Home Connect i Home Assistant.
- Remote Start og Control er enabled på maskinen.
- Billigste el-pris er givet via en sensor (min sensor indeholder billigste pris for en dobbelt-time)

![image](https://user-images.githubusercontent.com/103023823/223043170-354f9fc6-b945-4371-899b-570230649db8.png)

Automatiseringer kører når der er tændt for strømmet og når låge er lukket. Så beregnes antal sekunder til starttidspunkt, og vaske-program vælges fra input_select: "opvaskemaskine_program:". På opvaskemaskinens display viser antal hele timer til start.

Hvis lågen ikke er lukket, så fortæller Frk. Google det ("Home Connect" er en cloud-løsning, så der kan forekomme nogle forsinkelser).
Er alt ok, så fortæller Frk. Google det, og fortæller hvor opvaskemakinen starter, samt hvad alternativet er. Afbryd er at slukke for strømmen på kontakten på opvaskeren.

Hvis du mangler opvaskemaskinens vaske-program-navne, så ligger de her: https://github.com/MaximusClavius/dishwasher/blob/main/dishwasher%20programs eller på Home Connect API docs: https://api-docs.home-connect.com/programs-and-options#dishwasher
