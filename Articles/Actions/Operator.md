# <a name="chat-card-customization---operators"></a>Chat Karte Anpassung - Operatoren 

In einigen Szenarien auftreten gibt es muss, in denen möglicherweise unterschiedliche Benutzer müssen verschiedene Chat-Karte anzeigen, die basiert auf einige Attribute. Um diese Szenarien zu ermöglichen, bietet Kaizala Operatoren, mit dem Ersteller der Aktion Chat Kartenansichten für die gleiche Aktionsinstanz unterschiedlich für verschiedene Szenarien/Benutzer personalisieren können.

## <a name="lets-take-an-example"></a>Betrachten Sie ein Beispiel:

Nehmen wir an, dass wir die Kartenansicht anders als dessen Empfängern Absender anzeigen möchten. Mit Operatoren, die wir in diesem Szenario problemlos erreichen können, liegt unter der benutzerdefinierten Chat Ansicht JSON für diese:  


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

Hier können Sie diesen Operator beobachten "Conditional_value" Abrufen Boolean-Wert aus geschachtelten Operator "Is_it_me" Weiter mit Operator "Property_value" geschachtelt. In ähnlicher Weise kann dies auf einfache Weise auf eines dieser Szenarien, sogar komplexe eine erweitert werden. Darüber hinaus muss der folgende Eintrag hinzugefügt werden, um das Paketmanifest: ActionStoreSchema: "<name of the action store schema definition file>". Weitere Informationen finden Sie in [JSON Manifestschema Paket](package_manifest_schema.md) .


 
## <a name="list-of-supported-operators"></a>Liste der unterstützten Operatoren: 

> **Hinweis** : die Variablen X, y, Z, die in den Syntaxbeispielen verwendet können einfache Werte oder von geschachtelten Operatoren zurückgegebene Ergebnis sein 


