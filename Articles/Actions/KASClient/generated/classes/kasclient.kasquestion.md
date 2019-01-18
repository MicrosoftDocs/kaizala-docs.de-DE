---
ms.openlocfilehash: cd7a7880b45a68ea4ac977487756c754a2291dd4
ms.sourcegitcommit: 1482683c0fde70600ce3b2948cbba8856935d91e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28728074"
---
<span data-ttu-id="5caca-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="5caca-101">[](../README.md) > [KASClient](../modules/kasclient.md) > [KASQuestion](../classes/kasclient.kasquestion.md)</span></span>

# <a name="class-kasquestion"></a><span data-ttu-id="5caca-102">Klasse: KASQuestion</span><span class="sxs-lookup"><span data-stu-id="5caca-102">Class: KASQuestion</span></span>

## <a name="hierarchy"></a><span data-ttu-id="5caca-103">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="5caca-103">Hierarchy</span></span>

<span data-ttu-id="5caca-104">**KASQuestion**</span><span class="sxs-lookup"><span data-stu-id="5caca-104">**KASQuestion**</span></span>

## <a name="index"></a><span data-ttu-id="5caca-105">Index </span><span class="sxs-lookup"><span data-stu-id="5caca-105">Index</span></span>

### <a name="properties"></a><span data-ttu-id="5caca-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5caca-106">Properties</span></span>

