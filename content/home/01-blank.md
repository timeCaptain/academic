---
widget: blank
headless: true

# ... Put Your Section Options Here (title etc.) ...
title: Widget - Blank
subtitle:
weight: 10  # section position on page
active: true  # Activate this widget? true/false
design:
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns: '1'
  background:
    color: 'Navy'
    text_color_light: true

---
Add any content here - text, images, videos, galleries - and even HTML code!


## Überschriften:
{style="color: red"}
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5

## Hervorhebungen:
{style="color: red"}
Italic: mit _Unterstrichen_ _.

Fett: mit **Doppelsternen** **.

Kombiniert: mit **Doppelsternen and _Unterstrichen_**.

Durchgestrichen: mit ~~Doppeltilden~~ ~~.

Farbiger Text: mit HTML (style-Tag)
{style="color: green"}

Zitat: mit gt-Zeichen: 
> This is a blockquote.

Hervorhebung: mit hl-shortcode: This is a {{< hl >}}highlighted quote{{< /hl >}}.

## Auflistungen:
{style="color: red"}

ordered Lists: 
1. First item
   1. A sub-item
2. Another item

unordered Lists:
- First item
  - A sub-item
- Another item

ToDo-Lists:
- [x] Write math example
  - [x] Write diagram example
- [ ] Do something else

Aufklapplisten: mit spoiler-shortcode
{{< spoiler text="Klick hier für den Einkaufszettel" >}}
1. Mehl
2. Eier
3. Milch
4. Schokolade
{{< /spoiler >}}

## Links:
{style="color: red"}

[Externer Link zu google](https://www.google.com)

[Link zu einem Projekt]({{< relref "/landing/index.md" >}})

[Scroll zu einer page section mit der Überschrift *Hi*](#hi)

{{% staticref "uploads/cv.pdf" "newtab" %}}PDF_Download: mit shortcode staticref - Datei muss im Verzeichnis static/uploads/ gespeichert sein{{% /staticref %}}

Zitat1 (Stream):
{style="color: green"}
{{< cite page="/landing/index.md" view="1" >}}

Zitat2 (Compact):
{style="color: green"}
{{< cite page="/landing/index.md" view="2" >}}

Zitat3 (Card):
{style="color: green"}
{{< cite page="/landing/index.md" view="3" >}}

Zitat4 (Traditional - as configured by the citation_style setting in params.yaml):
{style="color: green"}
{{< cite page="/landing/index.md" view="4" >}}

## Inhaltsverzeichnis 
{style="color: red"} 

uber toc-shortcode
{{< toc >}}

Für umfangreiche Dokumentationen kann auch das book-layout gewählt werden (type: book)

Fußnoten:
Ich habe noch mehr zu sagen [^1].
Jetzt ist mir noch was eingefallen [^2]

[^1]: Fußnoten-Beispiel.
[^2]: Zweites Beispiel.

Tags und Kategorien auflisten:

Tags: 
{style="color: green"}
{{< list_tags >}} 

Categories: 
{style="color: green"}
{{< list_categories >}} 

Call-to-Action Buttons mit dem CTA-shortcode.

Example CTA button:

{{< cta cta_text="Do something" cta_link="/" cta_new_tab="false" >}}

{{< cta cta_text="Begin the course Python" cta_link="kapitel1" >}}

{{< cta cta_text="Do something" cta_link="/" cta_new_tab="false" cta_alt_text="Alternative action" cta_alt_link="/" cta_alt_new_tab="false" >}}

Unterseiten auflisten, wie z.B. Buchkapitel (sofern vorhanden): 
{{< list_children >}}

## Bilder
{style="color: red"} 

Einzel-Bilder per Markdown: ![screen reader text](teufel.jpg "Teufel")

Einzel-Bilder per figure-shortcode: {{< figure src="teufel.jpg" caption="A caption" numbered="true" >}}

dynamically theme images, jpg:

{{< figure src="teufel.jpg" caption="test" theme="light" >}}
{{< figure src="teufel.jpg" caption="test" theme="dark" >}}

Bilder-Gallerie
  
1. Photo-Album erstellen unter assets/media/albums/
2. gallery-shortcode einfügen {{< gallery album="animals" >}} 
3. Optional, um für die Bilder Untertitel hinzuzufügen images, können folgende Zeilen am Ende des Fontmatters hinzugefügt werden

gallery_item:
- album: <ALBUM FOLDER>
  image: <IMAGE 1 NAME>.jpg
  caption: Write your image 1 caption here
- album: <ALBUM FOLDER>
  image: <IMAGE 2 NAME>.jpg
  caption: Write your image 2 caption here

Inline-Bilder (Icons): mit Icon-shortcode

Terminal {{< icon name="terminal" pack="fas" >}} Terminal  
Python {{< icon name="python" pack="fab" padding_left="3">}} Python 

Python {{< icon name="python" pack="fab" >}} Python  

Python {{< icon name="python" pack="fab" padding_right="3">}} Python

Emojis (Emoji cheat sheet: https://www.webfx.com/tools/emoji-cheat-sheet/)

:de:
:hourglass_flowing_sand:
:file_folder:
:paperclip:
:pushpin:
:moneybag:
:euro:
:dart:
:heavy_check_mark:
:wavy_dash:

## Callouts
{style="color: red"} 

callout notes

{{% callout note %}}
A Markdown callout is useful for displaying notices, hints, or definitions to your readers.
{{% /callout %}}

callout warnings
{{% callout warning %}}
Here's some important information...
{{% /callout %}}


## Audio
{style="color: red"} 

{{< audio src="mp3sample.mp3" >}}

## Video
{style="color: red"} 

Video aus dem Verzeichnis static/media/ :

{{< video library="true" src="test.mp4" controls="yes" >}}

Video aus dem Seitenordner :
{{< video src="test.mp4" controls="yes" >}}

Youtube:

{{< youtube ni88uy9WavY >}}

## Code highlighting
{style="color: red"} 

Pass the language of the code, such as python, as a parameter after three backticks:

```python
# Example of code highlighting
input_string_var = input("Enter some data: ")
print("You entered: {}".format(input_string_var))
```

## Tabellen

Hilfsmittel: https://www.tablesgenerator.com/markdown_tables

Einsetzen
|  2021   	| Januar 	| Februar 	| März  	| April  	|
|---------	|--------	|:-------:	|-------	|--------	|
| Kochen  	| Maria  	| Puppi   	| Ölm   	|  Maria 	|
| Putzen  	| Ölm    	| Maria   	| Puppi 	| Ölm    	|
| Waschen 	| Puppi  	| Ölm     	| Maria 	| Puppi  	|