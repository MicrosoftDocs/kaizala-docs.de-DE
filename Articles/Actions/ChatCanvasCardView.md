# <a name="customizing-chatcanvascardview"></a>Anpassen von ChatCanvasCardView

Im Gegensatz zu den Erstellungs-, Antwort-und zusammenfassungsansichten, die HTML sind, sind Chat Ansichten systemeigene Ansichten. Zum Anpassen der Chat Kartenansicht müssen Sie eine JSON des Kartenlayouts sowie die Werte in der Ansicht angeben. Fehlt eine angepasste Chat Canvas-Kartenansicht, lautet die standardmäßige Chat Kartenansicht mit dem Text des App-Titels. 

## <a name="views-and-their-supported-properties"></a>Ansichten und ihre unterstützten Eigenschaften
Nachfolgend finden Sie verschiedene Arten von unter Ansichten/Widgets zusammen mit ihren anpassbaren Eigenschaften. Nur wenige Eigenschaften sind mit <sup>IOS</sup> gekennzeichnet, was darauf hinweist, dass Sie nur für IOS gelten _(und keine Auswirkungen auf Android haben)_.

### <a name="container--view"></a>Container/Ansicht

<ol>
<li>ID (optional, muss jedoch eindeutig sein)</li>
<li>Visible<sup>IOS</sup></li>
<li>Typ _(einer der unter Ansichtstypen, die wir hier erwähnen)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>Gewichtung _(Prozentsatz der Breite/Höhe der übergeordneten Ansicht bei horizontalen/vertikalen Layouts)_</li>
<li>Background Color _(nur Hexadezimalcode hier zulässig)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>Children _(Array der untergeordneten Ansichten)_</li>
<li>Layout _(vertikal/horizontal, wenn nicht angegeben, standardmäßig vertikal)_</li>
<li>verticalAlignment _(oben/unten/Mitte/stretchiOS – wie untergeordnete Elemente vertikal ausgerichtet werden)_</li>
<li>horizontalAlignment _ (Left/Right/Center/spaceBetween<sup>IOS</sup> /spaceAround<sup>IOS</sup>)-wie untergeordnete Elemente horizontal ausgerichtet werden. _</li>
<li>initialHeight<sup>IOS</sup> _eine nur-IOS-Eigenschaft, die im obersten Container verwendet wird, die zum Rendern der Karte verwendet wird, bevor die genaue Dimension ermittelt wird. Es wird dringend empfohlen, diese Eigenschaft für eine reibungslosere Erfahrung zu verwenden!_</li>
</ol>

### <a name="text"></a>Text

<ol>
<li>ID (optional, muss jedoch eindeutig sein)</li>
<li>Visible<sup>IOS</sup></li>
<li>Typ _(einer der unter Ansichtstypen, die wir hier erwähnen)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>Gewichtung _(Prozentsatz der Breite/Höhe der übergeordneten Ansicht bei horizontalen/vertikalen Layouts)_</li>
<li>Background Color _(nur Hexadezimalcode hier zulässig)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>string</li>
<li>fontSize _(Schriftfamilie ist immer System Standard, um Probleme beim Rendern zu vermeiden)_</li>
<li>TextColor _(nur Hexadezimalcode hier zulässig)_</li>
<li>ellipsizeMode _(Head/Middle/Tail)_</li>
<li>maxNumberOfLines _(0 für keine Begrenzung, andernfalls wird der Text nach ellipsizeMode abgeschnitten)_</li>
</ol>


### <a name="image"></a>Image

<ol>
<li>ID (optional, muss jedoch eindeutig sein)</li>
<li>Visible<sup>IOS</sup></li>
<li>Typ _(einer der unter Ansichtstypen, die wir hier erwähnen)_</li>
<li>Margin/marginTop/marginRight/marginBottom/marginLeft</li>
<li>Padding/paddingTop/paddingRight/paddingBottom/paddingLeft</li>
<li>width</li>
<li>height</li>
<li>Gewichtung _(Prozentsatz der Breite/Höhe der übergeordneten Ansicht bei horizontalen/vertikalen Layouts)_</li>
<li>Background Color _(nur Hexadezimalcode hier zulässig)_</li>
<li>cornerRadius</li>
<li>borderWidthiOS/borderColoriOS</li>
<li>source</li>
<li>contentMode _ (aspectFit/aspectFill/Stretch/Repeat<sup>IOS</sup>) _</li>
</ol>