* [<span data-ttu-id="5caca-107">config</span><span class="sxs-lookup"><span data-stu-id="5caca-107">config</span></span>](kasclient.kasquestion.md#config)
* [<span data-ttu-id="5caca-108">displayType</span><span class="sxs-lookup"><span data-stu-id="5caca-108">displayType</span></span>](kasclient.kasquestion.md#displaytype)
* [<span data-ttu-id="5caca-109">id</span><span class="sxs-lookup"><span data-stu-id="5caca-109">id</span></span>](kasclient.kasquestion.md#id)
* [<span data-ttu-id="5caca-110">isEditable</span><span class="sxs-lookup"><span data-stu-id="5caca-110">isEditable</span></span>](kasclient.kasquestion.md#iseditable)
* [<span data-ttu-id="5caca-111">isExcludedFromReporting</span><span class="sxs-lookup"><span data-stu-id="5caca-111">isExcludedFromReporting</span></span>](kasclient.kasquestion.md#isexcludedfromreporting)
* [<span data-ttu-id="5caca-112">isInvisible</span><span class="sxs-lookup"><span data-stu-id="5caca-112">isInvisible</span></span>](kasclient.kasquestion.md#isinvisible)
* [<span data-ttu-id="5caca-113">isResponseOptional</span><span class="sxs-lookup"><span data-stu-id="5caca-113">isResponseOptional</span></span>](kasclient.kasquestion.md#isresponseoptional)
* [<span data-ttu-id="5caca-114">options</span><span class="sxs-lookup"><span data-stu-id="5caca-114">options</span></span>](kasclient.kasquestion.md#options)
* [<span data-ttu-id="5caca-115">title</span><span class="sxs-lookup"><span data-stu-id="5caca-115">title</span></span>](kasclient.kasquestion.md#title)
* [<span data-ttu-id="5caca-116">type</span><span class="sxs-lookup"><span data-stu-id="5caca-116">type</span></span>](kasclient.kasquestion.md#type)
* [<span data-ttu-id="5caca-117">valif</span><span class="sxs-lookup"><span data-stu-id="5caca-117">valif</span></span>](kasclient.kasquestion.md#valif)
* [<span data-ttu-id="5caca-118">visif</span><span class="sxs-lookup"><span data-stu-id="5caca-118">visif</span></span>](kasclient.kasquestion.md#visif)
### <a name="methods"></a><span data-ttu-id="5caca-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="5caca-119">Methods</span></span>

* [<span data-ttu-id="5caca-120">getAPICompatibleQuestionType</span><span class="sxs-lookup"><span data-stu-id="5caca-120">getAPICompatibleQuestionType</span></span>](kasclient.kasquestion.md#getapicompatiblequestiontype)
* [<span data-ttu-id="5caca-121">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-121">toAPICompatibleJSON</span></span>](kasclient.kasquestion.md#toapicompatiblejson)
* [<span data-ttu-id="5caca-122">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-122">toClientJSON</span></span>](kasclient.kasquestion.md#toclientjson)
* [<span data-ttu-id="5caca-123">toJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-123">toJSON</span></span>](kasclient.kasquestion.md#tojson)
* [<span data-ttu-id="5caca-124">validateResponse</span><span class="sxs-lookup"><span data-stu-id="5caca-124">validateResponse</span></span>](kasclient.kasquestion.md#validateresponse)
* [<span data-ttu-id="5caca-125">fromJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-125">fromJSON</span></span>](kasclient.kasquestion.md#fromjson)

---

## <a name="properties"></a><span data-ttu-id="5caca-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5caca-126">Properties</span></span>

<a id="config"></a>

###  <a name="config"></a><span data-ttu-id="5caca-127">config</span><span class="sxs-lookup"><span data-stu-id="5caca-127">config</span></span>

<span data-ttu-id="5caca-128">**● Config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* = Null</span><span class="sxs-lookup"><span data-stu-id="5caca-128">**● config**: *[KASQuestionConfig](kasclient.kasquestionconfig.md)* =  null</span></span>

<span data-ttu-id="5caca-129">Konfiguration/Verhalten einer Frage</span><span class="sxs-lookup"><span data-stu-id="5caca-129">Configuration/behaviour of a question</span></span>

___

<a id="displaytype"></a>

###  <a name="displaytype"></a><span data-ttu-id="5caca-130">displayType</span><span class="sxs-lookup"><span data-stu-id="5caca-130">displayType</span></span>

<span data-ttu-id="5caca-131">**● DisplayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* = KASQuestionDisplayType.None</span><span class="sxs-lookup"><span data-stu-id="5caca-131">**● displayType**: *[KASQuestionDisplayType](../enums/kasclient.kasquestiondisplaytype.md)* =  KASQuestionDisplayType.None</span></span>

<span data-ttu-id="5caca-132">Typ der Optionen für die Frage anzeigen</span><span class="sxs-lookup"><span data-stu-id="5caca-132">Display type of the question's options</span></span>

___

<a id="id"></a>

###  <a name="id"></a><span data-ttu-id="5caca-133">id</span><span class="sxs-lookup"><span data-stu-id="5caca-133">id</span></span>

<span data-ttu-id="5caca-134">**●-Id**: *`number`* = 0</span><span class="sxs-lookup"><span data-stu-id="5caca-134">**● id**: *`number`* = 0</span></span>

<span data-ttu-id="5caca-135">Index der Frage, beginnt mit 0</span><span class="sxs-lookup"><span data-stu-id="5caca-135">Index of the question, starts with 0</span></span>

___

<a id="iseditable"></a>

###  <a name="iseditable"></a><span data-ttu-id="5caca-136">isEditable</span><span class="sxs-lookup"><span data-stu-id="5caca-136">isEditable</span></span>

<span data-ttu-id="5caca-137">**● IsEditable**: *`boolean`* = True</span><span class="sxs-lookup"><span data-stu-id="5caca-137">**● isEditable**: *`boolean`* = true</span></span>

<span data-ttu-id="5caca-138">Kennzeichnet der Standardwert ist true, wenn die Frage vom Responder bearbeitet werden kann,</span><span class="sxs-lookup"><span data-stu-id="5caca-138">Denotes if the question can be edited by the responder, default is true</span></span>

___

<a id="isexcludedfromreporting"></a>

###  <a name="isexcludedfromreporting"></a><span data-ttu-id="5caca-139">isExcludedFromReporting</span><span class="sxs-lookup"><span data-stu-id="5caca-139">isExcludedFromReporting</span></span>

<span data-ttu-id="5caca-140">**● IsExcludedFromReporting**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="5caca-140">**● isExcludedFromReporting**: *`boolean`* = false</span></span>

<span data-ttu-id="5caca-141">Gibt an, ob die Frage aus allen möglichen reporting übersprungen werden</span><span class="sxs-lookup"><span data-stu-id="5caca-141">Denotes if the question will be skipped from all sorts of reporting</span></span>

___

<a id="isinvisible"></a>

###  <a name="isinvisible"></a><span data-ttu-id="5caca-142">isInvisible</span><span class="sxs-lookup"><span data-stu-id="5caca-142">isInvisible</span></span>

<span data-ttu-id="5caca-143">**● IsInvisible**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="5caca-143">**● isInvisible**: *`boolean`* = false</span></span>

<span data-ttu-id="5caca-144">Gibt an, wenn die Frage für den-Responder nicht sichtbar sein soll, standardmäßig false ist</span><span class="sxs-lookup"><span data-stu-id="5caca-144">Denotes if the question should be invisible to the responder, default is false</span></span>

___

<a id="isresponseoptional"></a>

###  <a name="isresponseoptional"></a><span data-ttu-id="5caca-145">isResponseOptional</span><span class="sxs-lookup"><span data-stu-id="5caca-145">isResponseOptional</span></span>

<span data-ttu-id="5caca-146">**● IsResponseOptional**: *`boolean`* = False</span><span class="sxs-lookup"><span data-stu-id="5caca-146">**● isResponseOptional**: *`boolean`* = false</span></span>

<span data-ttu-id="5caca-147">Gibt an, ob es obligatorisch ist, diese Frage zu beantworten</span><span class="sxs-lookup"><span data-stu-id="5caca-147">Denotes if it's mandatory to respond to this question</span></span>

___

<a id="options"></a>

###  <a name="options"></a><span data-ttu-id="5caca-148">options</span><span class="sxs-lookup"><span data-stu-id="5caca-148">options</span></span>

<span data-ttu-id="5caca-149">**● Optionen**: \* [KASQuestionOption](kasclient.kasquestionoption.md)[]\* =]</span><span class="sxs-lookup"><span data-stu-id="5caca-149">**● options**: *[KASQuestionOption](kasclient.kasquestionoption.md)[]* =  []</span></span>

<span data-ttu-id="5caca-150">Liste der Optionen für die Frage</span><span class="sxs-lookup"><span data-stu-id="5caca-150">List of options for the question</span></span>

___

<a id="title"></a>

###  <a name="title"></a><span data-ttu-id="5caca-151">title</span><span class="sxs-lookup"><span data-stu-id="5caca-151">title</span></span>

<span data-ttu-id="5caca-152">**● Titel**: *`string`* = ""</span><span class="sxs-lookup"><span data-stu-id="5caca-152">**● title**: *`string`* = ""</span></span>

<span data-ttu-id="5caca-153">Titel der Frage</span><span class="sxs-lookup"><span data-stu-id="5caca-153">Title of the question</span></span>

___

<a id="type"></a>

###  <a name="type"></a><span data-ttu-id="5caca-154">type</span><span class="sxs-lookup"><span data-stu-id="5caca-154">type</span></span>

<span data-ttu-id="5caca-155">**● Typ**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* = KASQuestionType.None</span><span class="sxs-lookup"><span data-stu-id="5caca-155">**● type**: *[KASQuestionType](../enums/kasclient.kasquestiontype.md)* =  KASQuestionType.None</span></span>

<span data-ttu-id="5caca-156">Typ der Frage</span><span class="sxs-lookup"><span data-stu-id="5caca-156">Type of the question</span></span>

___

<a id="valif"></a>

###  <a name="valif"></a><span data-ttu-id="5caca-157">valif</span><span class="sxs-lookup"><span data-stu-id="5caca-157">valif</span></span>

<span data-ttu-id="5caca-158">**● Valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* = Null</span><span class="sxs-lookup"><span data-stu-id="5caca-158">**● valif**: *[KASValidationRule](kasclient.kasvalidationrule.md)* =  null</span></span>

<span data-ttu-id="5caca-159">Eine Frage - JSON von Regeln, Fehlerzeichenfolge und Hilfezeichenfolge Validierungsregeln</span><span class="sxs-lookup"><span data-stu-id="5caca-159">Validation rules of a question - JSON of rule(s), error string and help string</span></span>

___

<a id="visif"></a>

###  <a name="visif"></a><span data-ttu-id="5caca-160">visif</span><span class="sxs-lookup"><span data-stu-id="5caca-160">visif</span></span>

<span data-ttu-id="5caca-161">**● Visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* = Null</span><span class="sxs-lookup"><span data-stu-id="5caca-161">**● visif**: *[KASVisibilityRule](kasclient.kasvisibilityrule.md)* =  null</span></span>

<span data-ttu-id="5caca-162">Regeln für die Sichtbarkeit der eine Frage - Regelzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5caca-162">Visibility rules of a question - rule string</span></span>

___

## <a name="methods"></a><span data-ttu-id="5caca-163">Methoden</span><span class="sxs-lookup"><span data-stu-id="5caca-163">Methods</span></span>

<a id="getapicompatiblequestiontype"></a>

###  <a name="getapicompatiblequestiontype"></a><span data-ttu-id="5caca-164">getAPICompatibleQuestionType</span><span class="sxs-lookup"><span data-stu-id="5caca-164">getAPICompatibleQuestionType</span></span>

<span data-ttu-id="5caca-165">▸ **GetAPICompatibleQuestionType**(Typ: *`string`*):`string`</span><span class="sxs-lookup"><span data-stu-id="5caca-165">▸ **getAPICompatibleQuestionType**(type: *`string`*): `string`</span></span>

<span data-ttu-id="5caca-166">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="5caca-166">**Parameters:**</span></span>

| <span data-ttu-id="5caca-167">Name</span><span class="sxs-lookup"><span data-stu-id="5caca-167">Name</span></span> | <span data-ttu-id="5caca-168">Typ</span><span class="sxs-lookup"><span data-stu-id="5caca-168">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="5caca-169">Typ</span><span class="sxs-lookup"><span data-stu-id="5caca-169">type</span></span> | `string` |

<span data-ttu-id="5caca-170">**Gibt:**`string`</span><span class="sxs-lookup"><span data-stu-id="5caca-170">**Returns:** `string`</span></span>

___

<a id="toapicompatiblejson"></a>

###  <a name="toapicompatiblejson"></a><span data-ttu-id="5caca-171">toAPICompatibleJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-171">toAPICompatibleJSON</span></span>

<span data-ttu-id="5caca-172">▸ **ToAPICompatibleJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-172">▸ **toAPICompatibleJSON**(): `JSON`</span></span>

<span data-ttu-id="5caca-173">**Gibt:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-173">**Returns:** `JSON`</span></span>

___

<a id="toclientjson"></a>

###  <a name="toclientjson"></a><span data-ttu-id="5caca-174">toClientJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-174">toClientJSON</span></span>

<span data-ttu-id="5caca-175">▸ **ToClientJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-175">▸ **toClientJSON**(): `JSON`</span></span>

<span data-ttu-id="5caca-176">**Gibt:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-176">**Returns:** `JSON`</span></span>

___

<a id="tojson"></a>

###  <a name="tojson"></a><span data-ttu-id="5caca-177">toJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-177">toJSON</span></span>

<span data-ttu-id="5caca-178">▸ **ToJSON**():`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-178">▸ **toJSON**(): `JSON`</span></span>

<span data-ttu-id="5caca-179">**Gibt:**`JSON`</span><span class="sxs-lookup"><span data-stu-id="5caca-179">**Returns:** `JSON`</span></span>

___

<a id="validateresponse"></a>

###  <a name="validateresponse"></a><span data-ttu-id="5caca-180">validateResponse</span><span class="sxs-lookup"><span data-stu-id="5caca-180">validateResponse</span></span>

<span data-ttu-id="5caca-181">▸ **ValidateResponse**(Antwort: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span><span class="sxs-lookup"><span data-stu-id="5caca-181">▸ **validateResponse**(response: *`string`*): [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span></span>

<span data-ttu-id="5caca-182">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="5caca-182">**Parameters:**</span></span>

| <span data-ttu-id="5caca-183">Name</span><span class="sxs-lookup"><span data-stu-id="5caca-183">Name</span></span> | <span data-ttu-id="5caca-184">Typ</span><span class="sxs-lookup"><span data-stu-id="5caca-184">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="5caca-185">Antwort</span><span class="sxs-lookup"><span data-stu-id="5caca-185">response</span></span> | `string` |

<span data-ttu-id="5caca-186">**Gibt:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span><span class="sxs-lookup"><span data-stu-id="5caca-186">**Returns:** [KASQuestionValidationResponse](kasclient.kasquestionvalidationresponse.md)</span></span>

___

<a id="fromjson"></a>

### <a name="static-fromjson"></a><span data-ttu-id="5caca-187">`<Static>`fromJSON</span><span class="sxs-lookup"><span data-stu-id="5caca-187">`<Static>` fromJSON</span></span>

<span data-ttu-id="5caca-188">▸ **FromJSON**(Objekt: *`any`*): [KASQuestion](kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="5caca-188">▸ **fromJSON**(object: *`any`*): [KASQuestion](kasclient.kasquestion.md)</span></span>

<span data-ttu-id="5caca-189">**Parameter:**</span><span class="sxs-lookup"><span data-stu-id="5caca-189">**Parameters:**</span></span>

| <span data-ttu-id="5caca-190">Name</span><span class="sxs-lookup"><span data-stu-id="5caca-190">Name</span></span> | <span data-ttu-id="5caca-191">Typ</span><span class="sxs-lookup"><span data-stu-id="5caca-191">Type</span></span> |
| ------ | ------ |
| <span data-ttu-id="5caca-192">object</span><span class="sxs-lookup"><span data-stu-id="5caca-192">object</span></span> | `any` |

<span data-ttu-id="5caca-193">**Gibt:** [KASQuestion](kasclient.kasquestion.md)</span><span class="sxs-lookup"><span data-stu-id="5caca-193">**Returns:** [KASQuestion](kasclient.kasquestion.md)</span></span>

___

