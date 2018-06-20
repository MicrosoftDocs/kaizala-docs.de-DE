# <a name="security-for-end-users"></a>Sicherheit für Endbenutzer
## <a name="client-data-protection"></a>Client-Datenschutz

Alle Daten speichern auf Android-, IOS- und Windows-Clients sind auf interne Speichern ausgeführt, die Sandbox der Anwendung angeben, die Ihre app-Daten und Code-Ausführung von anderen apps isoliert. Berechtigungen zum Einschränken des Zugriffs auf Systemfeatures und Benutzerdaten dem Benutzer erteilt werden nur verwendet werden. Kaizala richtet alle die Plattform Standards Zugriff einschränken auf Clients Ressourcen basierend auf Berechtigungen gewährt. Keine externer Speicher World Lese- und Schreibzugriff, wodurch wird verwendet. MODE_WORLD_READABLE oder MODE_WORLD_WRITEABLE sind nicht aktiviert. 

## <a name="authentication-and-authorization"></a>Authentifizierung und Autorisierung

Microsoft Kaizala mobile app authentifiziert Benutzer auf Geräten mit Telefonnummer und eine Uhrzeit Password (OTP) für einfacher Anmeldung und Onboarding wünschen.  

Aus Sicherheitsgründen gilt Kaizala auch mehrere Sicherheitsrichtlinien, um eine Telefonnummer an einem Gerät zu einer Zeit und die Anzahl der OTP Anforderungen pro Tag einschränken.  

Zugriff auf alle Kundendaten, wie Nachrichten, Dokumente, Medien usw. ist auf die relevanten Endbenutzer und Mitglieder der Gruppe Organisations-Administratoren beschränkt. 

Mehrstufige Authentifizierung für die Kaizala app-Benutzer kann mithilfe von Gruppenrichtlinien aktiviert werden. Ein Gruppe oder des Mandanten Admin erzwingen möglicherweise zusätzliche Anmeldung für Office 365 (AAD) um eine Gruppe Kaizala öffnen können. Dies bedeutet, dass einen Benutzer darüber hinaus müssen sich anmelden AAD verknüpft Konto in der mobilen app Kaizala, Telefonnummer & OTP. Erst nach der Anmeldung mit AAD Konto verknüpft, können vom Benutzer für den konfigurierten Gruppe die Nachrichten in der Gruppe angezeigt werden. 

Kaizala-Verwaltungsportal verwendet Azure Active Directory Services-Authentifizierung für sicheren Zugriff und Verwaltung von Unternehmensdaten. Dieser Dienst wird von Millionen von Kunden weltweit verwendet zum Hosten ihrer Geschäftsdaten sicher in Office 365. 

In Kaizala ist die vollständige Kontrolle über die Verwaltung und Mitgliedschaften nur die Gruppe und die entsprechenden Organisations-Administratoren beschränkt. 

## <a name="kaizala-group-policies"></a>Kaizala von Gruppenrichtlinien

Kaizala bietet die Möglichkeit für Gruppe und Mandanten Administratoren, die den Datenfluss und Verhalten in eine einzelne oder alle Organisationsgruppen steuern. Dies sind die verschiedenen Gruppenrichtlinien, die von Gruppen- und Mandanten Administratoren zur Verbesserung der Sicherheit konfiguriert werden können: 

  
- Einschränken Sie Weiterleiten von Nachrichten, Anlagen und Kaizala Aktionen aus der aktuellen Gruppe oder seine Organisationseinheit 
- Einschränken Sie kopieren von Inhalt für Nachrichten, Anlagen und Kaizala Aktionen 
- Einschränken Sie gemeinsame Nutzung von Inhalten für Nachrichten, Anlagen und Kaizala Aktionen 
- Aktivieren der mehrstufigen Authentifizierung für Mitglieder über solche AAD muss der Benutzer melden Sie sich mit ihrer Organisation AAD Konto Nachrichten innerhalb der Gruppe anzeigen. 
- Aktivieren Sie Microsoft Intune für erweiterte Richtlinien diese Vorgaben unter PIN-Nummer nach der Leerlaufzeit. Wenn Benutzer Intune aktiviert, kann die Gruppe nicht vom Benutzer geöffnet sein. 

## <a name="mobile-application-management-with-microsoft-intune"></a>Verwaltung von mobilen mit Microsoft Intune

Erweiterte anwendungsverwaltung kann die mobile app Kaizala mit Microsoft Intune Containern werden. Microsoft Kaizala Intune SDK systemintern integriert ist und bietet Unterstützung für erste Anbieter für bestimmte erweiterte Intune-Richtlinien, die unten aufgeführten:
    - Benötigen Sie PIN-Zugriff in der mobilen app für erweiterte Clientsicherheit (engl.) 
    - Block verwaltete apps Ausführung auf Jailbroken oder Stamm-Geräten 
    - Einschränken Ausschneiden, kopieren, fügen Sie ihn mit anderen verwalteten apps • Restrict-app zum Übertragen von Daten und andere verwaltete apps 
    - Bildschirmaufnahme blockieren oder Bildschirmfreigabe 
    - Android OS Mindestversion erzwingen 
    - Einschränken von Webinhalten in verwalteten Browser anzeigen
    - Offline Intervall, bevor die Daten gelöscht wird 

Die Richtlinien Intune können auf einfache Weise zentral über Intune Portal, verwaltet werden, wie unten dargestellt:  

![Intune.PNG](Images/Intune.png)



