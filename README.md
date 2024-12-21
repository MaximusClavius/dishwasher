# dishwasher/opvasker
Automatisering af opvasker/Automation of dishwasher

<p><strong>Bemærk:</strong> Der er kommet nye programmer til opvaskeren som kan downloades via Home Connect appen. Yderligere er der kommet en sensor til salt (sensor.opvaskemaskine_salt_nearly_empty) og afspænding (sensor.opvaskemaskine_rinse_aid_nearly_empty).</p>

<p><strong>Forudsætning:</strong>
- Opvaske- eller vaskemaskine er integreret i Home Connect i Home Assistant
- Remote Start og Control er enabled på maskinen
- Et medie Frk. Goggle kan ævle fra/i
- Billigste el-pris er givet via en sensor (min sensor indeholder billigste pris for en dobbelt-time)</p>

![image](https://user-images.githubusercontent.com/103023823/223043170-354f9fc6-b945-4371-899b-570230649db8.png)

Automatiseringer kører når der er tændt for strømmet og når låge er lukket. Så beregnes antal sekunder til starttidspunkt, og vaske-program vælges fra input_select: "opvaskemaskine_program:". På opvaskemaskinens display viser antal hele timer til start.

Hvis lågen ikke er lukket, så fortæller Frk. Google det ("Home Connect" er en cloud-løsning, så der kan forekomme nogle forsinkelser).
Er alt ok, så fortæller Frk. Google det, og fortæller hvor opvaskemakinen starter, samt hvad alternativet er. Afbryd er at slukke for strømmen på kontakten på opvaskeren- eller vaskemaskinen.

Fremgangsmåde:
1) Lave input_select og tilføj den til dashboard, evt. med udgangspunkt i: https://github.com/MaximusClavius/dishwasher/blob/main/input_select
2) Lave automatisering med dine tilpasninger, evt. med udgangspunkt i: https://github.com/MaximusClavius/dishwasher/blob/main/automation

PS<br>
I automationen er vist hvorledes man sender en besked til mobiltelefonen via servicen: notify, dog er den disabled (enabled: false)

Hvis du mangler opvaskemaskinens vaske-program-navne, så ligger de her: https://github.com/MaximusClavius/dishwasher/blob/main/dishwasher%20programs eller på Home Connect API docs: https://api-docs.home-connect.com/programs-and-options#dishwasher

<a href="https://www.paypal.com/donate/?hosted_button_id=NNUF56TVFMJXY"><img src="https://www.paypalobjects.com/da_DK/DK/i/btn/btn_donateCC_LG.gif" alt="Doner en skræv"></a>
