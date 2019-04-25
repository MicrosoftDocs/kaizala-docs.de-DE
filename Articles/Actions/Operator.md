# <a name="chat-card-customization---operators"></a>Anpassung der Chat Karte-Operatoren 

In einigen Szenarien kann es erforderlich sein, dass andere Benutzer möglicherweise andere Chat Karten anzeigen müssen, die möglicherweise auf einigen Attributen basieren. Um solche Szenarien zu aktivieren, stellt Kaizala Operatoren bereit, die es Aktions erStellern ermöglichen, Chat Kartenansichten für die gleiche Aktionsinstanz für verschiedene Szenarien/Benutzer unterschiedlich zu personalisieren.

## <a name="lets-take-an-example"></a>Nehmen wir ein Beispiel:

Angenommen, wir möchten die Kartenansicht anders als die Empfänger anzeigen. Unter Verwendung von Operatoren können wir dieses Szenario leicht erreichen, unten ist die benutzerdefinierte Chatansicht JSON für diese:  


```json

                  { 

                      "schemaVersion": 3, 

                      "schema": { 

                        "type": "container", 

                        "layout": "vertical", 

                        "children": [ 

                          { 

                            "type": "text", 

                            "string": "Title: ${Form.title}" 

                          }, 

                          { 

                            "type": "text", 

                            "string": "Who am I: ${Operators.custom_text}" 

                          } 

                        ] 

                      }, 

                      "Operators": { 

                        "custom_text": { 

                          "operator": "conditional_value", 

                          "condition": { 

                            "operator": "is_it_me", 

                            "value": { 

                              "operator": "property_value", 

                              "property": "creator", 

                              "src": "local" 

                            } 

                          }, 

                          "value": "Sender", 

                          "default": "Receiver" 

                        } 

                      } 

                  } 
```

Hier können Sie beobachten, dass der Operator "conditional_value" den booleschen Wert aus dem geschachtelten Operator "is_it_me" abgerufen, der weiter mit dem Operator "property_value" geschachtelt ist. Auf ähnliche Weise kann dies problemlos auf beliebige Szenarien ausgedehnt werden, sogar auf komplexe. Darüber hinaus muss der folgende Eintrag zum Paketmanifest hinzugefügt werden: ActionStoreSchema:<name of the action store schema definition file>"". Weitere Informationen finden Sie unter [JSON-Schema des Paketmanifests](package_manifest_schema.md) .


 
## <a name="list-of-supported-operators"></a>Liste der unterstützten Operatoren: 

> **Hinweis** : die Variablen x, y, z, die in den Syntax Beispielen verwendet werden, können einfache Werte oder Ergebnisse sein, die von geschachtelten Operatoren zurückgegeben werden. 


