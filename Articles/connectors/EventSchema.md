# <a name="webhook-response-schema-for-registered-events"></a>Webhook Antwortschema für registrierte Ereignisse

Wenn eine Webhook registriert ist, wird eine Antwort WebHook für jedes Ereignis Kaizala auf die registrierten ObjectId für registrierte Ereignisse gefiltert zurückgegeben. Hier finden Sie Informationen über Schemas für verschiedene Webhook Antwort für verschiedene Ereignisse.

## <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| objectId | String | Bezeichner, die für das Objekt, in welchen, das Kontext der Webhook erstellt wurde. Für ObjectType = Gruppe, dessen Gruppenbezeichner für ObjectType = Action, dessen ActionId für ObjectType = ActionPackage, dessen Action-Paket-Id |
| objectType | String | Enum: "Group" / "Aktion" / "ActionPackage" |
| eventType | String | Registrierte Ereignis, das aufgerufen wurde |
| eventId | String | Bezeichner für das Ereignis |
| data | JSON-Objekt | Ein Objekt, Daten, die spezifisch für dieses Ereignis darstellt. Parameter für jeden unterstützten Ereignisempfänger beschrieben. |
| context | String | Gibt-Wert, der bei der Registrierung einer Webhook unter Parameter 'CallbackContext' festgelegt wurde|
| fromUser | String | Telefonnummer des Absenders |
| fromUserId | String | Benutzer-ID des Absenders |
| fromUserName | String | Registrierte Namen mit Kaizala des Absenders |
| fromUserProfilePic | url | Des Absenders Profil Pic |

Der Parameter 'Daten' würde je nach Ereignis WebHook variieren. Schema finden Sie für jedes Ereignis unten.

### <a name="data-for-event-textmessagecreated"></a>Daten für 'TextMessageCreated'-Ereignis
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| text | String | Textnachricht, die gesendet wurde |

#### <a name="sample-webhook-response-for-textmessagecreated"></a>Beispiel WebHook Antwort für 'TextMessageCreated'
```javascript
{
  "objectId": "8c2050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "TextMessageCreated",
  "eventId": "55ed01-02b5-491e-8e7e-484726da976b",
  "data": {
    "text": "Test Message"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-attachmentcreated"></a>Daten für 'AttachmentCreated'-Ereignis
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Medien | Array | Jedes Element enthält, MediaUrl und mediaFileName|
| mediaUrl | url | URL des Bilds |
| mediaFileName | String | Dateiname |
| actionType | String | Enum-Wert: 'Image' |
| Beschriftung | String | Beschriftung mit dem Bild zugeordnet ist |

#### <a name="sample-webhook-response-for-attachmentcreated"></a>Beispiel WebHook Antwort für 'AttachmentCreated'
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "AttachmentCreated",
  "eventId": "59e2e9f9-9b10-4b67-8bc5-3f85a04f2d91",
  "data": {
    "media": [
      {
        "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/0ad142c52b30d797addebadb620c19bf6f018299ed4acdce5760e45e2e4bc4ae.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Thbp46wdgoqbDaAF06v2Y2ijzny0jx2fBDo1EZab%2BNY%3D&amp;st=2018-03-22T10:22:21Z&amp;se=2292-01-05T11:22:21Z&amp;sp=r",
        "mediaFileName": "IMG_18-03-22_165220084_1.jpg"
      }
    ],
    "actionType": "Image",
    "caption": "Testing."
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```
### <a name="data-for-event-announcement"></a>Daten für das Ereignis 'Ankündigung'
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ankündigung Aktion |
| text | String | Nachrichtentext der Ankündigung Aktion |
| Medien | Array | Jedes Element enthält, MediaUrl und mediaFileName|
| mediaUrl | url | URL des Bilds |
| mediaFileName | String | Dateiname |


