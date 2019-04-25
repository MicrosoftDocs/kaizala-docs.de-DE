# <a name="webhook-response-schema-for-registered-events"></a>Webhook-Antwortschema für registrierte Ereignisse

Wenn ein webhook registriert ist, gibt Kaizala für jedes Ereignis in der registrierten objectId, gefiltert nach registrierten Ereignissen, eine webHook-Antwort zurück. NachFolgend finden Sie Schema Details für verschiedene webhook-Antworten für verschiedene Ereignisse.

## <a name="response-body"></a>Antworttext
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| objectId | String | Bezeichner, der das Objekt darstellt, in dem der webhook erstellt wurde. Für Objekttyp = Gruppe, ID der Gruppe, für ObjectType = Action, its Action-ID, für ObjectType = ActionPackage, its Action-Package-Identifier |
| objectType | String | Enum: "Group"/"action"/"ActionPackage" |
| eventType | String | Registriertes Ereignis, das aufgerufen wurde |
| eventId | String | Bezeichner, der das Ereignis darstellt |
| data | JSON-Objekt | Objekt, das die für dieses ereignisspezifischen Daten darstellt. Für jedes unterstützte Ereignis definierte Parameter. |
| context | String | Gibt den Wert zurück, der bei der Registrierung eines webhooks unter dem Parameter "callbackcontext" festgelegt wurde.|
| fromUser | String | Telefonnummer des abSenders |
| fromUserId | String | Absender-ID |
| fromUserName | String | Registrierter Name des abSenders mit Kaizala |
| fromUserProfilePic | url | Profilbild des abSenders |

Der Parameter "Data" würde je nach webHook-Ereignis variieren. Nachfolgend finden Sie ein Schema für jedes Ereignis.

### <a name="data-for-event-textmessagecreated"></a>Daten für das Ereignis ' TextMessageCreated '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| text | String | Text Nachricht, die gesendet wurde |

#### <a name="sample-webhook-response-for-textmessagecreated"></a>Beispiel-webHook-Antwort für ' TextMessageCreated '
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

### <a name="data-for-event-attachmentcreated"></a>Daten für das Ereignis ' AttachmentCreated '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Medien | Array | Jedes Element enthält mediaUrl und mediaFileName|
| mediaUrl | url | URL des Bilds |
| mediaFileName | String | Filename |
| actionType | String | Enumerationswert: ' Image ' |
| Beschriftung | String | mit dem Bild verknüpfte Beschriftung |

#### <a name="sample-webhook-response-for-attachmentcreated"></a>Beispiel-webHook-Antwort für ' AttachmentCreated '
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
### <a name="data-for-event-announcement"></a>Daten für Ereignis Ansage
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ansage Aktion |
| text | String | Nachrichtentext der Ansage Aktion |
| Medien | Array | Jedes Element enthält mediaUrl und mediaFileName|
| mediaUrl | url | URL des Bilds |
| mediaFileName | String | Filename |


#### <a name="sample-webhook-response-for-announcement"></a>Beispiel-webHook-Antwort für "Ansage"
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

### <a name="data-for-event-jobcreated"></a>Daten für das Ereignis ' JobCreated '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ansage Aktion |
| text | String | Nachrichtentext der Ansage Aktion |
| actionId | Id | Bezeichner für diese bestimmte Instanz von Job-Aktion |
| dueDate | Date | Datum, an dem der Auftrag ablaufen würde |
| assignedTo | Zeichenfolgenarray | Array von Telefonnummern |


#### <a name="sample-webhook-response-for-jobcreated"></a>Beispiel-webHook-Antwort für ' JobCreated '
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

### <a name="data-for-event-jobresponse"></a>Daten für das Ereignis ' JobResponse '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Titel der Ansage Aktion |
| text | String | Nachrichtentext der Ansage Aktion |
| actionId | Id | Bezeichner für diese bestimmte Instanz von Job-Aktion |
| groupId | String | Gruppenbezeichner |
| Antwort-Nr. | String | GUID zum Identifizieren dieser Antwort |
| responseDetails | Zeichenfolgenarray | Array von Response-Objekten |
| Empfänger | String | Telefonnummer des Empfängers |
| assigneeName | String | Name des Empfängers |
| assigneeProfilePic | url | URL des Profils des Empfängers PIC |
| isCompleted | Boolean | Ist der Auftrag abgeschlossen? |




