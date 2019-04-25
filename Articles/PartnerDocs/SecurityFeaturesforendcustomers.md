# <a name="security-for-end-users"></a>Sicherheit für Endbenutzer
## <a name="client-data-protection"></a>Client Datenschutz

Alle Datenspeicher auf Android-, iOS-und Windows-Clients werden auf internen Speichern ausgeführt, die Anwendungs-Sandbox bereitstellen, die Ihre APP-Daten und die Codeausführung von anderen apps isoliert. Benutzer erteilte Berechtigungen zum Einschränken des Zugriffs auf System Features und Benutzerdaten werden nur verwendet. Kaizala folgt allen Plattformstandards, um den Zugriff auf Clientressourcen basierend auf den zulässigen Berechtigungen einzuschränken. Kein externer Speicher, der Lese-und Schreibzugriff auf Welt ermöglicht, wird verwendet. MODE_WORLD_READABLE oder MODE_WORLD_WRITEABLE sind nicht aktiviert. 

## <a name="authentication-and-authorization"></a>Authentifizierung und Autorisierung

Microsoft Kaizala Mobile App authentifiziert die Benutzer auf Geräten, die Telefonnummer und einmaliges Kennwort (OTP) verwenden, um die Anmelde-und Onboarding-Erfahrung zu vereinfachen.  

Aus Sicherheitsgründen wendet Kaizala auch mehrere Sicherheitsrichtlinien an, um eine Telefonnummer auf ein Gerät zu begrenzen und die Anzahl von OTP-Anforderungen an einem Tag.  

Der Zugriff auf alle Kundendaten wie Nachrichten, Dokumente, Medien usw. ist auf die relevanten Endbenutzer, Gruppenmitglieder und Organisationsadministratoren beschränkt. 

Die mehrstufige Authentifizierung für die Benutzer der Kaizala-App kann über Gruppenrichtlinien aktiviert werden. Ein Gruppen-oder mandantenadministrator kann zusätzliche Office 365-Kontonamen (AAD) erzwingen, um eine Kaizala-Gruppe öffnen zu können. Dies hat zur Folge, dass ein Benutzer sich zusätzlich zur Telefonnummer & OTP bei AAD-verknüpften Konto in Kaizala Mobile-App anmelden muss. Bis der Benutzer sich mit AAD verknüpften Konto anmeldet, können die Nachrichten in der Gruppe vom Benutzer für die konfigurierte Gruppe nicht angezeigt werden. 

Das Kaizala-Verwaltungs Portal verwendet die Azure Active Directory Services-Authentifizierung für den sicheren Zugriff und die Verwaltung von Organisationsdaten. Dieser Dienst wird von Millionen Kunden weltweit verwendet, um Ihre Geschäftsdaten sicher in Office 365 zu hosten. 

In Kaizala ist die vollständige Steuerung der Gruppenverwaltung und Mitgliedschaften nur für Gruppen-und Organisationsadministratoren zulässig. 

## <a name="kaizala-group-policies"></a>Kaizala-Gruppenrichtlinien

Kaizala bietet Gruppen-und mandantenadministratoren die Möglichkeit, den Datenfluss und das Verhalten innerhalb einer einzelnen oder aller Organisationsgruppen zu steuern. Nachfolgend finden Sie die verschiedenen Gruppenrichtlinien, die von Gruppen-und mandantenadministratoren konfiguriert werden können, um die Datensicherheit zu verbessern: 

  
- Einschränken der Weiterleitung von Nachrichten-, Anlage-und Kaizala-Aktionen aus der aktuellen Gruppe oder deren Organisationsgruppen 
- Einschränken des Kopierens von Inhalten für Nachrichten, Anlagen und Kaizala-Aktionen 
- Einschränken der Freigabe von Inhalten für Nachrichten, Anlagen und Kaizala-Aktionen 
- Aktivieren Sie mehrstufige Authentifizierung für Mitglieder über AAD, sodass der Benutzer sich mit seinem Organisations AAD-Konto anmelden muss, um Nachrichten innerhalb der Gruppe anzuzeigen. 
- Aktivieren Sie Microsoft InTune für Erweiterte Richtlinien, beispielsweise PIN nach der Leerlaufdauer. Wenn der Benutzer InTune nicht aktiviert hat, wird die Gruppe möglicherweise nicht vom Benutzer geöffnet. 

## <a name="mobile-application-management-with-microsoft-intune"></a>Mobile Anwendungsverwaltung mit Microsoft InTune

Für die Erweiterte Anwendungsverwaltung kann die Mobile Kaizala-App mit Microsoft InTune Containern werden. Microsoft Kaizala ist nativ in das InTune SDK integriert und bietet Erstanbieter Support für erweiterte InTune-spezifische Richtlinien, die nachfolgend aufgeführt sind:
    - PIN-Zugriff auf Mobile App für verbesserte Clientsicherheit erforderlich 
    - Blockieren der Ausführung von verwalteten Apps auf per Jailbreak oder Rooting manipulierten Geräten 
    - Cut, Copy, Paste mit anderen verwalteten apps einschränken • Einschränken der APP zum Übertragen von Daten zu/von anderen verwalteten apps 
    - Blockieren der Bildschirmaufzeichnung oder Bildschirmfreigabe 
    - Erzwingen einer minimalen Android-Betriebssystemversion 
    - Anzeige von Webinhalten auf den Managed Browser beschränken
    - Offline Intervall vor dem Löschen der Daten 

Die Intune-Richtlinien können auf einfache Weise zentral über das InTune-Portal verwaltet werden, wie im folgenden dargestellt:  

![InTune. PNG](Images/Intune.png)



