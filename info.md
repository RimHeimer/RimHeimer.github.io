---
title: Info
layout: page
permalink: /info
---

<link rel="stylesheet" href="{{- 'assets/css/core.css' | relative_url -}} "/>
<script src="{{- 'assets/js/tabs.js' | relative_url -}}"></script>
<script src="{{- 'assets/js/filter.js' | relative_url -}}"></script>
<script src="https://www.kryogenix.org/code/browser/sorttable/sorttable.js"></script>

{%- assign utils = false -%}
{%- assign lootboxes = false -%}
{%- assign puppeteer = false -%}
{%- for mod in site.data.modlist -%}
    {%- case mod.name -%}
        {%- when 'ToolkitUtils' %}
            {%- assign utils = true -%}
        {%- when 'ToolkitUtils - Testing' -%}
            {%- assign utils = true -%}
        {%- when 'Puppeteer' -%}
            {%- assign puppeteer = true -%}
        {%- when 'TwitchToolkit - Lootboxes' -%}
            {%- assign lootboxes = true -%}
    {%- endcase -%}
{%- endfor -%}


{%- assign bal = '!bal' -%}
{%- assign buy = '!buy' -%}
{%- for command in site.data.commands -%}
    {%- if command.data.isBal -%}
        {%- assign bal = command.usage -%}
        {%- continue -%}
    {%- endif -%}

    {%- if command.data.isBuy -%}
        {%- assign buy = command.usage -%}
        {%- continue -%}
    {%- endif -%}
{%- endfor -%}

# Wilkommen

Wilkommen zu [{{ site.data.social.twitch }}](https://twitch.tv/{{ site.data.social.twitch }})'s Stream.
Ceraph nutzt die Rimworld Mod
[Twitch Toolkit](https://steamcommunity.com/sharedfiles/filedetails/?id=1718525787) um mit seinen Zuschauern gemeinsam ein Interaktives Rimworld Chaos zu schaffen. 
Vieles an dieser Mod mag am Anfang recht kompliziert erscheinen, nur hoffen wir, das diese kurze Anleitung dabei helfen kann im Ansatz zu verstehen, wie diese Mod funktioniert.

## Was ist eingentlich dieses Twitch Toolkit?

Twitch Toolkit ist eine Rimworld Mod von hodlhodl, die es den Zuschauern erlaubt das Spiel bzw die Kolonie auf viele verschiedene 
Arten zu beinflussen. Im guten wie auch im schlechten. Ganz wonach euch der Sinn steht. Das wichtigsten ist wohl der [Store]({{- "/" | relative_url -}}),
wo es dir möglich ist die verschiedenste Sachen mit Münzen zu kaufen. Je nachdem was ihr kauft erscheint es dann innerhalb der Kolonie,
löst eins der vielen möglichen Events aus oder beeinflusst die Kolonie in anderer Art und Weise. 
Ein weiterer Weg der Interaktion mit der Kolonie bzw Ceraph sind die immer mal wieder auftauchenden Abstimmungen. Bei diesen werden dann meist
3 Optionen vom Spiel vorgegeben, bei welcher man dann mit passender Zahl im Chat abstimmen kann. Die Abstimmungen werden stark davon beeinflusst, was Ceraph im Vorfeld eingestellt hat.

## Was sind Münzen?

Münzen sind die Währund dieser Mod. Du kannst dir deinen aktuellen Kontostand via Chatbefehl `{{ bal }}` jederzeit ansehen.
Münzen brauchst für jeder Interaktion mit der Kolonie. 

{% if utils == true %}
Du hast evtl gemerkt, das es in deiner Kontostandnachricht neue Emotes gibt. Wenn dem so ist hier eine kurze übersicht über diese:

- 💰 Zeigt dir die Menge an Münzen die du aktuell hast.
- ⚖ Zeigt dir dein aktuelles Karma.
- 📈 Gibt an wie viele Münzen du pro Zyklus dazu bekommst+.
- 📉 Gibt an wie viele Münzen du pro Zyklus verlierst.

{% endif %}

{%- if lootboxes == true -%}
## Lootboxen
Du hast bestimmt außerdem bemerkt, das du eine Nachricht über eine Lootbox erhalten hast. Du kannst diese Lootboxen
mit Hilfe des Chatbefehls `!openlootbox` öffnen. Außerdem kannst du mit dem Chatbefehl `!lootboxes` überprüfen wie viele Lootboxen du hast.
You'll always get a new lootbox everyday.
{%- endif -%}

<br/>
## Was ist Karma?

Karma ist ein System innerhalb von Twitch Toolkit das versucht die Anzahl negativer Ereignisse zu begrenzen,
die einer von euch auf mal kaufen kann. Dieses System funktioniert so, das es einen direkten Einfluss darauf hat,
wie viele Münzen ihr pro Zyklus bekommt bzw verliert. Genauer gesagt, sorgt ein hoher Karmawert für mehr Münzen
pro Zyklus und ein niedriger bzw negativer Karmawert sorgt dafür, das ihr Münzen verliert. Die Hoffnung dahinter ist,
das sich negative Events dadurch mehr verteilen und die Kolonie sich zwischendurch erholen kann.

## Wie benutze ich das Twitch Toolkit?

Du kannst das Toolkit auf verschiedenste Weise nutzen. Die prominenteste Art und Weise sind hierbei wohl die
[Befehle]({{- "/commands" | relative_url -}}). Der wichtigstes Befehl ist allerdings der `{{- buy -}}` Befehl,
welcher dich die verschiedensten Sachen aus den Store kaufen lässt. Ein weiterer erwähnungswerter Befehl ist
der `!mypawn` Befehl, dieser erlaubt dir eine vielzahl an Infomationen über deinen Pawn abzurufen. Um jeden
Befehl hier nun zu erklären ist viel zu wenig Platz. Du kannst daher die komplette Liste der [Befehle]({{- "/commands" | relative_url -}})
hier einsehen.

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

Du hast es bis ans Ende der Info Seite geschaft <img src="assets/img/3.0.gif"> lorem ipsum <br/>
 Der `{{- buy -}}` Befehlt lässt sich im übrigen durch ein simples $ ersetzen. <br/>

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.   

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.   

Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.   

Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.   

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis.   

At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, At accusam aliquyam diam diam dolore dolores duo eirmod eos erat, et nonumy sed tempor et et invidunt justo labore Stet clita ea et gubergren, kasd magna no rebum. sanctus sea sed takimata ut vero voluptua. est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.   

Consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus.   

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.   

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.   

Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.   

Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo