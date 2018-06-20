# <a name="customizing-chatcanvascardview"></a><span data-ttu-id="a18e0-101">Anpassen von ChatCanvasCardView</span><span class="sxs-lookup"><span data-stu-id="a18e0-101">Customizing ChatCanvasCardView</span></span>

<span data-ttu-id="a18e0-102">Im Gegensatz zur Erstellung, Antwort und Zusammenfassung Ansichten, die html sind, sind Chat Ansichten systemeigenen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="a18e0-102">Unlike the creation, response and summary views that are html, chat views are native views.</span></span> <span data-ttu-id="a18e0-103">Informationen zum Anpassen der Kartenansicht Chat, müssen Sie ein Json das Kartenlayout als auch die Werte in der Ansicht bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a18e0-103">To customize the chat card view, you will need to provide a json of the card layout as well as the values in the view.</span></span> <span data-ttu-id="a18e0-104">Ohne eine angepasste Chat Leinen Kartenansicht, der Standardwert Chat Kartenansicht mit dem Text der app-Titel.</span><span class="sxs-lookup"><span data-stu-id="a18e0-104">In the absence of a customized chat canvas card view, the default would be chat card view with the text of app title.</span></span> 

## <a name="views-and-their-supported-properties"></a><span data-ttu-id="a18e0-105">Ansichten und deren unterstützten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a18e0-105">Views and their supported properties</span></span>
<span data-ttu-id="a18e0-106">Im folgenden sind verschiedene Arten von sub-views/Widgets zusammen mit ihren anpassbaren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a18e0-106">Below are different types of sub-views/widgets along with their customizable properties.</span></span> <span data-ttu-id="a18e0-107">Einige Eigenschaften sind mit <sup>iOS</sup> zurück, der angibt, dass sie nur auf iOS _(und hat keine Auswirkung auf Android)_ anwendbar sind gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a18e0-107">Few properties are marked with <sup>iOS</sup>  indicating that they are applicable only on iOS _(and will have no effect on android)_.</span></span>

### <a name="container--view"></a><span data-ttu-id="a18e0-108">Container / anzeigen</span><span class="sxs-lookup"><span data-stu-id="a18e0-108">Container / View</span></span>

<ol>
<li><span data-ttu-id="a18e0-109">ID (optional, jedoch muss eindeutig sein)</span><span class="sxs-lookup"><span data-stu-id="a18e0-109">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="a18e0-110">sichtbar<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="a18e0-110">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="a18e0-111">Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-111">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="a18e0-112">Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-112">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="a18e0-113">Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-113">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="a18e0-114">width</span><span class="sxs-lookup"><span data-stu-id="a18e0-114">width</span></span></li>
<li><span data-ttu-id="a18e0-115">height</span><span class="sxs-lookup"><span data-stu-id="a18e0-115">height</span></span></li>
<li><span data-ttu-id="a18e0-116">Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-116">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="a18e0-117">BackgroundColor _(nur hex Code hier zulässig)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-117">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="a18e0-118">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="a18e0-118">cornerRadius</span></span></li>
<li><span data-ttu-id="a18e0-119">BorderWidthiOS / BorderColoriOS</span><span class="sxs-lookup"><span data-stu-id="a18e0-119">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="a18e0-120">untergeordnete Elemente _(Array von untergeordneten Ansichten)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-120">children _(array of sub-views)_</span></span></li>
<li><span data-ttu-id="a18e0-121">Layout _(vertikale / horizontale When nicht angegeben, wird standardmäßig auf vertikal)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-121">layout _(vertical / horizontal � when unspecified, defaults to vertical)_</span></span></li>
<li><span data-ttu-id="a18e0-122">VerticalAlignment _(oben / unten / zentriert / StretchiOS - wie untergeordnete Elemente vertikal ausgerichtet werden)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-122">verticalAlignment _(top / bottom / center / stretchiOS - how children will be aligned vertically)_</span></span></li>
<li><span data-ttu-id="a18e0-123">HorizontalAlignment _ (von links/rechts/zentriert/SpaceBetween<sup></sup> iOS/SpaceAround<sup>iOS</sup>) – wie untergeordnete Elemente horizontal ausgerichtet werden. _</span><span class="sxs-lookup"><span data-stu-id="a18e0-123">horizontalAlignment _(left / right / center / spaceBetween<sup>iOS</sup> / spaceAround<sup>iOS</sup>) - how children will be aligned horizontally._</span></span></li>
<li><span data-ttu-id="a18e0-124">InitialHeight<sup>iOS</sup> _eine einzige iOS-Eigenschaft verwendet, in der obersten Container, mit dem die Karte rendern, damit die genaue Dimension worden ist. Es wird dringend empfohlen, diese Eigenschaft für einen reibungsloseren verwenden!_</span><span class="sxs-lookup"><span data-stu-id="a18e0-124">initialHeight<sup>iOS</sup> � _an iOS only property used in the topmost container that is used to render the card before the accurate dimension is ascertained. It is strongly advised to use this property for a smoother experience!_</span></span></li>
</ol>

