# <a name="load-external-urls-within-your-action"></a>Laden externer URLs innerhalb der Aktion

Kaizala ermöglicht es Aktions Entwicklern, HTTPS-URLs innerhalb einer Aktion zu laden. In Szenarien, in denen Action Developer eine Webseite öffnen möchte, können Sie "externalUrls" verwenden, um Webseiten in immersiven Ansichten zu laden.
Um das Laden von Webseiten innerhalb einer Aktion zu ermöglichen, muss der Aktions Entwickler die URLs in der Liste Whitelist und Sie in der Datei Package. JSON für die Aktion hinzufügen.

## <a name="whitelisting-external-url"></a>Whitelisting externe URL

In der Datei "Package. JSON" für Ihre Aktion
* Hinzufügen eines neuen Tags **"externalUrls"**.
* Fügen Sie in diesem Tag eine Liste der URLs hinzu, die Sie in die Whitelist einfügen möchten. Den Teil des Beispielcodes finden Sie weiter unten. 
```
  "externalUrls": [
    { "url" : "https://www.example-url.com" },
    { "url" : "https://another-example-url.com" },
  ],
```
* Jede URL sollte eine gültige vollständige URL sein.
* Jede URL sollte eine HTTPS-URL sein.

