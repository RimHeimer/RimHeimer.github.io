---
title: Info
layout: page
permalink: /info
---

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


{%- if puppeteer -%}
<br/>
## What is Puppeteer?

[Puppeteer](https://steamcommunity.com/sharedfiles/filedetails/?id=2057192142) is a mod by Brrainz that
allows viewers to directly control their pawns, and even view a number of information about your pawn in
a graphical way. It also redirects some of the responses from Twitch Toolkit to its website to clean up
chat a bit. So, if you're logged into Puppeeter and you're wondering why the bot isn't responding to you,
you should check the `TT` tab on the website first.
{%- endif -%}
