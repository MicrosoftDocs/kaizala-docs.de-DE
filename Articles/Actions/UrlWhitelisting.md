# <a name="load-external-urls-within-your-action"></a>Laden von externen Urls in Ihre Aktion

Kaizala ermöglicht Entwicklern die Aktion zum Laden von Https-Urls innerhalb einer Aktion. In Szenarien, in dem Aktion Developer eine Webseite öffnen möchte, können sie "ExternalUrls" verwenden, um Webseiten in fesselnden Ansichten zu laden.
Um das Laden der Webseite innerhalb einer Aktion, weißen Aktion Developer muss die Urls zu aktivieren, und fügen sie in der Datei Package.json für die Aktion.

## <a name="whitelisting-external-url"></a>Externe URL mithilfe

In der Datei 'Package.json' für die Aktion
* Fügen Sie ein neues Tag **'ExternalUrls'** hinzu.
* Fügen Sie Liste der URLs sollen weißen in diesem Tag hinzu. Finden Sie den Teil der Beispielcode. 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* Jede Url muss eine gültige vollständige Url sein.
* Jede Url sollte eine Https-Url sein.

