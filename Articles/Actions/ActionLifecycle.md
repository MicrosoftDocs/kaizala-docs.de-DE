# <a name="action-lifecycle"></a>Aktions Lebenszyklus

Eine Aktion kann 5 Status aufweisen:

* **Entwurf** -Aktion wurde erfolgreich hochgeladen. Sie ist nur für Aktions Entwickler und Organisations-Admins im Kaizala-Verwaltungs Portal sichtbar. Es kann nicht zu Gruppen hinzugefügt werden
* **Staging** -Action in einem stufenweisen Zustand kann (vor der Bereitstellung) in Gruppen getestet werden, für die die Aktion Creator ein Administrator ist. Sie ist nur für Aktions Entwickler und Organisations-Admins auf dem Kaizala-Verwaltungs Portal sichtbar.
* **Aktiv** – nachdem eine Version einer Aktion bereitgestellt wurde, kann Sie aktiviert werden. Im aktiven Zustand ist es für alle Mitglieder der Organisation verfügbar, es in ihren Gruppen im Kaizala-Verwaltungs Portal hinzuzufügen.
* **Inaktiv** -Aktion im aktiven Zustand kann deaktiviert werden. In diesem Zustand ist das betreffende Aktionspaket anderen Mitgliedern in der Organisation nicht zur Verfügung, um es Ihren Gruppen hinzuzufügen. In der Kaizala-App kann Sie weiterhin von Benutzern in den Gruppen verwendet werden, in denen diese Aktion bereits hinzugefügt wurde.
* **Removed** – wenn eine Version einer Aktion explizit entfernt oder durch eine andere Version ersetzt wird, wird Sie in den Zustand "entfernt" verschoben. In Kaizala-Apps stehen diese Pakete nicht für Benutzer zur Verfügung.
