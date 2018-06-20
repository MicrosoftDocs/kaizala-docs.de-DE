# <a name="get-started-with-custom-kaizala-actions"></a>Erste Schritte mit benutzerdefinierten Kaizala Aktionen

## <a name="kaizala-action-development-lifecycle"></a>Kaizala Aktion Entwicklungslebenszyklus

Der normalen Entwicklungszyklus einer Aktion Kaizala umfasst die folgenden Schritte aus:

  **Schritt 1: entscheiden Sie sich für den Zweck der Aktion Kaizala**
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
Überlegen Sie sich, was die wichtigsten Features und Szenarios sind, und konstruieren Sie Ihr Design um diese herum.

   **Schritt 2: Identifizieren Sie das Datenmodell für die Aktion Kaizala**

Alle Kaizala Aktionen sind derzeit Formular basiert – d. h. ist das Datenmodell das Aggregieren Informationen anfordert, erfassen und eine Reihe von Frage und Antworttypen, die von der Plattform Kaizala Aggregation Services (KAS) unterstützt werden. Stellen Sie sich wie die Daten für die Aktion erforderlich Levergage können der Formular-Infrastruktur effektiv funktioniert.

   **Schritt 3: Entwerfen und implementieren die Benutzer wünschen und die Benutzeroberfläche für das Add-in.**

Entwerfen Sie ein schnelles und flüssiges Zusammenspiel Benutzererlebnis, der konsistente, leicht zu, mit häufig vorkommenden Szenarien erlernen, die nur einige Schritte erforderlich ist. Remeber, die eine Aktion Kaizala auf externen Quellen - verweisen kann nicht so praktikabel im Hinblick auf was Sie innerhalb der Aktion implementieren möchten.

Sie können aus einer Vielzahl von Webentwicklungstools auswählen und HTML und JavaScript verwenden, um die Benutzeroberfläche zu implementieren.

KAS Client JS-SDK können Sie mit der Kaizala Aggregation Dienste und die systemeigene Kaizala Client interagieren. 

   **Schritt 4 – erstellen eine Manifestdatei für die Aktion auf die Paket-Manifestschema basierte**

Erstellen einer Manifestdatei im JSON-Schreibweise zu identifizieren, die Aktion und die zugehörigen Komponenten, und geben Sie die Namen der Dateien anzeigen.

**Schritt 5 – eine ZIP-Datei des Pakets erstellen und auf das Portal hochladen**

Erstellen Sie eine ZIP-Datei des Pakets mit aller die Ressourcen im Stammverzeichnis des Pakets.

Laden Sie das Paket auf dem Kaizala-Verwaltungsportal. Nach dem Hochladen ist Aktion im Zustand Entwurf

**Schritt 6: Phase die Aktion Entwurf**

Tippen Sie auf der Detailseite der Aktion Version sich im Entwurf Zustand befindet, auf die Schaltfläche "Stufe". Nachdem eine Aktion bereitgestellt wird, können testen und Debuggen die Aktion 

 **Schritt 7: Aktivieren der mehrstufigen Aktion**

Sobald eine Aktivität befindet sich in mehrstufigen Zustand und erfolgreich getestet wurde, können Sie die Aktion in Ihrer Organisation aktivieren. Aktion verschiebt in aktiven Zustand. Andere Mitglieder in Ihrer Organisation können diese Aktion auch ihren jeweiligen Gruppen hinzufügen.

  **Schritt 8: Fügen Sie den jeweiligen Gruppen**

Sobald Aktion aktiv ist, können Sie die Aktion zu Gruppen zugeordnet Ihrer Organisation bereitstellen. 