## <a name="binding-data-with-views"></a>Binden von Daten mit Ansichten
* __Form__
  * $\{Form. Title}
  * $\{Form. expire} – _die Ausgabe ist eine Zeichenfolge mit Datum und Uhrzeit_ .
  * $\{Formular. questions}
  * $\{Form. questions. length}
  * $\{Formular. Fragen [Question-Nr]. Title}
  * $\{Formular. Fragen [Question-Nr]. Optionen}
  * $\{Formular. Fragen [Question-Nr]. Options. length}
  * $\{Formular. Fragen [Question-Nr]. options [options-Nr.]. Text}
  * $\{Formular. Fragen [Question-Nr]. options [options-Nr.]. pictureUrl}
  * $\{Form. Properties}
  * $\{Form. Properties. length}
  * $\{Form. Properties [propertyName]}
  * $\{Form. Properties [propertyName]. Value}
  * $\{Form. Properties [propertyName]. Length}- _für Array/Set Type-Eigenschaft_
* __MyLatestResponse__
  * $\{MyLatestResponse. Send Time}- _Output ist eine Zeichenfolge mit Datum und Uhrzeit_
  * $\{MyLatestResponse. questionToAnswerMap [Question-out]}
* __Zusammenfassung__
  * $\{Summary. totalResponseCount}
  * $\{Summary. totalParticipantsCount}
  * $\{Summary. targetResponderCount}

Außerdem können diese Variablen als Platzhalter verwendet werden, wie etwa:  
_"Vielen Dank für Ihren Nachrichten Bericht: $ {Form. Properties [newsDescription]. Value}"_

## <a name="operations"></a>Vorgänge

In einigen Szenarien kann es erforderlich sein, dass andere Benutzer möglicherweise andere Chat Karten anzeigen müssen, die möglicherweise auf einigen Attributen basieren. Um solche Szenarien zu ermöglichen, stellt Kaizala [Operatoren](Operator.md)bereit, die es Aktions Erstellern ermöglichen, die Ansichten von Chat Karten für die gleiche Aktionsinstanz für unterschiedliche Szenarien/Benutzer anders zu gestalten.

Sie können beispielsweise eine andere Kartenansicht für Benutzer anzeigen, die den Auftrag nicht abgeschlossen haben, und eine andere Kartenansicht für Benutzer, die den Auftrag abgeschlossen haben. Dies kann auf alle Arten von Szenarien ausgedehnt werden, die möglicherweise auftreten.

## <a name="how-to-provide-the-json-schema"></a>VorGehensWeise Bereitstellen des JSON-Schemas
Legen Sie in der Manifestdatei _(Package. Json)_ eines Pakets den JSON-Dateinamen unter **SourceLocation** -Schlüssel in **ChatCanvasCardView** unten ist ein Beispiel-Snapshot aus Package. JSON:

![Momentaufnahme von Package. JSON](./chatcardviewjson.png)

## <a name="example-chatcanvascardview-source-file"></a>Beispiel ChatCanvasCardView-Quelldatei
```json
{
    "schemaVersion": 1,
    "schema": {
        "type": "container",
        "initialHeight": 300,
        "layout": "vertical",
        "children": [
            {
                "type": "text",
                "paddingLeft": 10,
                "paddingRight": 10,
                "string": "${Form.properties[Property1].value}",
                "fontSize": 18,
                "fontStyle": "bold",
                "textColor": "#CE222E",
                "textAlignment": "left",
                "maxNumberOfLines": 2,
                "marginBottom": 10
            },
            {
                "type": "image",
                "height": 160,
                "source": "${Form.properties[CoverImageProperty].value}",
                "contentMode": "aspectFit",
                "backgroundColor": "#263749",
                "marginBottom": 10
            },
            {
                "type": "text",
                "paddingLeft": 10,
                "paddingRight": 10,
                "string": "${Form.properties[Property2].value}",
                "fontSize": 18,
                "fontStyle": "bold",
                "textColor": "#32495f",
                "textAlignment": "left",
                "maxNumberOfLines": 4,
                "marginBottom": 0
            }
        ]
    }
}