#### <a name="sample-webhook-response-for-announcement"></a>Beispiel WebHook Antwort für 'Ankündigung'
```javascript
{
  "objectId": "8c291050-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "Announcement",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "text": "Caption :Testing.",
    "title": "Sent by Robin Richard",
    "media": [
      {
        "url": "https://cdn.inc-000.kms.osi.office.net/contenthost/beb2cfef8732c6cc3b54652c1f6f99d64f529fd9be3d409e2966552639fb791f.jpeg",
        "fileName": "e3c145f1-5e6f-4ee9-bd83-49ec3a1c2550.jpeg"
      }
    ]
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobcreated"></a>Daten für 'JobCreated'-Ereignis
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ankündigung Aktion |
| text | String | Nachrichtentext der Ankündigung Aktion |
| actionId | Id | Bezeichner für die betreffende Instanz des Auftrags-Aktion |
| dueDate | Date | Datum nach dem Auftrag abläuft |
| assignedTo | Zeichenfolgenarray | Array von Telefonnummern |


#### <a name="sample-webhook-response-for-jobcreated"></a>Beispiel WebHook Antwort für 'JobCreated'
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "assignedTo": [
      "+919740797266"
    ],
    "title": "Test Job",
    "dueDate": "2018-03-22T18:29:59Z",
    "actionId": "aeb012-31a0-477a-a131-8a1e2791b36e",
    "groupId": "8c291050-9be8-6-97f5-bb7013930027"
  },
 "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-jobresponse"></a>Daten für 'JobResponse'-Ereignis
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ankündigung Aktion |
| text | String | Nachrichtentext der Ankündigung Aktion |
| actionId | Id | Bezeichner für die betreffende Instanz des Auftrags-Aktion |
| groupId | String | Gruppen-ID. |
| responseId | String | GUID zum Identifizieren dieser Antwort |
| responseDetails | Zeichenfolgenarray | Array von Antwortobjekte |
| Benutzer, dem | String | Telefonnummer der zugewiesenen Person |
| assigneeName | String | Benutzer, die dem Namen |
| assigneeProfilePic | url | URL von der zugewiesenen Profil pic |
| isCompleted | Boolean | Ist der Auftrag werden abgeschlossen? |




#### <a name="sample-webhook-response-for-jobresponse"></a>Beispiel WebHook Antwort für 'JobResponse'
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "actionId": "2ce34820-3d67-4807-9a1d-7cf099c2e7ae",
    "groupId": "8c291050-9be8-45d6-97f5-bb7013930027",
    "responseId": "80a883ec-e6c7-4dc8-979d-d268bbeeee8b",
    "responseDetails": {
      "response": {
        "assignee": "++91xxxxxxxx",
        "assigneeName": "Robin Richard",
        "assigneeProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d536285d08e6409e416.jpg",
        "isCompleted": true
      }
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

### <a name="data-for-event-actioncreated--surveycreated"></a>Daten für das Ereignis 'ActionCreated' / 'SurveyCreated'
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | Id | Bezeichner für die betreffende Instanz des Auftrags-Aktion |
| groupId | String | Gruppen-ID. |
| responseId | String | GUID zum Identifizieren dieser Antwort |
| Fragen | Zeichenfolgenarray | Array von Objekten |
| Responder | String | Telefonnummer des Responders |
| responderName | String | Name des Responders |
| responderProfilePic | url | URL der Responder Profil pic |
| isAnonymous | Boolean | Die Antwort Umfrage ist anonym gesendet wurde |
| isUpdateResponse | Boolean | Die Antwort aktualisiert wurde, vom Responder, nachdem die Antwort zuvor übermittelt wurde |


#### <a name="schema-details-for-responsewithquestions-object"></a>Schemadetails für 'ResponseWithQuestions'-Objekt
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Frage Titel |
| Typ | String | QuestionType |
| options | Array | Liste der Optionen (Schlüssel / Wert-Paar) für mit mehreren choice Fragen |
| isInvisible | Boolean | Die Frage wird von der Benutzeroberfläche ausgeblendet werden |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a>Beispiel-WebHook Antwort für 'ActionCreated' / 'SurveyCreated'
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "ActionCreated",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```



