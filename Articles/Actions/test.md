# <a name="test-and-debug"></a>Testen und Debuggen

Nachdem Sie die Entwicklung der benutzerdefinierten Aktion ausgeführt haben, können Sie Sie testen, um zu prüfen, ob Ihre Arbeit am Ende endet und Fehler beseitigt, die Sie beim Testen entdecken. Als auch in einigen Fällen möchten Sie die HTML-Ansichten für mögliche Probleme Debuggen.

Das Kaizala-Verwaltungs Portal bietet eine bequeme Möglichkeit zum Testen von &, die die neuen Kaizala-Aktionen Debuggen. 
>   Sie benötigen ein aktives Kaizala pro-oder Office365-Organisations Abonnement für den Zugriff auf das Verwaltungs Portal.

## <a name="steps-to-test-a-action"></a>Schritte zum Testen einer Aktion

Nachdem Sie die Voraussetzungen erfüllt haben, können Sie die Aktion anhand der folgenden Schritte testen.

*   Navigieren Sie zum Kaizala-Verwaltungs Portal @https://manage.kaiza.la/
*    Anmelden mit einem vorhandenen Office365-Konto
*    Registrieren Sie eine Telefonnummer im Portal, indem Sie auf "Telefonnummer hinzufügen" tippen.
*    Tippen Sie im linken Menü auf Aktionen.
*    Wählen Sie im Dropdownmenü "meine Aktionen" aus.
*    Suchen und klicken Sie auf die Aktion, die Sie testen möchten 
*    Öffnen der Version der Aktion im Entwurfsstatus
*    Tippen Sie auf dieser Seite auf "Stufe".
*    Nachdem die Aktion ausgeführt wurde, können Sie die Aktion zu den Gruppen hinzufügen, von denen Sie ein Administrator sind.

> Die Gruppe muss über eine verwaltete Palette für die Benutzerrolle verfügen, die die Aktion testet.

Führen Sie die folgenden Schritte aus, um die Palette "verwaltet" zu erstellen:
*    Navigieren Sie im linken Menü zu "Gruppen".
*    Suchen Sie die Gruppe, für die Sie die Aktions Palette verwalten möchten, und klicken Sie auf die ausgewählte Gruppe.
*    Wechseln Sie zur Registerkarte "Aktionen" für die ausgewählte Gruppe.
*    Klicken Sie auf den Link zum Verwalten der Aktions Palette für verschiedene Rollen.
     *    Wählen Sie im Dialog Feld Benutzer aus, für die Sie die Palette verwalten möchten.
     *    Klicken Sie auf speichern.
*    Sie können die Aktion in der Palette der ausgewählten Gruppen finden und entsprechend verwenden.

## <a name="steps-to-debug-a-action"></a>Schritte zum Debuggen einer Aktion

Nachdem Sie eine Testaktion hochgeladen haben, können Sie die HTML-Ansichten für die Testaktion Debuggen.

*   Aktivieren Sie die Option Entwickler Optionen, indem Sie 7 Mal auf Buildnummer tippen. [Mehr wissen](https://www.androidcentral.com/how-enable-developer-settings-android-42).
*   Aktivieren von USB-Debugging @ Settings-> Developer Options-> USB Debugging
*   Verbinden Sie das Telefon über USB-Kabel mit dem Computer, und installieren Sie die erforderlichen Gerätetreiber, falls erforderlich. [Weitere Informationen](https://developer.android.com/studio/run/oem-usb.html)
*   Öffnen Sie die Kaizala-APP, und öffnen Sie dann die Aktivität mit WebView-Inhalt.
*   Öffnen Sie Chrome Browser in Computer, und geben Sie **Chrome://Inspect** in Adressleiste ein, und drücken Sie die EINGABETASTE. 
*   Der Benutzer sieht sein Gerät dort erwähnt, zusammen mit einer HTML-Seite, die im WebView seiner Kaizala-app geöffnet wird.


**Weitere Informationen:** [Sofortige Bearbeitung von inszeniertEn Aktionen](EditAction.md)</br>
**Als nächstes:** [Veröffentlichen in einer Gruppe](publish.md)