### <a name="text"></a><span data-ttu-id="a18e0-125">Text</span><span class="sxs-lookup"><span data-stu-id="a18e0-125">Text</span></span>

<ol>
<li><span data-ttu-id="a18e0-126">ID (optional, jedoch muss eindeutig sein)</span><span class="sxs-lookup"><span data-stu-id="a18e0-126">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="a18e0-127">sichtbar<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="a18e0-127">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="a18e0-128">Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-128">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="a18e0-129">Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-129">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="a18e0-130">Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-130">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="a18e0-131">width</span><span class="sxs-lookup"><span data-stu-id="a18e0-131">width</span></span></li>
<li><span data-ttu-id="a18e0-132">height</span><span class="sxs-lookup"><span data-stu-id="a18e0-132">height</span></span></li>
<li><span data-ttu-id="a18e0-133">Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-133">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="a18e0-134">BackgroundColor _(nur hex Code hier zulässig)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-134">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="a18e0-135">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="a18e0-135">cornerRadius</span></span></li>
<li><span data-ttu-id="a18e0-136">BorderWidthiOS / BorderColoriOS</span><span class="sxs-lookup"><span data-stu-id="a18e0-136">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="a18e0-137">string</span><span class="sxs-lookup"><span data-stu-id="a18e0-137">string</span></span></li>
<li><span data-ttu-id="a18e0-138">FontSize _(Schriftartfamilie ist immer des Systems Standard, um Probleme beim Rendern zu vermeiden)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-138">fontSize _(font family is always System's default, to avoid rendering issues)_</span></span></li>
<li><span data-ttu-id="a18e0-139">TextColor _(nur hex Code hier zulässig)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-139">textColor _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="a18e0-140">EllipsizeMode _(Head / mittlere / Endezeigern)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-140">ellipsizeMode _(head / middle / tail)_</span></span></li>
<li><span data-ttu-id="a18e0-141">MaxNumberOfLines _(0 für keine Begrenzung, sonst noch Text werden gemäß den Anweisungen in EllipsizeMode abgeschnitten)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-141">maxNumberOfLines _(0 for no limit, else text will be truncated as per ellipsizeMode)_</span></span></li>
</ol>


### <a name="image"></a><span data-ttu-id="a18e0-142">Image</span><span class="sxs-lookup"><span data-stu-id="a18e0-142">Image</span></span>

<ol>
<li><span data-ttu-id="a18e0-143">ID (optional, jedoch muss eindeutig sein)</span><span class="sxs-lookup"><span data-stu-id="a18e0-143">id (optional, but must be unique)</span></span></li>
<li><span data-ttu-id="a18e0-144">sichtbar<sup>iOS</sup></span><span class="sxs-lookup"><span data-stu-id="a18e0-144">visible<sup>iOS</sup></span></span></li>
<li><span data-ttu-id="a18e0-145">Geben Sie _(beliebige der untergeordneten Ansichtstypen, den, die wir hier Erwähnung sind)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-145">type _(any of the sub-view types we are mentioning here)_</span></span></li>
<li><span data-ttu-id="a18e0-146">Rand / MarginTop / MarginRight / MarginBottom / MarginLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-146">margin / marginTop / marginRight / marginBottom / marginLeft</span></span></li>
<li><span data-ttu-id="a18e0-147">Abstand / PaddingTop / PaddingRight / PaddingBottom / PaddingLeft</span><span class="sxs-lookup"><span data-stu-id="a18e0-147">padding / paddingTop / paddingRight / paddingBottom / paddingLeft</span></span></li>
<li><span data-ttu-id="a18e0-148">width</span><span class="sxs-lookup"><span data-stu-id="a18e0-148">width</span></span></li>
<li><span data-ttu-id="a18e0-149">height</span><span class="sxs-lookup"><span data-stu-id="a18e0-149">height</span></span></li>
<li><span data-ttu-id="a18e0-150">Weight _(% Anteil der Ansicht Breite/Höhe im Fall eines WAN-Layouts Horizontal/vertikal jeweils parent)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-150">weight _(%ratio of parent view's width/height in case of horizontal/vertical layouts respectively)_</span></span></li>
<li><span data-ttu-id="a18e0-151">BackgroundColor _(nur hex Code hier zulässig)_</span><span class="sxs-lookup"><span data-stu-id="a18e0-151">backgroundColor  _(only hex code allowed here)_</span></span></li>
<li><span data-ttu-id="a18e0-152">cornerRadius</span><span class="sxs-lookup"><span data-stu-id="a18e0-152">cornerRadius</span></span></li>
<li><span data-ttu-id="a18e0-153">BorderWidthiOS / BorderColoriOS</span><span class="sxs-lookup"><span data-stu-id="a18e0-153">borderWidthiOS / borderColoriOS</span></span></li>
<li><span data-ttu-id="a18e0-154">source</span><span class="sxs-lookup"><span data-stu-id="a18e0-154">source</span></span></li>
<li><span data-ttu-id="a18e0-155">ContentMode _ (AspectFit/AspectFill/Dehnen/wiederholen Sie die<sup>iOS</sup>) _</span><span class="sxs-lookup"><span data-stu-id="a18e0-155">contentMode _(aspectFit / aspectFill / stretch / repeat<sup>iOS</sup>)_</span></span></li>
</ol>