| Operatorname |Parametername |Parametertyp |Funktion  |Syntax |Minimierten Syntax | Hinweis |
|--------|------|------|----|----|----|----|
|Bedingter Wert  |1. Bedingung 2. Wert 3. Standard|1. boolescher Wert 2. JSON-Wert 3. JSON-Wert | Dieser Operator wird verwendet, um einen angegebenen Wert zurück, wenn eine definierte Bedingung true ist. Wenn die Bedingung false ist, gibt den False zurück.|{</br>"Operator": "Conditional_value", "Bedingung": x "Wert": {y}, "Default": {Z}</br>}| ["Conditional_value", X, Y, Z] ||
|Gleich |1. 2.Klicken Wert |    1. 2.Klicken Zeichenfolge |True, wenn die angegebenen Werte (Wert1, Wert2) gleich sind, gibt dieser Operator zurück. Andernfalls wird false zurückgegeben |    {</br>"Operator": "Eq", "value1": X, "Wert2": y </br>} |[x, y "Eq"] ||
|FormatProfileName  |1. 2-Eigenschaft. Src |1. Zeichenfolge 2.Klicken PropertyType| Ruft die Eigenschaft aus der Src 'PropertyType' ab und formatiert die Liste der Benutzer-IDs als:</br></br>' < Name des Benutzers 1 > & n Weitere ' </br></br>n ist die Anzahl der Benutzer in der Liste - 1 vorhanden |{</br>"Operator": "Format_profile_names",</br>"Property": X, "Src": PropertyType</br>}|["Format_profile_names" PropertyType, X] |PropertyType</br>{</br>  lokale server</br>} </br></br>1. dieser Operator wird davon ausgegangen, dass die Eigenschaft X bereitgestellten Array von Benutzer-IDs zurückgibt </br></br>2. Benutzername1 ist Sie, wenn der aktuelle angemeldete Benutzer in der Liste der Benutzer-IDs vorhanden ist.|
|FormatString|1. Format 2. Agrs|1. Zeichenfolge 2.Klicken Array von Argumenten, die von der Formatzeichenfolge erwartet|Dieser Operator ermöglicht es, eine Zeichenfolge mit Formatspezifizierer formatieren formatieren.</br></br>Dieser Operator ist dasselbe wie alle anderen Format String-Operator in Cpp oder Java vorhanden |{</br>"Operator": "Format_string", "format": X, "Args": [y, Z...]</br>}|["Format_string", X, [y, Z...]]|Wie %s, Operatoren und %d usw. erwartet Argumente in derselben Reihenfolge des gleichen Typs vorhanden sein muss, kann X Bezeichner enthalten. </br></br>Für diese Vorgaben unter Zeichenfolge sein können</br>{</br>"Operator": "Format_string",</br>"Format": "Mein Name befindet sich %s und Meine Alter ist %d,"</br>"Args": [y, Z]</br>}</br></br>Wobei y ist eine String-Variable und z ist eine ganze Zahl|
|IsCurrentUser|1. Wert|1. Uuid vergleicht die bereitgestellte Uuid (UserId) mit dem Uuid (Benutzer-ID) des aktuellen angemeldeten Benutzers. Es gibt true zurück, wenn sie entspricht, und andernfalls "false" zurückgibt |{</br>"Operator": "Is_it_me",</br>"Wert": X</br>}|["Is_it_me" X]|
|JSONPathValue|1. 1. Entität 2.Klicken Pfad|1. EntityType 2.Klicken gültige Json Pfad| Ruft den Wert in der Entität Json vom angegebenen Typ am Schlüssel darstellen.  Es gibt ersten Wert, der erreicht wird im Pfad zurück. |{</br>"Operator": "Jsonpath_value",</br>"Entity": EntityType,</br>"Pfad": ValidJsonPath</br>}|["Jsonpath_value", "EntityType", ValidJsonPath]|{</br>"Operator":</br>"Jsonpath_value",</br>"Entity": Nachricht</br>"Pfad": "$... SenderName"</br>}</br></br>"$.." Rekursiv durchlaufen</br></br>"$." Nur 1. Ebene Entität hinweg|
|MessageConversationName|1. der Wert|1. messageId|Gibt den Namen der Unterhaltung zugewiesen die Nachricht mit MessageId gehört.|{"Operator": "Message_conversation_name", "Wert": X}|["Message_conversation_name", X]|
|MessageCreationTime|1. der Wert|1. messageId|Gibt der Menschen lesbare Zeitstempel Zeichenfolge für den Erstellungszeitstempel der Nachricht mit den angegebenen messageId |{</br>"Operator": "Message_creation_time",</br>"Wert": X</br>}|["Message_creation_time", X]|
|Profilname|1. id|1. uuid|Der Anzeigename des Benutzers zurück, wenn Uuid (UserId) bereitgestellt wird |{</br>"Operator": "Profilname", "Id": X</br>}|["Profilname", X]|
|PropertyValue|1. Src 2.Klicken-Eigenschaft|1. PropertyType 2.Klicken Zeichenfolge|Ruft die Eigenschaft aus der Src PropertyType|{</br>"Operator": "Property_value",</br>"Property": X, "Src": PropertyType</br>}|["Property_value" PropertyType, X]|PropertyType</br></br>{</br>lokale server</br>}|
|AdditionOperation |1. Arg1 | 1. Array von Argumenten, die von Addition ein benötigt |Es wird alle Werte, die sich innerhalb der Args ausgewertet und fügt diese hinzu |{</br>"Operator": "hinzufügen",</br>"Args": [{</br>"Operator".</br>}, 2,4]</br>} |["hinzufügen", [1, 2, 3]]|Vergewissern Sie sich für Args ausgewertet werden soll, wodurch Gleitkomma-Typ|
|SubtractionOperation |1.Arg1 2.Arg2|1. Argument aus der subtrahiert werden soll</br>2.-Argument muss subtrahiert werden soll|Es wird sowohl die Werte innerhalb der Args ausgewertet und im zweiten Beispiel aus dem ersten subtrahiert|{</br>"Operator": "Subtraktion"</br>"arg1":</br>{</br>"Operator".</br>}, </br>"arg2": 2</br>}|["Subtraktion", [4, 3]] |Vergewissern Sie sich für Args ausgewertet werden soll, wodurch Gleitkomma-Typ|
MultiplicationOperation |1. Arg1|1. Array von Argumenten, die von Multiplikation benötigt | Es wird alle Werte, die sich innerhalb der Args ausgewertet und mit multipliziert |{</br>"Operator": "Multiplikation" </br>"Args": [</br>{</br>"Operator".</br>}, 2,4]</br>}|["Multiplikation", [1, 2, 3]|Vergewissern Sie sich für Args ausgewertet werden soll, wodurch Gleitkomma-Typ|
|DivisionOperation |1. Arg1</br>2. Arg2|1. aus dem Dividieren-argument </br>2.-Argument aufgeteilt werden muss  |Es wird die Werte innerhalb der Args ausgewertet und teilt im zweiten Beispiel aus dem ersten|{</br>"Operator": "Division",</br>"arg1":</br>{</br>"Operator".</br>}, </br>"arg2": 2</br>} |["Division", [4, 3]] |Vergewissern Sie sich für Args ausgewertet werden soll, wodurch Gleitkomma-Typ |
|ModuloOperation |1. Arg1 </br>2. Arg2|1. aus dem Dividieren-argument </br> 2.-Argument werden muss aufgeteilt, um den Rest abrufen|Sie wertet die Werte innerhalb der Args und teilt im zweiten Beispiel aus dem ersten auf und gibt den Rest zurück |{</br>"Operator": "modulo"</br>"arg1":</br>{</br>"Operator".</br>},</br>"arg2": 2</br>}|["modulo" [4, 3]] |Vergewissern Sie sich für Args ausgewertet werden soll, wodurch Gleitkomma-Typ |