### <a name="data-for-event-surveyresponse-actionresponse"></a>Daten für das Ereignis 'SurveyResponse' / 'ActionResponse'
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | Id | Bezeichner für die betreffende Instanz des Auftrags-Aktion |
| groupId | String | Gruppen-ID. |
| responseId | String | GUID zum Identifizieren dieser Antwort |
| responseDetails | Zeichenfolgenarray | Array von 'ResponseWithQuestions'-Objekten |
| Responder | String | Telefonnummer des Responders |
| responderName | String | Name des Responders |
| responderProfilePic | url | URL der Responder Profil pic |
| isAnonymous | Boolean | Die Antwort Umfrage ist anonym gesendet wurde |
| isUpdateResponse | Boolean | Die Antwort aktualisiert wurde, vom Responder, nachdem die Antwort zuvor übermittelt wurde |


#### <a name="schema-details-for-responsewithquestions-object"></a>Schemadetails für 'ResponseWithQuestions'-Objekt
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Frage Titel |
| Typ | String | QuestionType |
| options | Array | Liste der Optionen für mit mehreren choice Fragen |
| answer | Array von Json-Objekt | Antworten |
| isInvisible | Boolean | Die Frage wird von der Benutzeroberfläche ausgeblendet werden |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a>Beispiel WebHook Antwort für 'SurveyResponse' 'ActionResponse'
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "SurveyResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
   "actionId": "920f9802-62dafb-9bc2-8d3ba5c43609",
    "groupId": "8c291050-9be8-4d6-97f5-bb7013930027",
    "responseId": "420e9ef0-2a6d-405-a2bf-2688648ce79a",
    "isUpdateResponse": false,
    "responder": "+91xxxxxxxxx",
    "responderName": "Robin Richard",
    "responderProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-f391-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg",
    "isAnonymous": false,
    "responseDetails": {
      "responseWithQuestions": [
        {
          "title": "1",
          "type": "Text",
          "options": [],
          "answer": "1"
        },
        {
          "title": "2",
          "type": "AttachmentList",
          "options": [],
          "answer": [
            {
              "mediaUrl": "https://cdn.inc-000.kms.osi.office.net/att/9841be297131449fba1123ec8545ab30fa72c2017555ba4bcd4ac18d5f7850b4.jpg?sv=2015-12-11&amp;sr=b&amp;sig=Egd4wDmAfGrIoklLj70SrV7D3QtwtMEWQx673U%3D&amp;st=2018-03-23T09:26:24Z&amp;se=2292-01-06T10:26:24Z&amp;sp=r",
              "mediaFileName": "IMG_18-03-23_155619990_1.jpg"
            }
          ]
        },
        {
          "isInvisible": true,
          "title": "ResponseTime",
          "type": "DateTime",
          "options": [],
          "answer": 1521800782956
        }
      ]
    }
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```


### <a name="data-for-event-memberadded--memberremoved"></a>Daten für das Ereignis 'MemberAdded' / 'MemberRemoved'
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Mitglied | String | Telefonnummer des Elements hinzugefügt |
| memberName | String | Name des Elements hinzugefügt |
| Typ | String | Rolle des Elements hinzugefügt Membership |
| memberProfilePic | url | URL von der zugewiesenen Profil pic |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a>Beispiel-WebHook Antwort für 'MemberAdded' / 'MemberRemoved'
```javascript
{
  "objectId": "8c2950-9be8-45d6-97f5-bb7013930027",
  "objectType": "Group",
  "eventType": "JobResponse",
  "eventId": "3e49b367-acf6-48a7-a675-6bf4d372a070",
  "data": {
    "member": "+91xxxxxxxx",
    "memberName": "Jan Decker",
    "memberProfilePic": "https://mobileonlyapps.blob.core.windows.net/polymer-7ebb8d90e1324b5cbd61d1e10a30ada7/bbac582a4364860679d40fda7c6b.jpg",
    "type": "Member"
  },
  "context": "Any data which is required to be returned in callback",
  "fromUser": "+91xxxxxxxx",
  "fromUserId": "72e91-f3-4e7b-84eb-4e228406fb9b",
  "fromUserName": "Robin Richard",
  "fromUserProfilePic": "https://mobileonlyapps.blob.core.windows.net/72e29591-4e7b-84eb-4e228406fb9b/c34afc0d53614ae29285d08e6409e416.jpg"
}
```

