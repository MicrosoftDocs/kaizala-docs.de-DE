# <a name="test-and-debug"></a>Testen und Debuggen

Nachdem benutzerdefinierte Aktion Entwicklung erfolgt ist, sollten Sie testen, um festzustellen, ob seine fehlerfrei funktioniert bis zum Ende zu beenden und Beheben von Fehlern, die Sie testen zu erkennen. Als auch in einigen Fällen möchten Sie die HTML-Ansichten auf mögliche Probleme zu debuggen.

Die Kaizala-Verwaltungsportal bietet eine bequeme Möglichkeit zum Testen und Debuggen Ihre neue Kaizala Aktionen. 
>   Sie benötigen ein aktiv Kaizala Pro oder Office365 Organisationseinheit Abonnement für das Management Portal zugreifen.

## <a name="steps-to-test-a-action"></a>Schritte zum Testen einer Aktion

Nachdem Sie die erforderlichen Komponenten erfüllt haben, können Sie Ihre Aktion durch folgenden unten beschriebenen Schritte testen.

*   Navigieren Sie zu dem Kaizala-Verwaltungsportal @https://manage.kaiza.la/
*    Melden Sie sich mit einem vorhandenen Office365-Konto
*    Registrieren Sie, indem Sie durch Tippen auf "Hinzufügen einer Telefonnummer" eine Rufnummer im Portal
*    Tippen Sie auf "Aktionen" im linken Menü auf
*    Wählen Sie aus der Dropdownliste aus 'Meine Aktionen'
*    Suchen Sie nach, und klicken Sie auf die Aktion, die Sie testen möchten. 
*    Öffnen Sie die Version der Aktion, die im Entwurf Zustand befindet
*    Tippen Sie auf dieser Seite auf "Stufe"
*    Nachdem die Aktion bereitgestellt ist, können Sie die Aktion an die Gruppen hinzufügen die Sie ein Administrator sind

> Die Gruppe benötigen eine verwaltete Palette für die Rolle des Benutzers, die die Aktion getestet wird

Um die Palette "managed" vornehmen, führen Sie folgende Schritte aus:
*    Navigieren Sie im linken Menü auf "Gruppen"
*    Hier finden Sie die Gruppe, den, die Sie verwenden möchten, die Aktion Palette für verwalten, und klicken Sie auf die ausgewählte Gruppe
*    Wechseln Sie zur Registerkarte für die ausgewählte Gruppe 'Aktionen'
*    Klicken Sie auf den Link, um die Aktion Palette für die verschiedenen Rollen verwalten
     *    Wählen Sie im Dialogfeld Benutzer, die für die Verwaltung die Palette werden soll
     *    Klicken Sie auf 'Speichern'
*    Sie können hier finden Sie die Aktion in der Palette der ausgewählten Gruppen und verwenden Sie es entsprechend.

## <a name="steps-to-debug-a-action"></a>Schritte zum Debuggen einer Aktion

Nachdem Sie einen Test Aktion hochgeladen haben, können Sie die HTML-Ansichten für den Test Aktion Debuggen.

*   Aktivieren von 7-Mal auf Buildnummer tippen Developer-Optionen. [Weitere wissen sollten](https://www.androidcentral.com/how-enable-developer-settings-android-42).
*   Einschalten @ debuggingeinstellungen USB -> Developer Optionen -> USB-Debuggen
*   Fügen Sie Telefon über USB-Kabel an Computer, und installieren Sie die erforderlichen Gerätetreiber bei Bedarf. [Mehr erfahren](https://developer.android.com/studio/run/oem-usb.html)
*   Öffnen Sie Kaizala app zu, und öffnen Sie die Aktivität die Webansicht-Inhalt enthält.
*   Geben Sie in Computer und geben Sie **Chrome://inspect** in der Adressleiste und Treffer Open Chrome-Browsers. 
*   Benutzer sehen seinem Gerät erwähnten es zusammen mit einer HTML-Seite, die in der Webansicht von seinem Kaizala app geöffnet ist.


**Mehr:** [Instant Bearbeiten der mehrstufigen Aktionen](EditAction.md)</br>
**Weiter:** [Veröffentlichen einer Gruppe](publish.md)
