# Richtlijnen om Mattermost te vertalen naar het Nederlands

<!-- vim-markdown-toc GFM -->

* [Inleiding](#Inleiding)
    * [Vertalingsserver](#Vertalingsserver)
    * [Opmerkingen voor vertalers](#opmerkingen-voor-vertalers)
    * [Offline vertaling](#offline-vertaling)
    * [Test jouw vertalingen](#test-jouw-vertalingen)
    * [Tools voor de vertaler](#tools-voor-de-vertaler)
        * [Pology](#pology)
        * [Bases de connaissance](#bases-de-connaissance)
    * [Punten om te verbeteren in de Nederlandse vertaling](#punten-om-te-verbeteren-in-de-nederlandse-vertaling)
    
* [Stijlgids](#stijlgoids)
    * [Jargon](#jargon)
    * [Hoofdletters](#hoofdletters)
    * [Afkortingen](#afkortingen)
    * [Citaten](#citaten)
    * [Majestueuze meervoud](#majestueuze-meervoud)
    * [Inclusie schrijven](#inclusief-schrijven)
    * [Traduction trop longue](#traduction-trop-longue)
    * [Gestion du pluriel](#gestion-du-pluriel)
        * [Exemple 1](#exemple-1)
        * [Exemple 2](#exemple-2)
        * [Exemple 3](#exemple-3)
        * [Exemple 4](#exemple-4)
* [Woordenschat](#Woordenschat)
    * [At rest / in transit](#at-rest--in-transit)
    * [API](#api)
    * [Attach](#attach)
    * [Autocompletion](#autocompletion)
    * [Batch](#batch)
    * [Before taking effect](#before-taking-effect)
    * [Beta](#beta)
    * [BG](#bg)
    * [Bot](#bot)
    * [Canonical](#canonical)
    * [Constraints](#constraints)
    * [Direct](#direct)
    * [Directory](#directory)
    * [Details](#details)
    * [Documentation](#documentation)
    * [Enter / specify / input field](#enter--specify--input-field)
    * [Email](#email)
    * [Emoji](#emoji)
    * [Encountered](#encountered)
    * [Endpoint](#endpoint)
    * [Failed to](#failed-to)
    * [FileInfos](#fileinfos)
    * [Flag](#flag)
    * [Folder](#folder)
    * [Follow up](#follow-up)
    * [Get / retrieve](#get--retrieve)
    * [Guest](#guest)
    * [Handle](#handle)
    * [Hours / timezone](#hours--timezone)
    * [Invitations](#invitations)
    * [Jobs](#jobs)
    * [Kick / ban / remove](#kick--ban--remove)
    * [Link/linking](#linklinking)
    * [Marketplace](#marketplace)
    * [Marshalling](#marshalling)
    * [Member / channel member / membership](#member--channel-member--membership)
    * [Message](#message)
    * [Message export job](#message-export-job)
    * [Modify](#modify)
    * [Mute](#mute)
    * [Notifications push / mobile / desktop](#notifications-push--mobile--desktop)
    * [Optional](#optional)
    * [Override](#override)
    * [Packaged](#packaged)
    * [Parse / parser](#parse--parser)
    * [Permanently](#permanently)
    * [Permissions](#permissions)
    * [Populate](#populate)
    * [Purge](#purge)
    * [Posted / posts / publication](#posted--posts--publication)
    * [Private message](#private-message)
    * [Preview mode](#preview-mode)
    * [Preview features](#preview-features)
    * [Privacy](#privacy)
    * [Purpose](#purpose)
    * [Rate limits](#rate-limits)
    * [Reactions](#reactions)
    * [Refresh](#refresh)
    * [Retrieve](#retrieve)
    * [Rollback](#rollback)
    * [Routes](#routes)
    * [Save](#save)
    * [Scheme](#scheme)
    * [Slash commands](#slash-commands)
    * [SSO](#sso)
    * [Support](#support)
    * [Sysadmin / system admin / team admin / channel admin](#sysadmin--system-admin--team-admin--channel-admin)
    * [Terms](#terms)
    * [Token / secret key](#token--secret-key)
    * [Trigger](#trigger)
    * [URL signing](#url-signing)
    * [Worker](#worker)

<!-- vim-markdown-toc -->

## Inleiding

Welkom en hartelijk dank om mee te willen werken aan de Nederlandse vertaling van Mattermost !

De Nederlandse vertaling wordt actief bijgewerkt. We geven hier wat raadgevingen en regels mee om de eenheid en consistentie in de vertaling te behouden. Bij vragen kan je steeds contact opnemen met ctlaltdieliet (Tom De Moor) op [https://community.mattermost.com](https://community.mattermost.com)

### Vertalingsserver

Mattermost gebruikt  [weblate voor de vertalingen](https://translate.mattermost.com/nl/). Het eenvoudigste om in te loggen is via je Gitlab of Github account.

Het aantal vertaalde zinnen is vrij hoog binnen het Mattermost-project. Als je vertalingen vindt die de onderstaande regels niet respecteren, aarzel dan niet om een correctie op Weblate voor te stellen.

Weblate wordt gebruikt sinds Mattermost versie 5.25 (juli 2020) en is dus nog vrij nieuw.

### Opmerkingen voor vertalers

Pootle ondersteunt het toevoegen van opmerkingen om de vertaler te helpen. Ze zijn handig om aan de gebruiker te specificeren of een zin bijvoorbeeld moet vertaald worden naar de infinitief of de imperatief. 
In het Engels is er inderdaad geen verschil tussen deze twee vormen, alleen de context en de consistentie van de rest van het dialoogvenster stellen ons in staat om de ene keer te kiezen in plaats van de andere.


Deze opmerkingen kunnen worden toegevoegd via Weblate.

Houd er echter rekening mee dat deze opmerkingen kort moeten zijn.



### Offline vertaling

Hoewel de Pootle-instantie die door Mattermost wordt gebruikt de mogelijkheid biedt om .po-bestanden te downloaden om ze te testen op een test-instantie van Mattermost, heeft de technische manager van Mattermost [handmatig uitgeschakeld op Pootle] (https: // pre-release .mattermost.com / core / pl / 9x5msk5iuifuxfm8wyjadsdyec) de mogelijkheid om vertalingen te verzenden en te vervangen door onze eigen .po-bestanden om de volgende redenen.

* Alle strings worden gemarkeerd als `vertaald` nadat het bestand is verzonden, zelfs als de strings niet zijn vertaald;
* Vertalingen kunnen verouderd zijn tussen het moment dat de bijdrager zijn bestand uploadt en het bestand terugstuurt naar Pootle;
* Het terugbrengen van de bestanden naar het platform overschrijft de vorige versie; in het geval van een probleem, zoals het in het vorige punt genoemde met opmerkingen die het bouwproces kunnen beschadigen, moet een ontwikkelaar het bestand kunnen herstellen in het geval dat hij zich realiseert dat de .po -> JSON-conversie mislukt. Mattermost kan niet garanderen dat een ontwikkelaar de tijd heeft die nodig is om deze actie toe te wijzen.

Dit is waarom online binnen Pootle de enige manier is om Mattermost te vertalen. Offline vertalingen zijn niet mogelijk.

### Test jouw vertalingen

Het wordt sterk aanbevolen om [een ontwikkelingsversie van Mattermost te gebruiken] (https://developers.mattermost.com/contribute/server/developer-setup/) zodat je  [ervoor kunt zorgen dat uw vertalingen correct zijn in de context ] (https://docs.mattermost.com/developer/localization.html#test-translations).
Maar het kan ook zonder!

### Tools voor de vertaler




#### Ondersteuning

Als je niet vindt hoe je een term moet vertalen, zijn er verschillende oplossingen:

* zie hoe dezelfde term de vorige keer werd vertaald in de vertaling van Mattermost,

* kijk op het [Microsoft-taalportaal] (https://www.microsoft.com/nl-nl/language/Search),

* stel uw vraag op [het Mattermost-kanaal gereserveerd voor Franse vertaling] (https://community.mattermost.com/core/channels/i18n-dutch).

### Punten om te verbeteren in de Nederlandse vertaling

De Nederlandse vertaling is volledig maar nog zeker niet consistent. Mogelijks is de vertaling meer Vlaams als Nederlands.

Zo is er het verschil in gebruik van u/jij of uw/jouw. Ook qua correcte spelling is er nog heel wat werk. 

Sommige zinnen zijn niet in overeenstemming met de context. Voel je dus zeker vrij om aanpassingen voor te stellen of zelf aanpassingen te maken.
Het consequent gebruik van [hoofdletters](###Hoofdletters) staat ook nog niet op punt.


## Stijlgids

### Jargon

Mattermost gebruikt zijn eigen jargon. Meer informatie hier rond vind je bij [Berichten](#Berichten).


### Hoofdletters

| EN | NL |
| --- | --- |
| System Console |Systeem console |
| Private Messages |Privé berichten|

In het Engels plaatst men hoofdletters in samengestelde woorden. Dit doen we niet in het Nederlands.

Vandaar dat we in zinnen geen hoofdletter gebruiken: Bijvoorbeeld. Ga naar systeem console. Enkel bij aanduidingen voor een menu gebruiken we wel een hoofdletter.  (bv.: `Accounteigenschappen` > `Geavanceerde opties` > `...`).

### Afkortingen

Bijvoorbeeld (e.g.) wordt afgekort als `Bijv. :`. Let op de spatie tussen het punt en het dubbelpunt. We gebruiken Bijv en niet bv.

### Citaten

Gerbruik dubbele aanhalingstekens om aan te geven dat het een citaat is.

### Majestueze meervoud.

Het majestueze meervoud wordt vrij vaak gebruikt in Engelse taalbronnen binnen Mattermost met de vermelding van de term 'We couldn't'.
volkomen onjuist.

Om zo dicht mogelijk bij andere vertalingen te zijn, zal dergelijke tekst worden vertaald als 'We konden de rechten niet controleren' in plaats van 'De machtigingen konden niet worden gecontroleerd' of 'Kan machtigingen niet controleren'.


### Inclusief schrijven

| EN | NL |
| --- | --- |
| @{{.Username}} was mentioned, but they did not receive notifications because they do not belong to this channel. | | @ {{.Username}} werd genoemd, maar ontvangt geen meldingen omdat deze niet tot dit kanaal behoort. |

We gebruiken geen hij/zij, omdat dit de tekst moeilijker te begrijpen maakt. Suggesties zijn zeker welkom omdat we inclusie belangrijk vinden.


### Te lange vertalingen

Als jouw vertaling te lang blijkt te zijn voor de ruimte die door de gebruikersinterface is toegewezen en als je, gezien de betekenis, de Nederlandse vertaling niet kan inkorten, leg het probleem dan uit op het [kanaal "Lokalisatie" van Mattermost] (https://community.mattermost.com/core/channels/localization).

### Meervouden

Binnen Mattermost worden de meervoudsregels volgens de taal beheerd door de formatjs-bibliotheek. Mogelijk komt je de syntaxis van deze bibliotheek tegen, afhankelijk van jouw vertalingen. De formatjs syntax komt als volgt tot stand:
    {key, plural, matches}

* `key`: dit is de variabele die het aantal elementen vertegenwoordigt
* `plural`: het is een vast trefwoord (in dit geval `meervoud`) dat aangeeft dat de afbeelding een aanroep van de formatjs-bibliotheek betreft.
* `matches`: 

In plaats van `matches'kunnen daarom een of meer van de volgende trefwoorden zijn:
* `zero`: Deze categorie wordt gebruikt voor talen die een specifieke grammatica hebben wanneer er geen element is, zoals Arabisch of Lets. Nederlands is niet direct betrokken bij dit element, we kunnen dat gebruiken dat betrekking heeft op het enkelvoud in plaats van op deze categorie.
* `one`: Deze categorie wordt gebruikt voor talen met een specifieke grammatica voor een enkel element, dat veel talen betreft. Veel Aziatische talen, zoals Chinees of Japans, gebruiken deze categorie NIET. Nederlands kent dit wel. We zullen daarom dit zoekwoord gebruiken, vaak in combinatie met `andere`, cf. verderop.
* `two`: Deze categorie wordt gebruikt voor talen met een specifieke grammatica voor twee elementen, zoals Arabisch of Welsh. Nederlands wordt ook beïnvloed, hoewel in plaats daarvan 'overig' kan worden gebruikt.
* `few`: Deze categorie wordt gebruikt voor talen met een specifieke grammatica voor een paar elementen. Sommige talen hebben regels voor 2-4 elementen, andere voor 3-10 en andere hebben zelfs complexere regels. Deze regel is niet van toepassing op het Nederlands.
* `many`: Deze categorie wordt gebruikt voor talen met een specifieke grammatica voor veel elementen zoals Arabisch, Pools of Russisch.
* `other`: Deze categorie wordt gebruikt als er geen waarde overeenkomt met een van de vorige categorieën. Deze categorie wordt vaak gebruikt als de meervoudsvorm voor bepaalde talen zoals Frans of Engels, die alleen een aparte grammatica hebben voor de enkelvoudige elementen en die meervoud.
* `=value`: Deze categorie wordt gebruikt om een bepaalde waarde aan te passen, ongeacht de meervoudscategorie die hierboven is gebruikt.

Om het [functioneren van deze bibliotheek] (https://formatjs.io/guides/message-syntax/#plural-format) te illustreren, nemen we de volgende voorbeelden.

#### Voorbeeld 1

    New {count, plural, one {message} other {messages}}

geeft binnen de interface "New message" in het enkelvoud en "New mesages" voor het meervoud.
In het Nederlands zijn ook 2 versies van vertaling vereist. Een voor het enkelvoud (`Nieuw bericht`) en de andere voor het meervoud (` Nieuwe berichten`).
In de formatjs syntax geeft dit het volgende:

    {count, plural, one {Nieuw bericht} other {Nieuwe berichten}}

#### Voorbeeld 2

    {count, number} {count, plural, one {user} other {users}} of {total, number} total

    {count, number} {count, plural, one {gebruiker} other {gebruikers}} op een totaal van {total, number}

Dit geeft 2 vertalingen: `1 gebruiker op een totaal van x` vs `x gebruikers op een totaal van x`.

#### Voorbeeld 3

    {count, number} {count, plural, one {Feature} other {Features}} Ingeschakeld

    {count, number} {count, plural, one {functie ingeschakeld} other {functies ingeschakeld}}

Zoals je kan zien, moet je, afhankelijk van de context, mogelijk meer woorden tussen accolades plaatsen om bij het bijvoeglijk naamwoord te passen. Het bijvoeglijk naamwoord is inderdaad onveranderlijk in het Engels, Engelse kanalen houden geen rekening met dit detail. `1 functie ingeschakeld` versus` x functies ingeschakeld`.

#### Voorbeeld 4

    Every {count, plural, one {minute} other {{count, number} minutes}}

    {count, plural, one {Elke minuut} other {Alle {count, number} minuten}}

Hier hebben we het over een belangrijke verandering, de zinomslag wordt helemaal niet op dezelfde manier vertaald, afhankelijk van of het enkelvoud of het meervoud is: 'Elke minuut' versus 'Elke x minuten'.

## Woordenschat

### In rust / In transit

| EN | NL |
| --- | --- |
| Invalid at rest encrypt key for SQL settings. Must be 32 chars or more. | Ongeldige coderingssleutel voor SQL-parameters voor gegevens in rust (gegevens die op schijven in deze datacenters zijn opgeslagen, worden "in rust" genoemd, in tegenstelling tot "in transit", hetzij wanneer ze via het netwerk worden overgedragen). Moet gelijk zijn aan of groter zijn dan 32 tekens. |

Dit concept is vrij recent en heeft recentelijk meer bekendheid gekregen na de inwerkingtreding van nieuwe regelgeving inzake de bescherming van persoonsgegevens zoals de GDPR.

In het kader van gegevensverwerking bevindt dit laatste zich altijd in een van de volgende staten:
* `Data in use`: data wordt constant veranderd van opslag naar datacenter, gebruik in spreadsheets, etc.
* `Data in motion` of `Data in transit`: wanneer de gegevens worden overgedragen via het computernetwerk of wanneer ze worden overgebracht naar RAM of eenvoudig worden bijgewerkt.
* `Data at rest`: inactieve data opgeslagen in databases, archieven, backups, kortom alle data die waarschijnlijk niet direct gebruikt zullen worden. In het geval van Mattermost kunnen dit de oude chatgegevens zijn die lang geleden op de applicatie zijn uitgewisseld.

We hebben besloten een aantal verduidelijkingen in de vertaalde keten te nemen om details over deze term nogal vaag voor een Nederlandstalige toe te voegen.

### API

| EN | NL |
| --- | --- |
| Empty array under 'image' in request | Lege array in de 'afbeelding' parameter van het verzoek |

In de context van een API-verzoek voegen we nog "parameter" toe.

### Bijvoegen

| EN | NL |
| --- | --- |
| Error attaching files to post. postId=%v, fileIds=%v, message=%v | Er is een fout opgetreden bij het koppelen van de bestanden aan het bericht. postId=%v, fileIds=%v, message=%v |
| Unable to attach emoji data to request | Kan geen emoji-gegevens koppelen aan verzoek |
| Attaching Files | Bestanden toevoegen |
| To import posts with attached files, see {slackAdvancedExporterLink} for details. | Om bestanden te importeren met bijgevoegde bestanden, zie {slackAdvancedExporterLink} voor verdere details. |

als we over bijlagen en toevoegen  bestanden gesproken, gebruik de term toevoegen of bijgevoegen`.

Gebruik anders indien mogelijk de `koppelen`. 

### Auto-aavullen of suggestie

| EN | NL |
| --- | --- |
| Check with your System Admin or open the autocomplete list by typing `/` to determine if your team configured any custom slash commands. | Vraag jouw systeembeheerder of open de lijst met opdrachtsuggesties door `/` te typen om te zien of jouw team aangepaste slash-opdrachten heeft geconfigureerd. |
| When true, Elasticsearch will be used for all autocompletion queries on users and channels using the latest index. | Indien ingeschakeld, wordt Elasticsearch gebruikt voor alle verzoeken om automatische aanvulling op gebruikers en kanalen met behulp van de laatst beschikbare index. |

Afhankelijk van het geval kan ook het idee van "suggestie" of "semi-automatische gegevensinvoer" worden uitgedrukt.

### Batch

| EN | NL |
| --- | --- |
| Email batching job's receiving channel was full. Please increase the EmailBatchingBufferSize. | Het kanaal dat batch-e-mails ontvangt, is vol. Verhoog de parameter EmailBatchingBufferSize. |

In bulk verzenden

### Before taking effect

| EN | NL |
| --- | --- |
| Changing properties in this section will require a server restart before taking effect. | Het wijzigen van de instellingen in deze sectie vereist een herstart van de server voordat deze van kracht worden. |



### Beta

| EN | NL |
| --- | --- |
| Compliance Export (Beta) | Compliance Export (Experimenteell) |

Hier, aangezien de term "alpha" niet aanwezig is in de interface, mag de notie van het voortgangspad van een project niet worden uitgedrukt. Het is daarom niet nodig om het jargon van de verschillende stadia van softwareontwerp te gebruiken. Er kan dan een meer Nederlandstalige term worden gebruikt die voor iedereen begrijpelijk is.

Bovendien klinkt 'bèta' in het Nederlands misschien als een belediging. Deze term kan worden uitgedrukt in de vorm van "experimentele functionaliteiten", een term die des te meer bekend is in andere software zoals LibreOffice.

### Achtergrond

| EN | NL |
| --- | --- |
| Button BG | Achtergrond van knop |

`BG` verwijst naar `background`. Wij gebruiken achtergrond.

### Bot

We gebruiken BOT of Bot omdat deze term in het Nederlands steeds vaker wordt gebruikt in de context van berichtenoplossingen om computerprogramma's aan te duiden die communiceren alsof het een persoon binnen de chat is.

### Canonical

| EN | NL |
| --- | --- |
| Invalid Canonical Algorithm. | Ongeldige canoniek algoritme |

De term "canoniek" verwijst naar het proces van het omzetten van gegevens in een gestandaardiseerde, genormaliseerde vorm. (zie [canonicalisatie op Wikipedia](https://en.wikipedia.org/wiki/Canonicalization)).

### Beperkingen

| EN | NL |
| --- | --- |
| Channel membership denied to the following users because of group constraints: {{ .UserIDs }} | De volgende gebruikers zijn vanwege groepsbeperkingen het lidmaatschap van het kanaal ontzegd: {{ .UserIDs }} |
| User cannot be added to this channel because it is constrained to group members only. | De gebruiker kan niet worden toegevoegd aan dit kanaal omdat het alleen beperkt is tot groepsleden.  |
| Unable to remove a user from a group-constrained team. | Kan een gebruiker niet verwijderen uit een team met groepsbeperkingen. |

Te vertalen naar "beperkingen" op het gebied van toegangsrechten.

### Create
| EN | NL |
| Create Posts | Berichten aanmaken |

"Create" wordt vertaald als "aanmaken".

### Direct

[cf. Bericht](#Bericht)

### Directory

De term map wordt gebruikt in de vertaling, met uitzondering van AD/LDAP of Active Directory, die onvertaald blijven omdat het de naam van een product is.

### Details

| EN | NL |
| --- | --- |
| Please ask your system administrator for more details | Vraag jouw systeembeheerder meer informatie |

Gebruik geen `voor meer details'. 

### Documentatie

In dit verband wordt de term 'Controleer de documentatie voor meer informatie' gebruikt. We gebruiken de zinsnede 'om meer te weten te komen' niet, die is te lang. 

Wanneer referenties zoals `voor documentatie' worden gebruikt, is het belangrijk om deze te vertalen als `onze documentatie' en niet als `de documentatie'. Dergelijke vermeldingen zijn inderdaad te vinden in het geval van ElasticSearch. In deze context is het Mattermost's eigen (en dus specifieke) ElasticSearch-documentatie; de gebruiker moet niet naar de generieke ElasticSearch-documentatie gaan die hem in dit geval niet zal helpen.

### Enter / specify / input field

| EN | NL |
| --- | --- |
| Please enter your email | Voer jouw email-adres in |
| Please enter an email address | Vier een email-adres in |
| SHIFT+DOWN (in input field): Highlight text to the next line\n | SHIFT+PIJLTJE OMLAAG (in het invoerveld): Selecteert de tekst tot aan de volgende regel.
Met het oog op de consistentie is de algemene regel om de term `invoeren` te gebruiken. 

Voor berichten die geen optie specificeren: een bericht, een sms, gebruiken we de term `opstellen` ([cf. Bericht](#bericht)).

### E-mail

| EN | NL |
| --- | --- |
| Unable to find status of recipient for batched email notification | Kan de status van de ontvanger niet vinden voor batch-e-mailmeldingen |
| Email invitations are disabled, no invite(s) sent | E-mailuitnodigingen zijn uitgeschakeld, er worden geen uitnodigingen verstuurd. |

Gebruik `e-mailadres` voor adressen en `e-mail` voor e-mailberichten. De correcte schrijfwijze is e-mail.

### Emoticon

`emoticon` wordt verkozen binnen de vertaling van Mattermost.

### Encountered

| EN | NL |
| --- | --- |
| An error encountered | Er is een fout opgetreden |


### Endpoint

[zie paragraaf over API's en API-routes](#Routes)


### Failed to Unable to

| EN | NL |
| --- | --- |
| Failed to upgrade websocket connection | Fout bij het upgraden van de WebSocket-verbinding |
| Post search failed to complete | Zoekopdracht kon niet worden niet voltooid |
| Unable to create the zip file | Fout bij het aanmaken van het zip-bestand |


Pragmatisch worden alle teksten die beginnen (en alleen die welke beginnen) met "Failed to" vertaald als "Kon niet" of "Fout bij" voor consistentie.

### FileInfos

Zoals [`NotifyProps`, zie hieronder](#Push notifications / mobile / desktop), dit is de naam van een object en moet vertaald worden volgens de context. Als het bericht bijvoorbeeld API-gerelateerd is, laat dan de term `FileInfos` staan; als het bericht bedoeld is voor de eindgebruiker, vertaalt u het naar `bestandinformatie`.

### Flag

| EN | NL |
| --- | --- |
| Flagged Posts | Gemarkeerde berichten |
| Flag | Markeren |
| Flag | Ajouter un indicateur |
| Flag | Marquer |
| Unflag | Markering verwijderen |


Let op, het woord `vlag` wordt ook gebruikt voor emoticon-categorieën (zie `.mobile.emoji_picker.flags`). In dit geval en alleen in dit geval, gebruik de term `Vlaggen`.

### Folder

[cf. Directory](#directory)

### Follow up

| EN | NL |
| --- | --- |
| Follow up flag | Volgmarkering |

Het zijn gewoon indicatoren om een boodschap te volgen. 

### Get / retrieve

| EN | NL |
| --- | --- |
| We couldn't get the team members | We konden de teamleden niet ophalen |
| Error to retrieve the current channel. | Fout bij het ophalen van het huidig kanaal. |

Ophalen wordt verkozen omwille van consistentie.

### Guest

| EN | NL |
| --- | --- |
| Guests | Gastgebruikers |
| Invite guests | Gastgebruiker uitnodigen |



### Handle

| EN | NL |
| --- | --- |
| A channel with that handle already exists | Er bestaat al een kanaal met deze pseudoniem |
| This field is handled through your login provider. If you want to change it, you need to do so through your login provider. | Dit veld wordt beheerd door de authenticatiedienst. Als u het wilt veranderen, moet u dit doen via uw authenticatiedienst. |

Gebruik in dit verband geen pseudoniem. Gebruikersnaam is voldoende.


### Hours / timezone

| EN | NL |
| --- | --- |
| {{.SenderName}} - {{.Hour}}:{{.Minute}} {{.TimeZone}}, {{.Month}} {{.Day}} | {{.SenderName}} - {{.Day}}/{{.Month}}, {{.Hour}}:{{.Minute}} {{.Timezone}} |

Bij vertaalwerk gaat het niet alleen om een domme en vervelende vertaling van zinnen. De zinnen moeten ook worden aangepast aan het gebruik of de gewoonte. In de Nederlandstalige wereld is de volgorde van de elementen van een datum niet dezelfde als in het Engels. Dit is allemaal een kwestie van lokalisatie.

In dit geval wordt de datum voor de tijd geplaatst en worden de elementen gescheiden door een schuine streep (`/`).


### Invitations

[cf. e-mail](#email)

### Jobs

| EN | NL |
| --- | --- |
| No indexing jobs queued. | Geen indexeringstaken in de wachtrij. |

De term `taak' wordt in het jargon gebruikt (zie `geplande taken' in Windows).

### Kick / ban / remove

| EN | NL |
| --- | --- |
| Remove a member from the channel | Verwijder een kanaallid |
| Failed to add user to channel because they have been removed from the team. | Fout bij het toevoegen van het kanaallid omdatdat deze verwijderd werd uit het team. |
| Failed to find user to be removed | Kon de te verwijderen gebruiker niet vinden. |
| Unable to remove license file, err=%v | Fout bij het verwijderen van het licentiebestand, err=%v |

* Voor een bestand gebruiken we `wissen`.
* Voor het verwijderen van een gebruiker uit een kanaal of team, gebruiken we "verwijderen".
* Voor een `ban` gebruiken we `verbannen` om dichter bij het Engels te zijn en termen als `uitsluiten` te vermijden.
* Voor een `kick`, gebruiken we `schoppen'
* Om een gebruiker volledig te verwijderen, gebruik je `verwijderen`.
* Het verschil tussen een 'ban' en een 'schop' is of de gebruiker later opnieuw kan verbinden. Voor het bannen zal de gebruiker niet in staat zijn om opnieuw in te loggen totdat de kanaalbeheerder van gedachten verandert.

### Link/linking

| EN | NL |
| --- | --- |
| Link failed | De associatie heeft gefaald |
| Linked | Geassocieerd |
| Unlink failed | Fout bij dissociatie |

Deze vermeldingen komen vaak voor bij het synchroniseren van gebruikers op meerdere platforms, met name AD/LDAP-mappen. In deze context zullen we de termen "associatie" en "dissociatie" gebruiken die het vaakst voorkomen in plaats van de term "link". We hebben geen vertaling voor "unlink" wat het geheel minder harmonieus maakt.

### Marketplace

| EN | NL |
| --- | --- |
| Plugin Marketplace | Plugin marktplaats |
| Failed to marshal marketplace plugins. | Niet in staat om de gegevens van de plugins op de marktplaats te interpreteren. |
| URL of the marketplace server. | De URL van de marktplaats server. |

### Marshalling

| EN | NL |
| --- | --- |
| An error occurred marshalling the JSON data for export. | Er is een fout opgetreden bij het voorbereiden van JSON-gegevens voor export (marshalling). |
| marshal error | fout in de gegevenstransformatie (marshalling) |
| Failed to marshal marketplace plugins. | Fout bij de interpretatie van de gegevens van de plugins op de marktplaats. |

In de computerwetenschap is marshalling de handeling waarbij de geheugenvoorstelling van een object wordt omgezet in een formaat dat bestemd is voor netwerkopslag of -transmissie. Deze term komt dicht in de buurt van serialisatie. Om ons aan te passen aan deze definitie, aarzelen we niet om veralgemeningen in de vertaling te nemen, zodat niet-Engelstaligen of mensen zonder geavanceerde computerkennis het toch kunnen begrijpen.


### Member / channel member / membership

| EN | NL |
| --- | --- |
| Could not find channel member when importing direct channel | Kan kanaallid niet vinden bij het importeren van persoonlijk berichtkanaal |
| No channel member found for that user ID and channel ID | Er zijn geen kanaalleden gevonden voor dit gebruikers-ID en kanaal-ID |
| Failed to update the user channels memberships | Kan de kanalen van de gebruiker waartoe deze behoort niet bijwerken |



### Mention / Mentions

| EN | NL |
| --- | --- |
Notify group members with a group mention | Groepsleden verwittigen bij een groepsvermelding |

Mention wordt vertaald als vermelding

### Message

Mattermost wordt gebruikt om `berichten' te versturen. Deze berichten kunnen worden samengesteld uit tekst en/of objecten zoals bestanden (afbeeldingen, documenten, emoticons, etc.).

Binnen Mattermost zijn er 3 soorten kanalen en dus 3 soorten berichten:

* Publieke berichten die in publieke kanalen worden gepubliceerd (publieke groepen)

* Privé-berichten zijn berichten die in privé-kanalen worden gepubliceerd (privé-groepen)

* Persoonlijke berichten die live aan één persoon zijn gericht, op een één-op-één-basis, of recentelijk in kleine groepen tot maximaal 5 personen. Meer algemeen bekend als Directe Berichten (of DM) op Twitter, binnen Mattermost is deze term echter anders. Inderdaad, op Twitter bevat de DM-functionaliteit zowel privé-groepsberichten als één-op-één-berichten. De functionaliteit is verdeeld in 2 verschillende functies binnen Mattermost.

Voor elk type van kanaal, Mattermost beschouwt 2 types van berichten: 

* berichten die de bovenliggende berichten zijn die een draadje (thread) thread starten;

* Antwoorden die de berichten zijn die antwoorden op een ouder bericht (post) in een draadje (thread).

Als een gebruiker antwoordt op een bericht zonder door de thread-functie te gaan die zich in de rechter zijbalk bevindt, wordt zijn bericht als een nieuw bericht beschouwd en wordt er een nieuwe thread geopend.

Je 'verzendt' een antwoord en 'publiceert' een bericht.

Stel een bericht op, post of antwoord.


| EN | NL |
| --- | --- |
| Invalid user ID for direct channel creation | Ongeldige gebruikers-ID voor het aanmaken van een privé-berichtkanaal |
| Failed to create direct channel | Fout bij het aanmaken van het privé-berichtkanaal |
| Failed to create group channel | Fout bij het aanmaken van een groepskanaal |
| Missing required direct channel property: members | De vereiste eigenschap voor een privé-berichtkanaal ontbreekt: leden |

[cf. Posted / posts / publication](#posted--posts--publication)

### Message export job

| EN | NL |
| --- | --- |
| Message export job BatchSize must be a positive integer | Bericht export job BatchSize moet een positief geheel getal zijn |

### Modify

| EN | NL |
| --- | --- |
| Update Email | E-mailadres bijwerken |

Hoewel we de neiging hebben om te vertalen als `updaten`, is het vertalen als `bijwerken` meestal eenvoudiger en correcter. We zullen de term `update' alleen gebruiken in de context van applicatie-updates, of het nu gaat om het server- of clientgedeelte (webapp, mobiel of desktopapplicatie).

Bij wijze van uitzondering kunnen we de term "update" gebruiken wanneer we het hebben over het verversen van de weergave van een beeld van de software, het updaten van een WebSocket-verbinding of wanneer we het hebben over SMTP/STARTTLS-verbindingen, hoewel in het laatste geval het gebruik van "upgrade" meer op zijn plaats lijkt.

### Mute

| EN | NL |
| --- | --- |
| mute | dempen |
| Could not mute channel {{.Channel}} as you are not a member. | Kon kanaal {{.Channel}} niet dempen omdat je geen lid bent. |

### Notifications push / mobile / desktop

| EN | NL |
| --- | --- |
| Desktop notifications | Bureaubladmeldingen |
| Invalid Channel Trigger Notify Prop for user. | Ongeldige kanaaltriggerberichteigenschap voor gebruiker. |
| Mobile Push | Mobiele meldingen |
| Encountered error when getting files for notification message, post_id=%v, err=%v | Fout bij het ontvangen van bestanden voor een notificatiebericht, post_id=%v, err=%v |
| Invalid Email Notify Prop value for user. | Ongeldige emailmeldingeigenschap voor gebruiker. |
| Turns off desktop, email and push notifications for the current channel or the channel specified. | Schakelt desktop, e-mail and mobiele meldingen uit voor het huidige kanaal of het gespecificeerde kanaal.

Desktop vertalen we als Bureaublad.
Notifications vertalen we als meldingen.
Push notifications vertalen we als push-meldingen.


Zorg ervoor dat u `melding` op de laatste plaats zet, zodat deze in overeenstemming is met termen als `push-meldingen' en `mobiele meldingen'. Dit is `e-mailmelding' en niet `melding per e-mail'.

Beschouw de termen `NotifyProps` en `Notify Props` als vergelijkbaar. Ze moeten worden vertaald. `notify_props` is een JSON-veld, dus dit vertalen we niet

### Optional

Voor de consistentie wordt aanbevolen om `Optioneel` te gebruiken in plaats van `Facultatief`.

### Override

| EN | NL |
| --- | --- |
| Enable integrations to override usernames | Integraties mogelijk maken om gebruikersnamen te overschrijven  |

### Packaged

| EN | NL |
| --- | --- |
| Cannot install prepackaged plugin | Kan geen voorverpakte plugin installeren |


### Parse / parser

| EN | NL |
| --- | --- |
| Elasticsearch indexing worker failed to parse the start time | Het Elasticsearch-aggregatiesysteem kon de starttijd niet interpreteren |
| Could not parse multipart form | Kan multipart formulier niet interpreteren. |

Niet vertalen door `analyseren`, ook al vertegenwoordigt deze meest voorkomende term de analyse van de grammaticale syntaxis van een taal, is `interpreteren`  correcter in dit geval.

### Permanently

Gebruik `definitief` in plaats van `permanent`.

### Permissions

| EN | NL |
| --- | --- |
| You do not have the appropriate permissions | Je hebt niet voldoende rechten. |
| Invalid permissions to regenerate the OAuth2 App Secret | Onvoldoende rechten om de OAuth2 App Secret te regeneren |
| Inappropriate channel permissions | Onvoldoende rechten vor dit kanaal |

`Rechten` heeft de voorkeur. `Machtigingen` en `Permissies` proberen we te vermijden.

In het geval van de machtigingscontext die ons betreft, hebben we het over machtigingen die te beperkend zijn en geen ongeldige toegangsmachtigingen (bijvoorbeeld UNIX 775-machtigingen in plaats van 770).

### Populate

| EN | NL |
| --- | --- |
| (Optional) The attribute in the AD/LDAP server used to populate the first name of users in Mattermost. When set, users cannot edit their first name, since it is synchronized with the LDAP server. When left blank, users can set their first name in Account Settings. | (Optioneel) Het attribuut in de AD/LDAP-server dat wordt gebruikt om de voornaam van gebruikers in Mattermost in te vullen. Wanneer deze is ingesteld, kunnen gebruikers hun voornaam niet bewerken, omdat deze gesynchroniseerd is met de LDAP-server. Wanneer deze optie leeg is, kunnen gebruikers hun voornaam instellen in Account Instellingen. |

### Purge

| EN | NL |
| --- | --- |
| Failed to purge channel indexes. | Fout bij het opschonen van de kanaalindexen. |


### Posted / posts / publication

| EN | NL |
| --- | --- |
| Unable to create /echo post, err=%v | Fout bij het aanmaken van een bericht via het commando /echo, err=%v |
| We couldn't find the pinned posts | Fout bij het ophalen van de vastgemaakte berichten |
| Failed to post update channel header message | Fout bij het wijzigen van de kanaalhoofding |
| Go to Post | Ga naar bericht |

Een 'post' of 'post' is een anglicisme. De algemene regel is om de vermelding `bericht` en het werkwoord `sturen` te behouden in plaats van `publiceren` ([cf. Bericht](#boodschap)).

In zeer zeldzame gevallen, zoals wanneer men expliciet het eerste bericht van een draadje(thread) wil identificeren, of wanneer men praat over een bericht dat gepubliceerd is door een integratie (een dienst van een derde partij die gekoppeld is aan Mattermost), heeft de term `publiceren` de voorkeur. Op dezelfde manier zullen we bij de globale kwalificatie van de berichten van een kanaal bijvoorbeeld de term 'berichten gepubliceerd in kanaal X' gebruiken.

Merk op dat voor `Go to Post`, aangezien deze tekst van toepassing is op alle soorten berichten, het niet alleen zichtbaar is voor berichten, maar voor alle berichten. Wees dus voorzichtig en lees zorgvuldig wanneer je probeert delen van de software te vertalen die gebruik maken van functies die u niet volledig begrijpt.

Wanneer een bericht wordt verstuurd door een gebruiker, wordt er gezegd dat het 'verzonden' is, wanneer het bericht wordt gepubliceerd door het systeem (bericht `join`/`leave`/change of header), wordt er gezegd dat het `gepubliceerd` is.

Voor vastgepinde berichten, hoewel `find` vertaald had kunnen worden als `vinden`, gebruiken we hier het werkwoord `ophalen` (zie [Krijgen / ophalen](#get-retrieve) hierboven) om de consistentie met andere foutmeldingen van dit type te waarborgen.

### Private message

[cf. Message](#message)

### Preview mode

Dit is de modus waarin Mattermost zich bevindt wanneer e-mailmeldingen niet zijn geactiveerd en daarom de configuratie niet volledig is voltooid. Om geen verwarring te creëren, gebruiken we de term "Demomodus".

### Preview features

Wanneer deze term wordt gebruikt om te praten over de te testen functionaliteiten, die nog niet stabiel zijn, soms bèta genoemd, zullen we de term "experimentele functionaliteiten" gebruiken.

### Privacy

Voor consistentie, vooral na de nieuwe regelgeving zoals de GDPR / GDPR, vertalen we door "privacy".

### Purpose

`Doel` wordt bijvoorbeeld vaak gebruikt voor het kanaalbeschrijvingsbericht. Het moet in deze context daarom worden vertaald als `beschrijving`.

### Rate limits

| EN | NL |
| --- | --- |
| Invalid memory store size for rate limit settings. Must be a positive number | Ongeldige geheugenopslaggrootte voor instellingen voor snelheidslimieten. Moet een positief getal zijn |
| Unable to initialize rate limiting. | Kan snelheidsbeperking niet initialiseren op de API. |

Vaak gebruikt om een ​​tarieflimiet aan te geven. In de context van Mattermost is dit een tarief om het aantal aanroepen van de Mattermost API te beperken dat de gebruiker bijvoorbeeld in een bepaalde tijd kan doen.

Hoewel het soms voorkomt in netwerkdomeinen, is dit concept van limiet niet gemakkelijk uit te drukken in het Nederlands. Laat het ons weten als je een geschiktere vertaling heeft.

### Reactions

| EN | NL |
| --- | --- |
| Reaction CreateAt property must be greater than the parent post CreateAt. | De eigenschap Reacie CreateAt  moet groter zijn dan de waarde van de bovenliggende eigenschap CreateAt. |
| Missing required Reaction property: create_at. | De vereiste reactie-eigenschap ontbreekt: created_at. |

Binnen Mattermost bepalen de reacties de +1 / -1 voor berichten. Net als andere berichtenoplossingen zoals Facebook Messenger, kunnen de reacties ook emoticons bevatten uit de standaardcollectie die bij Mattermost wordt geleverd, of zelfs gepersonaliseerde emoticons.

Reacties moeten daarom niet worden verward met reacties op een bericht. ([cf. Bericht](#bericht)).

### Refresh

| EN | NL |
| --- | --- |
| Refresh the app now | Ververs de app nu|

De term "verversen" wordt vaak gebruikt om het feit van het vernieuwen van de pagina van een webbrowser te bepalen. Soms wordt de gebruiker te vragen de Mattermost-applicatie te vernieuwen. In die zin betekent dit dat de gebruiker op een bepaalde knop moet drukken of de Mattermost-applicatie moet sluiten of opnieuw moet starten. In het laatste geval wordt de vertaling "vernieuwen" in plaats van "verversen" gebruikt.

### Retrieve

[cf. Get](#get--retrieve)

### Rollback

In het kader van databases en transacties gebruiken we "annuleer de transactie".

### Routes

| EN | NL |
| --- | --- |
| Initializing team API routes | Team API-routes initialiseren |
| Auth Endpoint: | Auth-eindpunt |

Hoewel deze berichten voornamelijk door technisch personeel moeten worden gezien en daardoor Engels kunnen spreken, verdient het de voorkeur om ze te vertalen.

Je moet een API zien als een boom die bestaat uit takken en bladeren. In de context van een API wordt elke tak `route` genoemd, elke tak (inclusief de allerlaatste die in blad is geplaatst) wordt een` knooppunt` genoemd. In het geval van een blad wordt dit specifieke knooppunt vaak het 'eindpunt' genoemd.

Gezien de locatie van dergelijke tekenreeksen binnen de software, verdient het de voorkeur om de oorspronkelijke Engelse term naast de Nederlandse term opnieuw te specificeren. Omdat deze kanalen voornamelijk worden gezien door technisch personeel en online gidsen en tutorials vaak in het Engels zijn, maakt het gebruik van de term in het Engels het daarom gemakkelijker om een ​​match te vinden.

Microsoft, als onderdeel van zijn .NET-platform, had een van de weinige technische documentatie volledig vertaald in het Frans. Een [artikel in 
We gebruiken de term `routing` alleen in dit geval:
| EN | NL |
| --- | --- |
| ASP.NET Routing | ASP.NET routing |


### Save

We geven de voorkeuraan de term `Opslaan` boven `Bewaren`

### Scheme

Pas op voor deze term, deze wordt op verschillende plaatsen gebruikt voor sterk uiteenlopende betekenissen.
* Het URI-schema is het protocol dat wordt gebruikt in een URI zoals http: //, https: //, wss: //, ftp: //, etc. In deze context gebruiken we "URI-protocol" of "URL-protocol".
* In het kader van geavanceerde toestemmingen en toegangsrechten is een schema een set standaardregels voor deelname aan een systeem, team of kanaal. In deze context gebruiken we, naast een zekere gelijkenis met de Engelse term "scheme", "toestemmingsschema" ("toestemmingsschema's" in het meervoud). Om regels en toegangsrechten in een organisatie toe te wijzen, is het inderdaad vaak nodig om een ​​plan of een organigram te maken, en dus een diagram. "Strategie" wordt hier verboden, ook al wordt het vaak gebruikt in Windows-omgevingen.

| EN | NL |
| --- | --- |
| The custom URL scheme {{.Scheme}} is invalid. Custom URL schemes must start with a letter and contain only letters, numbers, plus (+), period (.), and hyphen (-). | Het aangepaste URL-protocol {{.Scheme}} is ongeldig. Aangepaste URL-schema's moeten beginnen met een letter en alleen letters, cijfers, plus (+), punt (.) en streepje (-) bevatten. |
| The provided role is managed by a Scheme and therefore cannot be applied directly to a Channel Member | De toegekende rol wordt beheerd door een toegangsschema en kan hierdoor niet direct toegepast worden op een kanaallid. |
| New Team Override Scheme | Nieuwe aangepaste teamtoestemmingsschema  |

We gebruiken geen zinsconstructies die de term "override" letterlijk vertalen; dit resulteert in overdreven gecompliceerde zinnen.

### Slash commands

Dit zijn de commando's die u opgeeft wanneer u uw bericht start met een schuine streep in Mattermost. 'slash-commando's' heeft de voorkeur voor consistentie.

### SSO

| EN | NL |
| --- | --- |
| SSO / Single Sign-On | Single Sign-On (SSO) |

In technisch jargon is de term SSO of `Single Sign-On` gekend. We hebben niet direct een goed Nederlands alternatief. Suggesties zijn zeker welkom.

De vertaling  "vereenvoudigde authenticatie" is niet toegestaan.

### Support

| EN | NL |
| --- | --- |
| ID Loaded Push Notifications are not configured or supported on this server. | ID Loaded Pushmeldingen zijn niet geconfigureerd of ondersteund door deze server. |

`support` wordt vertaald als ondersteund.

### Sysadmin / system admin / team admin / channel admin

`Systeembeheerder` werd gekozen in het enkelvoud en `systeembeheerders` in het meervoud. De term `systeembeheerder` is in feite de term voor debeheerder van de systeemkwaliteit van de computer (alles wat niet gerelateerd is aan het netwerk). Het moet daarom niet worden opgevat als informatiesysteembeheerder/informatiesysteembeheerder. Bovendien hebben we het hier over één enkel systeem, dat van Mattermost.

Dezelfde logica is toegepast op team- en kanaalbeheerders (respectievelijk `teambeheerders` en `kanaalbeheerders`).

### Terms

| EN | NL |
| --- | --- |
| Please enter text for your Custom Terms of Service. | Voer de tekst in voor uw aangepaste servicevoorwaarden. |

Gebruik de term `aangepaste gebruiksvoorwaarden`. 

### Token / secret key

| EN | FR |
| --- | --- |
| Personal access token added to your account | Een persoonlijk toegangstoken werd toegevoegd aan jouw account |


* `token`: We gebruiken het woord token omdat we geen gepaste Nederlandse vertaling vinden. Voorstellen zijn zeker welkom.
* `secret key`: `geheime sleutel` als het gaat om een sleutel die wordt gebruikt in de zin van 'niet openbaar te maken sleutel', `privésleutel` in het geval dat er sprake is van een openbare sleutel of van asymmetrische versleuteling.

### Trigger

| EN | NL |
| --- | --- |
| A trigger word cannot begin with a / | Een triggerwoord kan niet beginnen met een  / |


### URL signing

| EN | NL |
| --- | --- |
| Additional options such as the URL signing key. Refer to your image proxy documentation to learn more about what options are supported. | Extra parameters zoals de URL-signeersleutel. Zie de beeldproxydocumentatie voor meer informatie over de ondersteunde instellingen. |

URL signing is een principe om bestanden op een webserver te beschermen tegen ongeautoriseerde toegang met behulp van een sleutel die soms in de URL zelf is gespecificeerd ([src.](https://www.limestonenetworks.com/support/knowledge-center/24/112/what_is_url_signing.html)). In de praktijk kunnen we dit vertalen als `URL-signeersleutel`.

### When true

We gebruiken hier "Indien ingeschakeld"

### Worker

| EN | NL |
| --- | --- |
| Elasticsearch indexing worker failed to parse the end time | Het Elasticsearch-aggregatiesysteem kon de eindtijd niet analyseren. |

Hoewel de term moet worden vertaald als `werknemer`, zal de term `systeem` worden gebruikt afhankelijk van de context.

