# <a name="customizing-chatcanvascardview"></a>Anpassen von ChatCanvasCardView

Im Gegensatz zur Erstellung, Antwort und Zusammenfassung Ansichten, die html sind, sind Chat Ansichten systemeigenen Ansichten. Informationen zum Anpassen der Kartenansicht Chat, müssen Sie ein Json das Kartenlayout als auch die Werte in der Ansicht bereitzustellen. Ohne eine angepasste Chat Leinen Kartenansicht, der Standardwert Chat Kartenansicht mit dem Text der app-Titel. 

## <a name="views-and-their-supported-properties"></a>Ansichten und deren unterstützten Eigenschaften
Im folgenden sind verschiedene Arten von sub-views/Widgets zusammen mit ihren anpassbaren Eigenschaften. Einige Eigenschaften sind mit <sup>iOS</sup> zurück, der angibt, dass sie nur auf iOS _(und hat keine Auswirkung auf Android)_ anwendbar sind gekennzeichnet.

### <a name="container--view"></a>Container / anzeigen

<ol>
<li>ID (optional, jedoch muss eindeutig sein)</li>
<li>sichtbar<sup>iOS</sup></li>
<li>Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</li>
<li>Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</li>
<li>Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</li>
<li>width</li>
<li>height</li>
<li>Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</li>
<li>BackgroundColor _(nur hex Code hier zulässig)_</li>
<li>cornerRadius</li>
<li>BorderWidthiOS / BorderColoriOS</li>
<li>untergeordnete Elemente _(Array von untergeordneten Ansichten)_</li>
<li>Layout _(vertikale / horizontale When nicht angegeben, wird standardmäßig auf vertikal)_</li>
<li>VerticalAlignment _(oben / unten / zentriert / StretchiOS - wie untergeordnete Elemente vertikal ausgerichtet werden)_</li>
<li>HorizontalAlignment _ (von links/rechts/zentriert/SpaceBetween<sup></sup> iOS/SpaceAround<sup>iOS</sup>) – wie untergeordnete Elemente horizontal ausgerichtet werden. _</li>
<li>InitialHeight<sup>iOS</sup> _eine einzige iOS-Eigenschaft verwendet, in der obersten Container, mit dem die Karte rendern, damit die genaue Dimension worden ist. Es wird dringend empfohlen, diese Eigenschaft für einen reibungsloseren verwenden!_</li>
</ol>

### <a name="text"></a>Text

<ol>
<li>ID (optional, jedoch muss eindeutig sein)</li>
<li>sichtbar<sup>iOS</sup></li>
<li>Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</li>
<li>Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</li>
<li>Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</li>
<li>width</li>
<li>height</li>
<li>Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</li>
<li>BackgroundColor _(nur hex Code hier zulässig)_</li>
<li>cornerRadius</li>
<li>BorderWidthiOS / BorderColoriOS</li>
<li>string</li>
<li>FontSize _(Schriftartfamilie ist immer des Systems Standard, um Probleme beim Rendern zu vermeiden)_</li>
<li>TextColor _(nur hex Code hier zulässig)_</li>
<li>EllipsizeMode _(Head / mittlere / Endezeigern)_</li>
<li>MaxNumberOfLines _(0 für keine Begrenzung, sonst noch Text werden gemäß den Anweisungen in EllipsizeMode abgeschnitten)_</li>
</ol>


### <a name="image"></a>Image

<ol>
<li>ID (optional, jedoch muss eindeutig sein)</li>
<li>sichtbar<sup>iOS</sup></li>
<li>Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</li>
<li>Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</li>
<li>Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</li>
<li>width</li>
<li>height</li>
<li>Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</li>
<li>BackgroundColor _(nur hex Code hier zulässig)_</li>
<li>cornerRadius</li>
<li>BorderWidthiOS / BorderColoriOS</li>
<li>source</li>
<li>ContentMode _ (AspectFit/AspectFill/Dehnen/wiederholen Sie die<sup>iOS</sup>) _</li>
</ol>



## <a name="binding-data-with-views"></a>Binden von Daten mit Ansichten
* __Form__
  * $\{Form.Title}
  * $\{Form.Expiry} - _Ausgabe ist eine Datum-Uhrzeit-Zeichenfolge_
  * $\{Form.Questions}
  * $\{Form.Questions.Length}
  * $\{Form.Questions[questionId].Title}
  * $\{Form.Questions[questionId].Options}
  * $\{Form.Questions[questionId].Options.Length}
  * $\{Form.Questions[questionId].Options[optionId].Text}
  * $\{Form.Questions[questionId].Options[optionId].pictureUrl}
  * $\{Form.Properties}
  * $\{Form.Properties.Length}
  * $\{Form.Properties[PropertyName]}
  * $\{Form.Properties[PropertyName].Value}
  * $\{Form.Properties[PropertyName].length} - _für Array/Set Type-Eigenschaft_
* __MyLatestResponse__
  * $\{MyLatestResponse.sendTime} - _Ausgabe ist eine Datum-Uhrzeit-Zeichenfolge_
  * $\{MyLatestResponse.questionToAnswerMap[questionId]}
* __Zusammenfassung__
  * $\{Summary.totalResponseCount}
  * $\{Summary.totalParticipantsCount}
  * $\{Summary.targetResponderCount}

Außerdem können eine diese Variablen als Platzhalter, wie folgt verwenden:  
_"Vielen Dank für Ihre News-Bericht: ${Form.properties[newsDescription].value}"_

## <a name="operations"></a>Vorgänge

In einigen Szenarien auftreten gibt es muss, in denen möglicherweise unterschiedliche Benutzer müssen verschiedene Chat-Karte anzeigen, die basiert auf einige Attribute. Um diese Szenarien zu ermöglichen, bietet Kaizala [Operatoren](Operator.md), mit dem Ersteller der Aktion auf Chat Kartenansichten für die gleiche Aktionsinstanz unterschiedlich für verschiedene Szenarien/Benutzer personalisieren können.

Sie können beispielsweise Anzeigen einer anderen Kartenansicht für Benutzer, die nicht den Auftrag abgeschlossen haben, und eine andere Kartenansicht für Benutzer, die den Auftrag abgeschlossen haben. Dies kann für jede Art von Szenarien erweitert werden, die auftreten können.

## <a name="how-to-provide-the-json-schema"></a>Zum Bereitstellen des Json-Schemas
In der Datei manifest _(package.json)_ eines Pakets, platzieren Sie den Namen der JSON **SourceLocation** ist Schlüssel in **ChatCanvasCardView** unten einen Beispielsnapshot package.json:

![Momentaufnahme der package.json](./chatcardviewjson.png)

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
