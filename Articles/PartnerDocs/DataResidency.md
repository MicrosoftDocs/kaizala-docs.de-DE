# <a name="data-residency-and-go-local-support-in-microsoft-kaizala"></a>Daten Wohnsitz und lokale Unterstützung in Microsoft Kaizala

Ab April 2019 wird Microsoft Kaizala den regionalen Daten-Residency-Support über die Rechenzentren in Europa (EU), Asien-Pazifik (APAC), USA (USA) und Indien (IN) bereitstellen. Dies hat zur Folge, dass Kaizala-Kundendaten im Zusammenhang mit [Organisations Chats und Gruppen](https://support.office.com/article/organization-chats-and-groups-in-kaizala-c8a7855c-d232-4914-811c-f6708734dcc3) wie Nachrichten, Anlagen und Kaizala-Aktionen haben, die im Rechenzentrum ihrer Abrechnungs Region gespeichert werden.

Zusätzlich zur Unterstützung der Ziele von Data Residency innerhalb der Region können Kaizala-Dienst Datencenter auch Failover-und Notfallwiederherstellung über die Rechenzentren erleichtern.

## <a name="global-datacenter-footprint-with-data-residency-support"></a>Globaler Datencenter-Footprint mit Data Residency-Unterstützung

Derzeit verfügt Kaizala über acht Rechenzentren (Primary und Backup) in drei Regionen und einem Land:

- APAC (bedient Asien-Pazifik außer Indien)-Rechenzentren in Singapur und Hongkong
- EMEA (EU, MEA)-Rechenzentren in Dublin und Amsterdam
- AMER (Nord-und Südamerika)-Rechenzentren in Texas und Illinois
- Indien (go-local)-Rechenzentren in Chennai und Pune

Neben der Bereitstellung von COMPUTE und Storage bietet Kaizala auch Unterstützung für Daten Residency, robustes Failover und Notfallwiederherstellung für Unternehmenskunden. Außerdem können diese Skalierungseinheiten sowohl für Unternehmens-als auch für allgemeine Kunden eine verbesserte Konnektivität und Messagingleistung sicherstellen. 

![Grafik mit Daten Wohnsitz und lokalen Geo-Begrenzungen in Kaizala](Images/data-residency-geo-boundaries.png)

## <a name="how-is-data-stored-in-kaizala"></a>Wie werden Daten in Kaizala gespeichert?

Kaizala speichert Daten basierend auf den Datentypen der Nachrichten unterschiedlich.

- **Chats, likes und comments** -alle Nachrichten, Vorlieben und Kommentardaten, die zu Organisationsgruppen-oder org 1:1-Chats gehören, werden in einem sicheren Office 365-und Azure powered Chat-Dienst gespeichert, der auf der Grundlage ihres Abrechnungs Landes Regional begrenzt ist.
- **Attachments** – alle Anlagen befinden sich zusammen mit Chatnachrichten in derselben Daten Grenze.
- **Kaizala Action Cards** -alle Kaizala-Aktionskarten Daten, die Metadaten, Aktionspaket und Antwort Berichtsdaten enthalten, sind mit Chatdienst in derselben Daten Grenze zusammengefunden.
- **Calling** -Transient, Kaizala-Anrufdaten werden nicht in Rechenzentren gespeichert. Anrufprotokolle folgen jedoch denselben Daten Wohnsitz wie Chats.

### <a name="example"></a>Beispiel

Contoso hat sein Office 365-Abrechnungs Land in der EU. Contoso hat sich auf Kaizala im April 2019 angemeldet, und alle Kern Daten, einschließlich Chats, Anlagen und Aktionskarten, werden in Ruhe ausschließlich in EU-Einheiten (Dublin und Amsterdam) gespeichert.

## <a name="what-is-in-store-in-future"></a>Was ist in der Zukunft?

- Onboarding auf der Seite für die **Datenspeicherort** -für Unternehmen ist der Datenspeicherort für unterschiedliche Arbeitsauslastungen von Office 365 unter dem Office 365-Administratorportal unter Home\Organizational-Profil sichtbar. Die Möglichkeit zur Onboarding-Kaizala auf der Seite Datenspeicherort im Administratorportal wird angezeigt. In diesem Abschnitt finden Sie Updates.
- **Neue Rechenzentren** – das Kaizala-Team beruht ständig auf der Erweiterung der Benutzerfreundlichkeit. Wenn Sie einen geschäftlichen Fall haben, veröffentlichen Sie Ihre Fragen in unserer [TechNet-Community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala).

## <a name="faqs"></a>Häufig gestellte Fragen (FAQs)

### <a name="what-does-it-mean-for-existing-enterprise-customers"></a>Was bedeutet dies für bestehende Unternehmenskunden?

Bestehende Kunden in Indien haben bereits Ihren Daten Wohnsitz in Indien. Daten für alle nicht von Indien bestehenden Mandanten bleiben jedoch weiterhin am Gruppen Standort (basierend auf dem Landescode des Erstellers). Nach dem 2019. April beginnen jedoch alle neueren Organisationsgruppen und Nachrichten vorhandener Organisationsgruppen oder Chats nach Daten Wohnsitz basierend auf der Abrechnungs Region des Mandanten.

### <a name="what-does-it-mean-for-new-enterprise-customers"></a>Was bedeutet dies für neue Enterprise-Kunden?

Der Daten Wohnsitz wird automatisch für alle Kunden angewendet, die sich nach April 2019 auf Kaizala registrieren. Darüber hinaus sollte auf den neuesten Android-oder iOS-App-Versionen der Daten Wohnsitz auf Aktionskarten angewendet werden.
 
### <a name="i-do-have-more-questions-who-do-i-reach-out-to"></a>Ich habe noch weitere Fragen. An wen kann ich mich wenden?

Wenn Sie weitere Fragen haben, wenden Sie sich an Ihr Account-Team oder unsere [TechNet-Community](https://techcommunity.microsoft.com/t5/Microsoft-Kaizala/ct-p/MicrosoftKaizala). Darüber hinaus können Sie in [Kaizalafeedback@microsoft.com](mailto:kaizalafeedback@microsoft.com)schreiben.








