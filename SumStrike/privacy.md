# Privatlivspolitik for Sum Strike

**Senest opdateret: 4. september 2026**

Sum Strike (“appen”, “vi”, “os”) er et matematisk straffesparksspil til iPhone. Denne politik forklarer, hvilke oplysninger der behandles, hvordan de indsamles, hvad de bruges til, hvem der har adgang, hvor længe de opbevares, og hvordan du kan få dem slettet.

Politikken er skrevet, så den opfylder [Apples App Store Review Guidelines 5.1.1](https://developer.apple.com/app-store/review/guidelines/#privacy) og [App Privacy Details](https://developer.apple.com/app-store/app-privacy-details/). Den engelske tekst nedenfor er den samme politik.

Hvis du ikke kan acceptere vilkårene, skal du ikke bruge appen.

---

## 1. Dataansvarlig

**Thomas Kramer Nielsen**  
Køge, Danmark  
E-mail: [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk)

App-navn: **Sum Strike**  
Bundle-id: `thomaskramer.Sum-Strike`

Vi driver ikke en egen server til Sum Strike. Det, der forlader enheden, går kun til **Apple** (App Store-køb og — hvis du slår det til — Game Center) og **RevenueCat** (abonnementstatus).

---

## 2. Kort overblik

| Vi gør | Vi gør ikke |
| --- | --- |
| Gemmer spil, fremgang og forældrerapport **på enheden** | Viser reklamer |
| Bruger **RevenueCat** til at se, om et abonnement er aktivt | Bruger analyseværktøjer, crash-reportere eller trackere fra tredjepart |
| Lader Apple håndtere **betaling** og valgfrit **Game Center** | Indsamler e-mail, telefonnummer, CPR, foto, kontakter eller placering |
| Sætter en **forældrelås** foran køb og forældrerapport | Tracker dig på tværs af andre firmaers apps og websites (ingen ATT-prompt) |
| Tillader **Familiedeling** af abonnementet | Sælger, udlejer eller bytter personoplysninger |
| Bruger kun **faste emotes** online — ingen fri tekst | Kræver login for at spille |

---

## 3. Hvilke oplysninger der behandles

### 3.1 Data der bliver på enheden (sendes ikke til os)

Følgende gemmes lokalt med **SwiftData** og **UserDefaults**. Vi har ingen kopi på en server, vi styrer.

**Profil og indstillinger**

- Valgfrit visningsnavn og navn på den anden spiller i pass-and-play
- Sprog, tilgængelighed (fx dysleksifont, reduceret bevægelse, skjul timer, stilladser), lyd og haptik
- Kosmetik (trøje, støvler m.m.) og mønter, som **kun** tjenes ved at spille — de kan ikke købes

**Læring og spil**

- Svar på opgaver: opgavetekst, rigtigt/forkert, valgt distraktor, svartid, om VAR-tjek blev brugt, spiltilstand
- Niveau pr. emne (Elo-lignende rating), dagsprøver og trend til forældrerapporten
- Karriere, kamphistorik, observationer om målmænd, uafsluttet kamp
- Tid brugt i appen pr. uge (til forældrerapporten)
- Midlertidige nøgler til online-runder (fx besvarede spørgsmål og målmandens forseglede valg)

**Formål:** at appen virker — at huske fremgang, tilpasse sværhedsgrad, vise forældrerapporten og gennemføre en kamp.

**Knyttet til personen:** kun på enheden. Vi kan ikke læse det.

**Brugt til tracking:** nej.

**Sletning:** Indstillinger → nulstil al data, eller afinstaller appen. Data kan også ligge i enhedens almindelige iCloud-/computer-backup, hvis det er slået til på telefonen.

En forælder kan **eksportere en PDF** af forældrerapporten via iOS’ deleark. Det sker kun, hvis forælderen selv trykker. Vi får ikke en kopi. Den, du deler med (fx Mail eller Beskeder), behandler filen efter deres egne regler.

### 3.2 Køb og abonnement (Apple + RevenueCat)

Appen har ét medlemskab (`sum_strike_pro`) som månedligt abonnement, årligt abonnement eller livstidskøb. Der er ingen mikrotransaktioner og ingen reklamer.

**Hvad der behandles**

- **Købshistorik:** produkt, dato, status, fornyelse, udløb, Familiedeling — nok til at afgøre, om medlemskabet er aktivt, og til at gendanne køb
- **Bruger-id:** et **anonymt** id, som RevenueCat udsteder. Appen opretter **ingen konto** og sender **ikke** barnets navn til RevenueCat
- **Tekniske oplysninger**, som SDK’et bruger til at levere tjenesten: enhedstype, styresystem og den IP-adresse, der følger med en HTTPS-forbindelse

**Vi behandler ikke** kortnummer, Apple-id eller adgangskode. Betalingen kører hos Apple.

**Sådan indsamles det:** Når appen starter, eller når en voksen (efter forældrelåsen) køber, gendanner eller administrerer abonnementet. RevenueCat-SDK’et taler med RevenueCats servere; StoreKit taler med Apple.

**Formål:** App-funktionalitet — at låse medlemskab op, gendanne køb, vise fornyelsesdato og lade Familiedeling virke. Ikke reklame, ikke analyse af barnets spil, ikke tracking.

**Knyttet til personen:** Ja, til det anonyme RevenueCat-id og — hos Apple — til det Apple-id, der betaler (typisk en forælder). Ikke til barnets visningsnavn.

**Brugt til tracking:** Nej. Vi indsamler ikke IDFA og viser ikke App Tracking Transparency-prompten.

**Tredjeparter:** Apple og RevenueCat, Inc. RevenueCat opbevarer data hos Amazon Web Services i USA.

### 3.3 Game Center (valgfrit, Apple)

Game Center er **ikke** påkrævet. Træning, karriere og pass-and-play virker uden. Online-kamp og rangliste kræver, at spilleren er logget ind i Game Center.

**Hvad Apple behandler** (ikke os), når Game Center er slået til:

- Game Center-kaldenavn, avatar og spiller-id
- Ranglistescore: **mål i alt** og **mål i indeværende måned** (`sumstrike.goals.alltime`, `sumstrike.goals.monthly`)
- Tur-baseret kampedata: stilling, strafespark, forseglet målmandsvalg, faste emotes, hvem der har tur

**Sådan indsamles det:** Kun efter Apples egen Game Center-login. Appen ærer Skærmtid: multiplayer kan være slået fra, og modstanderens navn/avatar kan skjules.

**Formål:** App-funktionalitet — online-kamp og rangliste.

**Knyttet til personen:** Hos Apple, under Game Center-kontoen.

**Brugt til tracking:** Nej, ikke af os.

**Ingen chat.** Online findes kun et lille sæt faste emotes. Der er intet fritekstfelt.

Apple beskriver selv behandlingen i [Game Center & Privacy](https://www.apple.com/legal/privacy/data/en/game-center/) og [Apples privatlivspolitik](https://www.apple.com/legal/privacy/).

### 3.4 Det vi ikke indsamler

- Navn, e-mail, telefon eller adresse som profilfelter (et valgfrit visningsnavn bliver **på enheden**)
- Præcis eller grov placering
- Helbred, Fitness eller HealthKit
- Kamera, fotos, mikrofon, kontakter eller kalender
- Reklame-id (IDFA) eller fingerprinting
- Betalingskort
- Analyse af, hvordan barnet spiller, sendt til os eller til et analysefirma
- Brugerindhold, der kan identificere et barn over nettet (ingen tegninger, fotos eller chat, der uploades)

Hvis du skriver til os på e-mail, får vi den adresse og den tekst, du sender. Det bruger vi kun til at svare.

---

## 4. Sådan bruger vi oplysningerne

| Formål | Hvad | Retsgrundlag (GDPR) |
| --- | --- | --- |
| Få appen til at virke | Lokal fremgang, opgaver, karriere, indstillinger | Art. 6(1)(b) aftale / art. 6(1)(f) berettiget interesse i at levere spillet |
| Medlemskab | Købshistorik og anonymt id via Apple og RevenueCat | Art. 6(1)(b) købsaftale |
| Online og rangliste | Game Center, hvis brugeren logger ind | Art. 6(1)(a) samtykke via Apples login / art. 6(1)(b) den valgte funktion |
| Forældrerapport | Lokale svar og tid på opgaven — vises kun bag forældrelåsen | Art. 6(1)(f) og forældres ansvar for barnet |
| Svar på henvendelser | E-mail, du selv sender | Art. 6(1)(b) eller 6(1)(f) |
| Lovkrav | Bogføring af salg hos Apple; eventuelle pålæg | Art. 6(1)(c) |

Vi bruger **ikke** oplysninger til reklame, profilering til markedsføring, videresalg eller til at bygge en identitet på tværs af apps.

Data indsamlet til ét formål genbruges ikke til et andet uden nyt, lovligt grundlag — i tråd med Apples regel 5.1.2.

---

## 5. Tredjeparter og samme beskyttelse

Vi deler kun det, der er nødvendigt for de funktioner, du (eller en forælder) bruger. Vi bekræfter, at de tredjeparter, der behandler oplysninger i forbindelse med appen, er forpligtet til at beskytte dem mindst på niveau med denne politik og med Apples retningslinjer.

### 5.1 Apple

App Store-køb, StoreKit, Familiedeling, Game Center og eventuelle crash-rapporter, du selv har slået til under iOS’ indstilling “Del med appudviklere”.

Privatlivspolitik: [https://www.apple.com/legal/privacy/](https://www.apple.com/legal/privacy/)  
Game Center: [https://www.apple.com/legal/privacy/data/en/game-center/](https://www.apple.com/legal/privacy/data/en/game-center/)

### 5.2 RevenueCat, Inc.

Abonnement og entitlement. RevenueCat er **databehandler** for slutbrugerdata; vi er dataansvarlige. De må bruge oplysningerne til at levere tjenesten til os — ikke til at reklamere over for barnet.

Privatlivspolitik: [https://www.revenuecat.com/privacy](https://www.revenuecat.com/privacy)

Vi integrerer **ikke** andre SDK’er (ingen reklamenetværk, Firebase, Amplitude, Crashlytics eller tilsvarende).

---

## 6. Overførsel uden for EU/EØS

RevenueCat opbevarer data i USA (AWS). Apple behandler data efter egne vilkår, som kan indebære behandling uden for EU.

Hvor GDPR kræver det, sker overførslen på grundlag af EU-Kommissionens standardkontraktbestemmelser og de garantier, leverandørerne beskriver i deres politikker. Du kan spørge os på [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk), hvis du vil have flere detaljer.

---

## 7. Opbevaring og sletning

| Data | Hvor længe | Sådan sletter du |
| --- | --- | --- |
| Lokal spildata | Indtil du nulstiller eller afinstallerer | **Indstillinger → nulstil** i appen, eller slet appen |
| RevenueCat anonymt id og købsstatus | Så længe medlemskabet skal kunne gendannes, derefter efter RevenueCats opbevaring | Skriv til os; vi beder RevenueCat slette slutbrugerposten. Selve købet ligger hos Apple |
| Game Center | Så længe Game Center-kontoen findes | Apple: Indstillinger → Game Center, eller [privacy.apple.com](https://www.apple.com/privacy/) |
| E-mail du sender os | Så længe sagen kræver det, typisk op til 12 måneder | Bed os slette tråden |

Afinstallation **opsiger ikke** et abonnement. Det gøres i iOS under Apple-id → Abonnementer.

Du kan trække samtykke til Game Center tilbage ved at logge ud af Game Center. Appen virker stadig offline.

---

## 8. Dine rettigheder (GDPR og tilsvarende)

Afhængigt af hvor du bor, kan du have ret til indsigt, berigtigelse, sletning, begrænsning, dataportabilitet, indsigelse og til at klage.

- **Lokale data:** brug nulstil i appen. Vi kan ikke udlevere det, vi ikke har.
- **Køb:** Apple-id → Købshistorik / Abonnementer. Gendan køb ligger i appens indstillinger og er **ikke** bag forældrelåsen, fordi det ikke koster penge.
- **Øvrigt:** skriv til [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk). Vi svarer som udgangspunkt inden for **30 dage**.

Klager i Danmark kan sendes til **Datatilsynet** ([datatilsynet.dk](https://www.datatilsynet.dk)). I andre EØS-lande til det lokale tilsyn. I Californien m.fl. kan CCPA/CPRA give ret til at vide, slette og sige nej til “salg” eller “deling” til reklame — vi sælger og deler ikke data til reklame.

Vi diskriminerer ikke for, at du bruger dine rettigheder.

---

## 9. Børn

Sum Strike er et **undervisningsspil**. Børn kan spille det; køb og forældrerapport ligger bag en **forældrelås** (et gangestykke, en voksen kan, et lille barn typisk ikke).

Forældrelåsen er **ikke** det samme som et verificeret forældresamtykke efter COPPA eller GDPR artikel 8. Den stopper barnet fra at nå en betalingsskærm. Den indsamler ikke barnets personoplysninger til os.

**Vi indsamler ikke bevidst personoplysninger fra børn under 13 år (COPPA) / under 13 år i Danmark (databeskyttelsesloven § 6) ud over det, der er nødvendigt for at levere appen:**

- Læringsdata bliver **på enheden**
- Køb går via **forælderens Apple-id** og et **anonymt** RevenueCat-id — ikke barnets navn
- Game Center er **valgfrit** og styres af Apple, inklusive Skærmtid for børnekonti (ingen fritekst, begrænset multiplayer)

I EU er behandlingsgrundlaget for et barns brug af informationssamfundstjenester som udgangspunkt forældres samtykke, indtil barnet er 13 år i Danmark. Ved at installere appen og — hvis I vil — købe medlemskab, handler forælderen på barnets vegne.

Vi overholder i øvrigt gældende regler om børns privatliv, herunder COPPA og GDPR, i det omfang de gælder.

Hvis du mener, vi alligevel ligger inde med et barns personoplysninger, så skriv. Vi sletter det, vi kan slette.

Appen ligger i kategorien **Educational Games**. Den er **ikke** indsendt i App Store’s Kids Category. Metadata bruger derfor ikke formuleringer forbeholdt den kategori.

---

## 10. Tracking (App Tracking Transparency)

Appen tracker **ikke** brugere på tværs af andre virksomheders apps eller websites. Der vises **ingen** ATT-dialog, og `NSUserTrackingUsageDescription` bruges ikke.

---

## 11. Sikkerhed

Lokal data ligger i iOS’ sandkasse (SwiftData/UserDefaults). Netværk til Apple og RevenueCat kører over HTTPS/TLS. Ingen metode er 100 % sikker.

---

## 12. Abonnement i korte træk

Priser, periode og eventuel prøveperiode vises på købsskærmen og i App Store og kan variere efter land.

1. Betaling trækkes på **Apple-id’et**. Vi ser ikke kortet.
2. Løbende abonnementer **fornyes automatisk**, medmindre de opsiges mindst 24 timer før periodens udløb.
3. Opsigelse: **Indstillinger → [dit navn] → Abonnementer**, eller Kundecenter i appen (bag forældrelåsen). At slette appen opsiger **ikke**.
4. Refusion følger **Apples** regler.
5. **Gendan køb** findes i indstillingerne.
6. Medlemskabet kan deles med **Familiedeling**, når det er slået til på produktet.
7. Køb er underlagt [Apple Media Services-vilkår](https://www.apple.com/legal/internet-services/itunes/) og [Apples Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/). Ved modstrid gælder Apples vilkår for betaling, fornyelse og refusion.

---

## 13. Ændringer

Vi kan opdatere denne politik og ændre datoen øverst. Væsentlige ændringer kan vises i appen eller på App Store-siden. Fortsat brug efter en opdatering betyder, at du er orienteret om den nye tekst.

---

## 14. Kontakt

**Udvikler:** Thomas Kramer Nielsen  
**App:** Sum Strike  
**Bundle-id:** `thomaskramer.Sum-Strike`  
**E-mail:** [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk)

**Politik-URL (til App Store Connect og appen):**  
https://github.com/thomaskramerdk/policy/blob/main/SumStrike/privacy.md

Skriv “Sum Strike / privatliv” i emnefeltet, og nævn gerne omtrentlig dato og land, hvis du beder om sletning af en købspost.

---

## 15. App Privacy-label (App Store Connect)

Det, der **forlader enheden**, og derfor skal afspejles i App Privacy:

| Datatype (Apple) | Indsamles | Knyttet til identitet | Tracking | Formål |
| --- | --- | --- | --- | --- |
| Purchase History | Ja (RevenueCat + Apple) | Ja (anonymt app-bruger-id / Apple-id hos Apple) | Nej | App Functionality |
| User ID | Ja (RevenueCats anonyme id) | Ja (pseudonymt) | Nej | App Functionality |
| Product Interaction | Kun via Game Center, hvis brugeren logger ind | Hos Apple | Nej | App Functionality |

**Ikke** indsamlet af os i Apples forstand: Location, Contact Info, Health, Sensitive Info, Contacts, Browsing History, Search History, Advertising Data, Usage Data til analyse, Diagnostics til os, Other Data Types til os.

Data der **kun** ligger på enheden (opgavesvar, navne, indstillinger) opfylder Apples kriterier for, at de **ikke** behøver stå på produktlabelen, så længe de ikke sendes af sted og ikke bruges til tracking. De er alligevel beskrevet i § 3.1, så politikken er dækkende.

---

# Privacy Policy for Sum Strike

**Last updated: 4 September 2026**

Sum Strike (“the App”, “we”, “us”) is a maths penalty-shootout game for iPhone. This policy explains what information is processed, how it is collected, how it is used, who can access it, how long it is kept, and how you can have it deleted.

It is written to meet [Apple App Store Review Guideline 5.1.1](https://developer.apple.com/app-store/review/guidelines/#privacy) and [App Privacy Details](https://developer.apple.com/app-store/app-privacy-details/). The Danish text above is the same policy.

If you do not agree, do not use the App.

---

## 1. Data controller

**Thomas Kramer Nielsen**  
Køge, Denmark  
Email: [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk)

App name: **Sum Strike**  
Bundle identifier: `thomaskramer.Sum-Strike`

We do not run our own backend for Sum Strike. Anything that leaves the device goes only to **Apple** (App Store purchases and, if you switch it on, Game Center) and **RevenueCat** (subscription status).

---

## 2. Snapshot

| We do | We do not |
| --- | --- |
| Store play, progress and the parent report **on the device** | Show ads |
| Use **RevenueCat** to know whether a membership is active | Use third-party analytics, crash reporters or trackers |
| Let Apple handle **payment** and optional **Game Center** | Collect email, phone, national ID, photos, contacts or location |
| Put a **parental gate** in front of purchases and the parent report | Track you across other companies’ apps or websites (no ATT prompt) |
| Allow **Family Sharing** of the membership | Sell, rent or trade personal data |
| Use **fixed emotes** only online — no free text | Require an account to play |

---

## 3. Information we process

### 3.1 Data that stays on the device (not sent to us)

The following is stored locally with **SwiftData** and **UserDefaults**. We do not hold a copy on a server we control.

**Profile and settings**

- Optional display name and the other player’s name in pass-and-play
- Language, accessibility (e.g. dyslexia font, reduced motion, hide timer, scaffolds), sound and haptics
- Cosmetics (kit, boots, etc.) and coins, which are **earned by playing only** — they cannot be bought

**Learning and play**

- Question answers: stem, right/wrong, chosen distractor, response time, whether a VAR check was used, game mode
- Per-topic level (Elo-style rating), daily samples and trend for the parent report
- Career, match history, keeper observations, unfinished match
- Time on task per week (for the parent report)
- Temporary keys for online rounds (answered questions and the keeper’s sealed choice)

**Purpose:** App functionality — remembering progress, adapting difficulty, showing the parent report and finishing a match.

**Linked to the user:** only on the device. We cannot read it.

**Used for tracking:** no.

**Deletion:** Settings → reset all data, or uninstall the App. The data may also sit in the device’s normal iCloud/computer backup if that is enabled.

A parent can **export a PDF** of the parent report through the iOS share sheet. That happens only if the parent taps share. We do not receive a copy. Whoever you share with (Mail, Messages, etc.) handles the file under their own rules.

### 3.2 Purchases and subscription (Apple + RevenueCat)

The App has one membership (`sum_strike_pro`) as a monthly subscription, yearly subscription or lifetime purchase. There are no microtransactions and no ads.

**What is processed**

- **Purchase history:** product, date, status, renewal, expiry, Family Sharing — enough to know whether membership is active and to restore purchases
- **User ID:** an **anonymous** identifier issued by RevenueCat. The App creates **no account** and does **not** send the child’s name to RevenueCat
- **Technical information** the SDK needs to provide the service: device type, operating system, and the IP address that accompanies an HTTPS connection

**We do not process** card numbers, Apple ID or password. Payment runs on Apple’s side.

**How it is collected:** When the App launches, or when an adult (after the parental gate) buys, restores or manages the subscription. The RevenueCat SDK talks to RevenueCat’s servers; StoreKit talks to Apple.

**Purpose:** App Functionality — unlocking membership, restoring purchases, showing the renewal date and making Family Sharing work. Not advertising, not analytics of the child’s play, not tracking.

**Linked to the user:** Yes, to the anonymous RevenueCat ID and — at Apple — to the Apple ID that pays (typically a parent). Not to the child’s display name.

**Used for tracking:** No. We do not collect IDFA and do not show the App Tracking Transparency prompt.

**Third parties:** Apple and RevenueCat, Inc. RevenueCat stores data on Amazon Web Services in the United States.

### 3.3 Game Center (optional, Apple)

Game Center is **not** required. Training, career and pass-and-play work without it. Online matches and leaderboards require the player to be signed in to Game Center.

**What Apple processes** (not us) when Game Center is on:

- Game Center nickname, avatar and player ID
- Leaderboard scores: **goals all-time** and **goals this month** (`sumstrike.goals.alltime`, `sumstrike.goals.monthly`)
- Turn-based match data: score, penalties, sealed keeper choice, fixed emotes, whose turn it is

**How it is collected:** Only after Apple’s own Game Center sign-in. The App honours Screen Time: multiplayer can be switched off, and the opponent’s name/avatar can be hidden.

**Purpose:** App Functionality — online play and leaderboards.

**Linked to the user:** At Apple, under the Game Center account.

**Used for tracking:** No, not by us.

**No chat.** Online play uses a small set of fixed emotes. There is no free-text field.

Apple describes this in [Game Center & Privacy](https://www.apple.com/legal/privacy/data/en/game-center/) and [Apple’s Privacy Policy](https://www.apple.com/legal/privacy/).

### 3.4 What we do not collect

- Name, email, phone or address as profile fields (an optional display name **stays on the device**)
- Precise or coarse location
- Health, Fitness or HealthKit
- Camera, photos, microphone, contacts or calendar
- Advertising identifier (IDFA) or fingerprinting
- Payment cards
- Analytics of how the child plays, sent to us or to an analytics vendor
- User content that could identify a child over the network (no drawings, photos or chat uploaded)

If you email us, we receive the address and the text you send. We use that only to reply.

---

## 4. How we use the information

| Purpose | What | Legal basis (GDPR) |
| --- | --- | --- |
| Make the App work | Local progress, questions, career, settings | Art. 6(1)(b) contract / art. 6(1)(f) legitimate interest in providing the game |
| Membership | Purchase history and anonymous ID via Apple and RevenueCat | Art. 6(1)(b) purchase contract |
| Online and leaderboards | Game Center, if the user signs in | Art. 6(1)(a) consent via Apple’s sign-in / art. 6(1)(b) the chosen feature |
| Parent report | Local answers and time on task — shown only behind the parental gate | Art. 6(1)(f) and parental responsibility |
| Support | Email you send us | Art. 6(1)(b) or 6(1)(f) |
| Legal duties | Apple’s records of sales; any lawful request | Art. 6(1)(c) |

We do **not** use information for advertising, marketing profiles, resale, or to build an identity across apps.

Data collected for one purpose is not reused for another without a new lawful basis — consistent with Apple guideline 5.1.2.

---

## 5. Third parties and equal protection

We share only what is needed for the features you (or a parent) use. We confirm that third parties who process information in connection with the App are required to protect it to the same or equal standard as this policy and as required by Apple’s Guidelines.

### 5.1 Apple

App Store purchases, StoreKit, Family Sharing, Game Center, and any crash reports you have opted into under iOS “Share with App Developers”.

Privacy policy: [https://www.apple.com/legal/privacy/](https://www.apple.com/legal/privacy/)  
Game Center: [https://www.apple.com/legal/privacy/data/en/game-center/](https://www.apple.com/legal/privacy/data/en/game-center/)

### 5.2 RevenueCat, Inc.

Subscription and entitlement. RevenueCat is a **processor** of end-user data; we are the controller. They may use the information to provide the service to us — not to advertise to the child.

Privacy policy: [https://www.revenuecat.com/privacy](https://www.revenuecat.com/privacy)

We do **not** integrate any other SDK (no ad network, Firebase, Amplitude, Crashlytics or similar).

---

## 6. Transfers outside the EU/EEA

RevenueCat stores data in the United States (AWS). Apple processes data under its own terms, which may include processing outside the EU.

Where GDPR requires it, the transfer relies on the European Commission’s Standard Contractual Clauses and the safeguards the providers describe in their policies. Email [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk) if you want more detail.

---

## 7. Retention and deletion

| Data | How long | How to delete |
| --- | --- | --- |
| Local game data | Until you reset or uninstall | **Settings → reset** in the App, or delete the App |
| RevenueCat anonymous ID and purchase status | For as long as membership must be restorable, then per RevenueCat’s retention | Email us; we will ask RevenueCat to delete the end-user record. The purchase itself remains with Apple |
| Game Center | For as long as the Game Center account exists | Apple: Settings → Game Center, or [privacy.apple.com](https://www.apple.com/privacy/) |
| Email you send us | For as long as the request requires, typically up to 12 months | Ask us to delete the thread |

Uninstalling the App does **not** cancel a subscription. Cancel under Apple ID → Subscriptions.

You can withdraw Game Center consent by signing out of Game Center. The App still works offline.

---

## 8. Your rights (GDPR and similar)

Depending on where you live, you may have rights to access, rectify, erase, restrict, port, object, and complain.

- **Local data:** use reset in the App. We cannot hand over what we do not have.
- **Purchases:** Apple ID → Purchase History / Subscriptions. Restore Purchases is in the App’s settings and is **not** behind the parental gate, because it spends nothing.
- **Anything else:** email [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk). We aim to reply within **30 days**.

Complaints in Denmark go to **Datatilsynet** ([datatilsynet.dk](https://www.datatilsynet.dk)); elsewhere in the EEA to your local authority. In California and similar US states, CCPA/CPRA may add rights to know, delete and opt out of “sale” or “sharing” for advertising — we do not sell or share data for advertising.

We will not discriminate against you for exercising your rights.

---

## 9. Children

Sum Strike is an **educational game**. Children can play it; purchases and the parent report sit behind a **parental gate** (an arithmetic check an adult passes and a young child typically does not).

The parental gate is **not** verifiable parental consent under COPPA or GDPR Article 8. It stops a child reaching a payment screen. It does not collect the child’s personal data for us.

**We do not knowingly collect personal information from children under 13 (COPPA) / under 13 in Denmark (Danish Data Protection Act § 6) beyond what is needed to provide the App:**

- Learning data **stays on the device**
- Purchases go through the **parent’s Apple ID** and an **anonymous** RevenueCat ID — not the child’s name
- Game Center is **optional** and run by Apple, including Screen Time for child accounts (no free text, restricted multiplayer)

In the EU, the lawful basis for a child’s use of information-society services is generally parental consent until the child is 13 in Denmark. By installing the App and — if you choose — buying membership, the parent acts on the child’s behalf.

We otherwise comply with applicable children’s privacy laws, including COPPA and GDPR, to the extent they apply.

If you believe we nonetheless hold a child’s personal data, email us. We will delete what we can delete.

The App is categorised as **Educational Games**. It is **not** submitted in the App Store Kids Category, so metadata does not use wording reserved for that category.

---

## 10. Tracking (App Tracking Transparency)

The App does **not** track users across other companies’ apps or websites. There is **no** ATT dialog, and `NSUserTrackingUsageDescription` is not used.

---

## 11. Security

Local data sits in the iOS sandbox (SwiftData/UserDefaults). Network calls to Apple and RevenueCat use HTTPS/TLS. No method is 100% secure.

---

## 12. Subscriptions in brief

Prices, period and any trial are shown on the paywall and on the App Store and may vary by country.

1. Payment is charged to the **Apple ID**. We never see the card.
2. Recurring subscriptions **renew automatically** unless cancelled at least 24 hours before the period ends.
3. Cancel: **Settings → [your name] → Subscriptions**, or Customer Center in the App (behind the parental gate). Deleting the App does **not** cancel.
4. Refunds follow **Apple’s** rules.
5. **Restore Purchases** is in Settings.
6. Membership can be shared with **Family Sharing** when enabled on the product.
7. Purchases are subject to the [Apple Media Services Terms](https://www.apple.com/legal/internet-services/itunes/) and [Apple’s Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/). If this summary conflicts with Apple’s terms, **Apple’s terms control** payment, renewal and refunds.

---

## 13. Changes

We may update this policy and change the date at the top. Material changes may appear in the App or on the App Store listing. Continued use after an update means you have been informed of the new text.

---

## 14. Contact

**Developer:** Thomas Kramer Nielsen  
**App:** Sum Strike  
**Bundle identifier:** `thomaskramer.Sum-Strike`  
**Email:** [thomas@thomas-kramer.dk](mailto:thomas@thomas-kramer.dk)

**Policy URL (for App Store Connect and in-app):**  
https://github.com/thomaskramerdk/policy/blob/main/SumStrike/privacy.md

Put “Sum Strike / privacy” in the subject line, and mention an approximate date and country if you are asking us to delete a purchase record.

---

## 15. App Privacy label (App Store Connect)

What **leaves the device**, and therefore belongs on the App Privacy answers:

| Data type (Apple) | Collected | Linked to identity | Tracking | Purpose |
| --- | --- | --- | --- | --- |
| Purchase History | Yes (RevenueCat + Apple) | Yes (anonymous app user ID / Apple ID at Apple) | No | App Functionality |
| User ID | Yes (RevenueCat anonymous ID) | Yes (pseudonymous) | No | App Functionality |
| Product Interaction | Only via Game Center if the user signs in | At Apple | No | App Functionality |

**Not** collected by us in Apple’s sense: Location, Contact Info, Health, Sensitive Info, Contacts, Browsing History, Search History, Advertising Data, Usage Data for analytics, Diagnostics to us, Other Data Types to us.

Data that **only** lives on the device (answers, names, settings) meets Apple’s criteria for **not** having to appear on the product label, provided it is not sent off-device and is not used for tracking. It is still described in § 3.1 so the policy is complete.

---

_This Privacy Policy applies to the Sum Strike mobile application (bundle id `thomaskramer.Sum-Strike`). It is not legal advice._