| Operator Name |Parametername |Parametertyp |Funktionalität  |Syntax |Minimierte Syntax | Hinweis |
|--------|------|------|----|----|----|----|
|Bedingter Wert  |1. Bedingung 2. Wert 3. Standard|1. boolescher Wert 2. JSON-Wert 3. JSON-Wert | Dieser Operator wird verwendet, um einen angegebenen Wert zurückzugeben, wenn eine definierte Bedingung true ist. Wenn die Bedingung false ist, wird false zurückgegeben.|{</br>"Operator": "conditional_value", "Condition": x, "Value": {y}, "Default": {z}</br>}| ["conditional_value", X, Y, Z] ||
|Gleich |1. Wert 2. Wert |    1. String 2. String |Dieser Operator gibt true zurück, wenn die bereitgestellten Werte (Wert1, Value2) gleich sind. Andernfalls wird false zurückgegeben. |    {</br>"Operator": "EQ", "Wert1": x, "Value2": y </br>} |["EQ", x, y] ||
|FormatProfileName  |1. Eigenschaft 2. Src |1. String 2. PropertyType| Ruft die Eigenschaft aus dem src-Eigenschaftswert ab und formatiert die Liste der userIds wie folgt:</br></br>"<Name von Benutzer 1> & n" </br></br>n ist die Anzahl der Benutzer, die in der Liste-1 vorhanden sind. |{</br>"Operator": "format_profile_names",</br>"Property": x, "src":P ropertyType</br>}|["format_profile_names", PropertyType, x] |PropertyType</br>{</br>  lokal, Server</br>} </br></br>1. dieser Operator übernimmt die Eigenschaft x provided gibt Array von userIds zurück. </br></br>2. Benutzername1 ist Sie, wenn der aktuelle angemeldete Benutzer in der Liste der userIds vorhanden ist.|
|FormatString|1. Format 2. Agrs|1. Zeichenfolge 2. Array von Argumenten, die von der Format Zeichenfolge erwartet werden|Dieser Operator ermöglicht es, eine Zeichenfolge mit Formatbezeichnern zu formatieren.</br></br>Dieser Operator ist identisch mit allen anderen Formatzeichenfolgen-Operatoren, die in cpp oder Java vorhanden sind. |{</br>"Operator": "FORMAT_STRING", "Format": x, "args": [y, z...]</br>}|["FORMAT_STRING", x, [y, z...]]|X kann Bezeichner wie% s,% d usw. enthalten, und die Operatoren erwarten, dass die Argumente vom gleichen Typ in derselben Reihenfolge vorhanden sind. </br></br>Beispielsweise kann die Zeichenfolge</br>{</br>"Operator": "FORMAT_STRING",</br>"Format": "Mein Name ist% s, und mein Alter ist% d",</br>"args": [y, z]</br>}</br></br>Wobei y eine Zeichenfolgenvariable und z eine ganze Zahl ist|
|IsCurrentUser|1. Wert|1. UUID vergleicht die bereitgestellte UUID (UserId) mit der UUID (UserId) des aktuellen angemeldeten Benutzers. Sie gibt true zurück, wenn Sie übereinstimmt, und gibt andernfalls false zurück. |{</br>"Operator": "is_it_me",</br>"Wert": x</br>}|["is_it_me" x]|
|JSONPathValue|1.1. Entity 2. Path|1. EntityType 2. gültiger JSON-Pfad| Ruft den Wert ab, der sich im Schlüssel in Entity JSON des angegebenen Typs befindet.  Es wird der erste Wert zurückgegeben, der im Pfad gefunden wird. |{</br>"Operator": "jsonpath_value",</br>"Entity": EntityType,</br>"Path": ValidJsonPath</br>}|["jsonpath_value", EntityType, ValidJsonPath]|{</br>"Operator":</br>"jsonpath_value",</br>"Entity": Nachricht,</br>"Path": "$.. Sendername</br>}</br></br>"$.." Rekursiv Traversieren</br></br>"$." Nur erste Ebene der Entität durchlaufen|
|MessageConversationName|1. Wert|1. messageId|Gibt den Unterhaltungs Namen zurück, zu dem die Nachricht mit der angegebenen messageId gehört.|{"Operator": "message_conversation_name", "Wert": x}|["message_conversation_name", x]|
|MessageCreationTime|1. Wert|1. messageId|Gibt die lesbare Timestamp-Zeichenfolge für den Erstellungszeitstempel der Nachricht mit der angegebenen messageId zurück. |{</br>"Operator": "message_creation_time",</br>"Wert": x</br>}|["message_creation_time", x]|
|ProfileName|1. ID|1. UUID|Gibt den Anzeigenamen des Benutzers zurück, wenn UUID (UserId) bereitgestellt wird. |{</br>"Operator": "profile_name", "ID": x</br>}|["profile_name", x]|
|PropertyValue|1. src 2. Property|1. PropertyType 2. String|Ruft die Eigenschaft aus dem src-PropertyType ab.|{</br>"Operator": "property_value",</br>"Property": x, "src": PropertyType</br>}|["property_value", PropertyType, x]|PropertyType</br></br>{</br>lokal, Server</br>}|
|AdditionOperation |1. arg1 | 1. Array von Argumenten erforderlich durch Additionsvorgang |Es werden alle Werte innerhalb der args ausgewertet und hinzugefügt. |{</br>"Operator": "Addition",</br>"args": [{</br>"Operator"..</br>}, 2, 4]</br>} |["Addition", [1, 2, 3]|Stellen Sie sicher, dass Sie args bewerten, die zu unverankertem Typ führen|
|SubtractionOperation |1. arg1 2. arg2|1. Argument, aus dem subtrahiert werden soll</br>2. Argument, das subtrahiert werden muss|Sie wertet sowohl die Werte innerhalb der args aus und subtrahiert den zweiten vom ersten|{</br>"Operator": "Subtraktion",</br>"arg1":</br>{</br>"Operator"..</br>}, </br>"arg2": 2</br>}|["Subtraktion", [4, 3] |Stellen Sie sicher, dass Sie args bewerten, die zu unverankertem Typ führen|
MultiplicationOperation |1. arg1|1. Array von Argumenten, die für Multiplikations Vorgänge erforderlich sind | Sie wertet alle Werte innerhalb der args aus und multipliziert Sie |{</br>"Operator": "Multiplikation", </br>"args": [</br>{</br>"Operator"..</br>}, 2, 4]</br>}|["Multiplikation", [1, 2, 3]|Stellen Sie sicher, dass Sie args bewerten, die zu unverankertem Typ führen|
|DivisionOperation |1. arg1</br>2. arg2|1. Argument, von dem geteilt werden soll </br>2. Argument, das geteilt werden muss  |Sie wertet sowohl die Werte innerhalb der args aus und teilt die zweite vom ersten|{</br>"Operator": "Division",</br>"arg1":</br>{</br>"Operator"..</br>}, </br>"arg2": 2</br>} |["Division", [4, 3] |Stellen Sie sicher, dass Sie args bewerten, die zu unverankertem Typ führen |
|ModuloOperation |1. arg1 </br>2. arg2|1. Argument, von dem geteilt werden soll </br> 2. Argument, das geteilt werden muss, um den Rest zu erhalten|Sie wertet sowohl die Werte innerhalb der args aus und teilt den zweiten vom ersten und gibt den Rest zurück. |{</br>"Operator": "Modulo",</br>"arg1":</br>{</br>"Operator"..</br>},</br>"arg2": 2</br>}|["Modulo", [4, 3] |Stellen Sie sicher, dass Sie args bewerten, die zu unverankertem Typ führen |

