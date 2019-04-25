# <a name="load-external-urls-within-your-action"></a><span data-ttu-id="2d6ec-101">Laden externer URLs innerhalb der Aktion</span><span class="sxs-lookup"><span data-stu-id="2d6ec-101">Load external urls within your Action</span></span>

<span data-ttu-id="2d6ec-102">Kaizala ermöglicht es Aktions Entwicklern, HTTPS-URLs innerhalb einer Aktion zu laden.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-102">Kaizala enables Action developers to load https urls within an Action.</span></span> <span data-ttu-id="2d6ec-103">In Szenarien, in denen Action Developer eine Webseite öffnen möchte, können Sie "externalUrls" verwenden, um Webseiten in immersiven Ansichten zu laden.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-103">In scenarios, where Action developer wants to open a webpage, they can use ‘externalUrls’ to load webpages within immersive views.</span></span>
<span data-ttu-id="2d6ec-104">Um das Laden von Webseiten innerhalb einer Aktion zu ermöglichen, muss der Aktions Entwickler die URLs in der Liste Whitelist und Sie in der Datei Package. JSON für die Aktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-104">In order to enable loading of webpage within an Action, Action developer needs to whitelist the urls and add them in the Package.json file for the Action.</span></span>

## <a name="whitelisting-external-url"></a><span data-ttu-id="2d6ec-105">Whitelisting externe URL</span><span class="sxs-lookup"><span data-stu-id="2d6ec-105">Whitelisting external URL</span></span>

<span data-ttu-id="2d6ec-106">In der Datei "Package. JSON" für Ihre Aktion</span><span class="sxs-lookup"><span data-stu-id="2d6ec-106">In your ‘Package.json’ file for your Action</span></span>
* <span data-ttu-id="2d6ec-107">Hinzufügen eines neuen Tags **"externalUrls"**.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-107">Add a new tag **‘externalUrls’**.</span></span>
* <span data-ttu-id="2d6ec-108">Fügen Sie in diesem Tag eine Liste der URLs hinzu, die Sie in die Whitelist einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-108">Add list of URLs which you want to whitelist in this tag.</span></span> <span data-ttu-id="2d6ec-109">Den Teil des Beispielcodes finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-109">Please find the part of the sample code below.</span></span> 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* <span data-ttu-id="2d6ec-110">Jede URL sollte eine gültige vollständige URL sein.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-110">Each url should be a valid complete url.</span></span>
* <span data-ttu-id="2d6ec-111">Jede URL sollte eine HTTPS-URL sein.</span><span class="sxs-lookup"><span data-stu-id="2d6ec-111">Each url should be an https url.</span></span>

