# <a name="get-started-with-custom-kaizala-actions"></a>Erste Schritte mit benutzerdefinierten Kaizala-Aktionen

## <a name="kaizala-action-development-lifecycle"></a>Kaizala-Aktions Entwicklungslebenszyklus

Der typische Entwicklungslebenszyklus einer Kaizala-Aktion umfasst die folgenden Schritte:

  **Schritt 1: Bestimmen des Zwecks der Kaizala-Aktion**
    
    Ask the following questions:
    
      - How is the Action useful? 
      - How does it make sense in a conversational context?
      - What is the information that flows from the creator to a responder and vice versa?
      - What scenarios does your Action support?
    
Überlegen Sie sich, was die wichtigsten Features und Szenarios sind, und konstruieren Sie Ihr Design um diese herum.

   **Schritt 2: Identifizieren des Datenmodells für die Kaizala-Aktion**

Alle Kaizala-Aktionen sind derzeit Formular basiert, d.h. das Datenmodell zum anfordern, sammeln und Aggregieren von Informationen ist eine Reihe von Frage-und Antworttypen, die von der Kaizala-Aggregations Dienste-Plattform (KAS) unterstützt werden. Stellen Sie sich vor, wie die für Ihre Aktion erforderlichen Daten levergage können, damit die formularinfrastruktur effektiv funktioniert.

   **Schritt 3: Entwerfen und Implementieren der Benutzerumgebung und der Benutzeroberfläche für das Add-in.**

Entwerfen Sie eine schnelle und flüssige Benutzererfahrung, die konsistent und leicht zu erlernen ist, und für deren primäre Szenarien nur wenige Schritte erforderlich sind. Denken Sie daran, dass eine Kaizala-Aktion nicht auf externe Quellen verweisen kann – also im Hinblick darauf, was Sie in ihrer Aktion implementieren möchten.

Sie können aus einer Vielzahl von Webentwicklungstools auswählen und HTML und JavaScript verwenden, um die Benutzeroberfläche zu implementieren.

Sie können das KAS-Client-JS-SDK verwenden, um mit den Kaizala-Aggregations Diensten und dem systemeigenen Kaizala-Client zu interagieren. 

   **Schritt 4: Erstellen einer Manifestdatei für die Aktion basierend auf dem Paketmanifest-Schema**

Erstellen Sie eine Manifestdatei in JSON-Notation, um die Aktion und ihre Komponenten zu identifizieren und die Namen der Ansichtsdateien anzugeben.

**Schritt 5: Erstellen einer ZIP-Datei des Pakets und hochladen im Portal**

Erstellen Sie eine ZIP-Datei des Pakets mit allen Ressourcen im Stammverzeichnis des Pakets.

Laden Sie das Paket im Kaizala-Verwaltungs Portal hoch. Nach dem Hochladen befindet sich die Aktion im Entwurfsstatus.

**Schritt 6-Phase der Entwurfs Aktion**

Tippen Sie auf der Detailseite der Aktions Version, die sich im Entwurfszustand befindet, auf die Schaltfläche "Stufe". Nachdem eine Aktion ausgeführt wurde, können Sie & testen, um die Aktion zu debuggen. 

 **Schritt 7 – Aktivieren der stufenweisen Aktion**

Sobald sich eine Aktion im Status "Staging" befindet und erfolgreich getestet wurde, können Sie die Aktion in Ihrer Organisation aktivieren. Aktion wechselt in den aktiven Zustand. Andere Mitglieder in Ihrer Organisation können diese Aktion auch zu ihren jeweiligen Gruppen hinzufügen.

  **Schritt 8: Hinzufügen der Aktion zu den entsprechenden Gruppen**

Sobald sich die Aktion im aktiven Zustand befindet, können Sie die Aktion für Gruppen bereitstellen, die Ihrer Organisation zugeordnet sind. 