## <a name="binding-data-with-views"></a><span data-ttu-id="a18e0-156">Binden von Daten mit Ansichten</span><span class="sxs-lookup"><span data-stu-id="a18e0-156">Binding data with views</span></span>
* <span data-ttu-id="a18e0-157">__Form__</span><span class="sxs-lookup"><span data-stu-id="a18e0-157">__Form__</span></span>
  * <span data-ttu-id="a18e0-158">$\{Form.Title}</span><span class="sxs-lookup"><span data-stu-id="a18e0-158">$\{Form.title}</span></span>
  * <span data-ttu-id="a18e0-159">$\{Form.Expiry} - _Ausgabe ist eine Datum-Uhrzeit-Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="a18e0-159">$\{Form.expiry} - _output is a date-time string_</span></span>
  * <span data-ttu-id="a18e0-160">$\{Form.Questions}</span><span class="sxs-lookup"><span data-stu-id="a18e0-160">$\{Form.questions}</span></span>
  * <span data-ttu-id="a18e0-161">$\{Form.Questions.Length}</span><span class="sxs-lookup"><span data-stu-id="a18e0-161">$\{Form.questions.length}</span></span>
  * <span data-ttu-id="a18e0-162">$\{Form.Questions[questionId].Title}</span><span class="sxs-lookup"><span data-stu-id="a18e0-162">$\{Form.questions[questionId].title}</span></span>
  * <span data-ttu-id="a18e0-163">$\{Form.Questions[questionId].Options}</span><span class="sxs-lookup"><span data-stu-id="a18e0-163">$\{Form.questions[questionId].options}</span></span>
  * <span data-ttu-id="a18e0-164">$\{Form.Questions[questionId].Options.Length}</span><span class="sxs-lookup"><span data-stu-id="a18e0-164">$\{Form.questions[questionId].options.length}</span></span>
  * <span data-ttu-id="a18e0-165">$\{Form.Questions[questionId].Options[optionId].Text}</span><span class="sxs-lookup"><span data-stu-id="a18e0-165">$\{Form.questions[questionId].options[optionId].text}</span></span>
  * <span data-ttu-id="a18e0-166">$\{Form.Questions[questionId].Options[optionId].pictureUrl}</span><span class="sxs-lookup"><span data-stu-id="a18e0-166">$\{Form.questions[questionId].options[optionId].pictureUrl}</span></span>
  * <span data-ttu-id="a18e0-167">$\{Form.Properties}</span><span class="sxs-lookup"><span data-stu-id="a18e0-167">$\{Form.properties}</span></span>
  * <span data-ttu-id="a18e0-168">$\{Form.Properties.Length}</span><span class="sxs-lookup"><span data-stu-id="a18e0-168">$\{Form.properties.length}</span></span>
  * <span data-ttu-id="a18e0-169">$\{Form.Properties[PropertyName]}</span><span class="sxs-lookup"><span data-stu-id="a18e0-169">$\{Form.properties[propertyName]}</span></span>
  * <span data-ttu-id="a18e0-170">$\{Form.Properties[PropertyName].Value}</span><span class="sxs-lookup"><span data-stu-id="a18e0-170">$\{Form.properties[propertyName].value}</span></span>
  * <span data-ttu-id="a18e0-171">$\{Form.Properties[PropertyName].length} - _für Array/Set Type-Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="a18e0-171">$\{Form.properties[propertyName].length} - _for Array/Set type property_</span></span>
