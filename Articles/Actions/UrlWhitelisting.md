# <a name="load-external-urls-within-your-action"></a><span data-ttu-id="f7811-101">Laden von externen Urls in Ihre Aktion</span><span class="sxs-lookup"><span data-stu-id="f7811-101">Load external urls within your Action</span></span>

<span data-ttu-id="f7811-102">Kaizala ermöglicht Entwicklern die Aktion zum Laden von Https-Urls innerhalb einer Aktion.</span><span class="sxs-lookup"><span data-stu-id="f7811-102">Kaizala enables Action developers to load https urls within an Action.</span></span> <span data-ttu-id="f7811-103">In Szenarien, in dem Aktion Developer eine Webseite öffnen möchte, können sie "ExternalUrls" verwenden, um Webseiten in fesselnden Ansichten zu laden.</span><span class="sxs-lookup"><span data-stu-id="f7811-103">In scenarios, where Action developer wants to open a webpage, they can use ‘externalUrls’ to load webpages within immersive views.</span></span>
<span data-ttu-id="f7811-104">Um das Laden der Webseite innerhalb einer Aktion, weißen Aktion Developer muss die Urls zu aktivieren, und fügen sie in der Datei Package.json für die Aktion.</span><span class="sxs-lookup"><span data-stu-id="f7811-104">In order to enable loading of webpage within an Action, Action developer needs to whitelist the urls and add them in the Package.json file for the Action.</span></span>

## <a name="whitelisting-external-url"></a><span data-ttu-id="f7811-105">Externe URL mithilfe</span><span class="sxs-lookup"><span data-stu-id="f7811-105">Whitelisting external URL</span></span>

<span data-ttu-id="f7811-106">In der Datei 'Package.json' für die Aktion</span><span class="sxs-lookup"><span data-stu-id="f7811-106">In your ‘Package.json’ file for your Action</span></span>
* <span data-ttu-id="f7811-107">Fügen Sie ein neues Tag **'ExternalUrls'** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7811-107">Add a new tag **‘externalUrls’**.</span></span>
* <span data-ttu-id="f7811-108">Fügen Sie Liste der URLs sollen weißen in diesem Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7811-108">Add list of URLs which you want to whitelist in this tag.</span></span> <span data-ttu-id="f7811-109">Finden Sie den Teil der Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="f7811-109">Please find the part of the sample code below.</span></span> 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* <span data-ttu-id="f7811-110">Jede Url muss eine gültige vollständige Url sein.</span><span class="sxs-lookup"><span data-stu-id="f7811-110">Each url should be a valid complete url.</span></span>
* <span data-ttu-id="f7811-111">Jede Url sollte eine Https-Url sein.</span><span class="sxs-lookup"><span data-stu-id="f7811-111">Each url should be an https url.</span></span>