#### <a name="sample-webhook-response-for-jobresponse"></a>Beispiel-webHook-Antwort für ' JobResponse '
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

### <a name="data-for-event-actioncreated--surveycreated"></a>Daten für das Ereignis ' ActionCreated '/' SurveyCreated '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | Id | Bezeichner für diese bestimmte Instanz von Job-Aktion |
| groupId | Zeichenfolge | Gruppenbezeichner |
| Antwort-Nr. | String | GUID zum Identifizieren dieser Antwort |
| Fragen | Zeichenfolgenarray | Array von Objekten |
| Responder | String | Telefonnummer des Responders |
| responderName | String | Name des Responders |
| responderProfilePic | url | URL des Profils des Responders PIC |
| isAnonymous | Boolean | Wurde die Umfrageantwort anonym übermittelt |
| isUpdateResponse | Boolean | Wurde die Antwort von Responder aktualisiert, da die Antwort zuvor übermittelt wurde |


#### <a name="schema-details-for-responsewithquestions-object"></a>Schema Details für ' responseWithQuestions '-Objekt
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Frage Titel |
| type | Zeichenfolge | Questiontype |
| options | Array | Liste der Optionen (Schlüssel-Wert-Paar), die für Fragen mit mehreren Auswahlen gelten |
| isUnsichtbar | Boolean | Ist die Frage von der Benutzeroberfläche ausgeblendet |



#### <a name="sample-webhook-response-for-actioncreated--surveycreated"></a>Beispiel-webHook-Antwort für ' ActionCreated '/' SurveyCreated '
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



### <a name="data-for-event-surveyresponse-actionresponse"></a>Daten für das Ereignis ' SurveyResponse '/' ActionResponse '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| actionId | Id | Bezeichner für diese bestimmte Instanz von Job-Aktion |
| groupId | Zeichenfolge | Gruppenbezeichner |
| Antwort-Nr. | String | GUID zum Identifizieren dieser Antwort |
| responseDetails | Zeichenfolgenarray | Array von ' responseWithQuestions '-Objekten |
| Responder | String | Telefonnummer des Responders |
| responderName | String | Name des Responders |
| responderProfilePic | url | URL des Profils des Responders PIC |
| isAnonymous | Boolean | Wurde die Umfrageantwort anonym übermittelt |
| isUpdateResponse | Boolean | Wurde die Antwort von Responder aktualisiert, da die Antwort zuvor übermittelt wurde |


#### <a name="schema-details-for-responsewithquestions-object"></a>Schema Details für ' responseWithQuestions '-Objekt
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| title | String | Frage Titel |
| type | Zeichenfolge | Questiontype |
| options | Array | Liste der Optionen, die für Fragen mit mehreren Auswahlen gelten |
| Antwort | Array des JSON-Objekts | Antworten |
| isUnsichtbar | Boolean | Ist die Frage von der Benutzeroberfläche ausgeblendet |



#### <a name="sample-webhook-response-for-surveyresponse-actionresponse"></a>Beispiel-webHook-Antwort für ' SurveyResponse ' ' ActionResponse '
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


### <a name="data-for-event-memberadded--memberremoved"></a>Daten für das Ereignis ' MemberAdded '/' MemberRemoved '
| Parameter | Typ | Beschreibung |
| :---: | :---: | :--- |
| Element | String | Telefonnummer des hinzugefügten Members |
| memberName | String | Name des hinzugefügten Members |
| type | Zeichenfolge | Mitgliedschafts Rolle des hinzugefügten Members |
| memberProfilePic | url | URL des Profils des Empfängers PIC |





#### <a name="sample-webhook-response-for-memberadded-memberremoved"></a>Beispiel-webHook-Antwort für ' MemberAdded '/' MemberRemoved '
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