* <span data-ttu-id="a18e0-172">__MyLatestResponse__</span><span class="sxs-lookup"><span data-stu-id="a18e0-172">__MyLatestResponse__</span></span>
  * <span data-ttu-id="a18e0-173">$\{MyLatestResponse.sendTime} - _Ausgabe ist eine Datum-Uhrzeit-Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="a18e0-173">$\{MyLatestResponse.sendTime} - _output is a date-time string_</span></span>
  * <span data-ttu-id="a18e0-174">$\{MyLatestResponse.questionToAnswerMap[questionId]}</span><span class="sxs-lookup"><span data-stu-id="a18e0-174">$\{MyLatestResponse.questionToAnswerMap[questionId]}</span></span>
* <span data-ttu-id="a18e0-175">__Zusammenfassung__</span><span class="sxs-lookup"><span data-stu-id="a18e0-175">__Summary__</span></span>
  * <span data-ttu-id="a18e0-176">$\{Summary.totalResponseCount}</span><span class="sxs-lookup"><span data-stu-id="a18e0-176">$\{Summary.totalResponseCount}</span></span>
  * <span data-ttu-id="a18e0-177">$\{Summary.totalParticipantsCount}</span><span class="sxs-lookup"><span data-stu-id="a18e0-177">$\{Summary.totalParticipantsCount}</span></span>
  * <span data-ttu-id="a18e0-178">$\{Summary.targetResponderCount}</span><span class="sxs-lookup"><span data-stu-id="a18e0-178">$\{Summary.targetResponderCount}</span></span>

<span data-ttu-id="a18e0-179">Außerdem können eine diese Variablen als Platzhalter, wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="a18e0-179">Also one can use these variables as placeholders, like:</span></span>  
<span data-ttu-id="a18e0-180">_"Vielen Dank für Ihre News-Bericht: ${Form.properties[newsDescription].value}"_</span><span class="sxs-lookup"><span data-stu-id="a18e0-180">_"Thanks for your news report: ${Form.properties[newsDescription].value}"_</span></span>

## <a name="operations"></a><span data-ttu-id="a18e0-181">Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a18e0-181">Operations</span></span>

<span data-ttu-id="a18e0-182">In einigen Szenarien auftreten gibt es muss, in denen möglicherweise unterschiedliche Benutzer müssen verschiedene Chat-Karte anzeigen, die basiert auf einige Attribute.</span><span class="sxs-lookup"><span data-stu-id="a18e0-182">In some scenarios, there may arise a need where different users may need to view different chat card, that may be based on some attributes.</span></span> <span data-ttu-id="a18e0-183">Um diese Szenarien zu ermöglichen, bietet Kaizala [Operatoren](Operator.md), mit dem Ersteller der Aktion auf Chat Kartenansichten für die gleiche Aktionsinstanz unterschiedlich für verschiedene Szenarien/Benutzer personalisieren können.</span><span class="sxs-lookup"><span data-stu-id="a18e0-183">In order to enable such scenarios, Kaizala provides [operators](Operator.md), that enables Action Creators to personalise chat card views for the same Action instance differently for different scenarios/users.</span></span>

<span data-ttu-id="a18e0-184">Sie können beispielsweise Anzeigen einer anderen Kartenansicht für Benutzer, die nicht den Auftrag abgeschlossen haben, und eine andere Kartenansicht für Benutzer, die den Auftrag abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="a18e0-184">For example, you may choose to show a different card view for users who have not completed the job, and a different card view for users who have completed the job.</span></span> <span data-ttu-id="a18e0-185">Dies kann für jede Art von Szenarien erweitert werden, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="a18e0-185">This can be extended to any type of scenarios that may arise.</span></span>

## <a name="how-to-provide-the-json-schema"></a><span data-ttu-id="a18e0-186">Zum Bereitstellen des Json-Schemas</span><span class="sxs-lookup"><span data-stu-id="a18e0-186">How to provide the json schema</span></span>
<span data-ttu-id="a18e0-187">In der Datei manifest _(package.json)_ eines Pakets, platzieren Sie den Namen der JSON **SourceLocation** ist Schlüssel in **ChatCanvasCardView** unten einen Beispielsnapshot package.json:</span><span class="sxs-lookup"><span data-stu-id="a18e0-187">In the manifest _(package.json)_ file of a package put the JSON file name under **sourceLocation** key in **ChatCanvasCardView** Below is a sample snapshot from package.json:</span></span>

![Momentaufnahme der package.json](./chatcardviewjson.png)

## <a name="example-chatcanvascardview-source-file"></a><span data-ttu-id="a18e0-189">Beispiel ChatCanvasCardView-Quelldatei</span><span class="sxs-lookup"><span data-stu-id="a18e0-189">Example ChatCanvasCardView source file</span></span>
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
