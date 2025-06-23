# Sistem Automatizat de Control pentru un Lift cu Două Etaje

Acest proiect reprezintă proiectarea și implementarea unui sistem automatizat de control pentru un lift cu două etaje (Parter și Etajul 1), utilizând mediul de programare și simulare **LOGO! Soft Comfort**. Sistemul este conceput pentru a asigura transportul eficient și sigur al persoanelor sau obiectelor între cele două niveluri, demonstrând capabilitățile unui automat programabil (PLC) în gestionarea unui sistem secvențial și interactiv.

---

## Scopul Proiectului

Scopul principal al acestui proiect este de a automatiza complet un sistem de lift cu două etaje, asigurând un transport eficient și sigur. Proiectul urmărește să demonstreze aplicabilitatea și eficiența automatelor programabile (PLC-uri) în gestionarea sistemelor complexe, secvențiale și interactive, punând accent pe siguranță și eficiență.

---

## Descriere Generală și Funcționalități

Sistemul automatizat de control al liftului a fost proiectat cu următoarele funcționalități cheie:

* **Controlul Mișcării Direcționate**: Asigură mișcarea liftului atât în sus, cât și în jos, prin activarea motoarelor corespunzătoare.
* **Detectarea și Memorarea Poziției**: Utilizează senzori dedicați (pentru Parter și Etajul 1) pentru a detecta și memora precis poziția actuală a liftului.
* **Gestionarea Cererilor de Apel**: Procesează eficient cererile de apel de la ambele etaje (butoane de apel), memorându-le și asigurând răspunsul liftului chiar și după eliberarea butonului.
* **Oprire Automată la Destinație**: Oprește automat motorul liftului la atingerea etajului solicitat.
* **Indicarea Vizuală a Stării**: Utilizează LED-uri (sau alte indicatoare luminoase) pentru a afișa starea curentă a liftului (poziție și direcție de deplasare).
* **Controlul Ușilor**: Gestionează deschiderea automată a ușilor la destinație și închiderea acestora după o anumită întârziere pentru a permite intrarea/ieșirea.
* **Secvențialitate Stabilă**: Asigură o succesiune logică și coerentă a tuturor operațiunilor, de la inițierea unei curse la oprirea la destinație și gestionarea automată a ușilor, contribuind la o funcționare fiabilă și sigură.

---

## Componente Tehnologice și Instrumente Utilizate

Acest proiect a fost realizat și simulat folosind:

* **LOGO! Soft Comfort**: Mediu de programare grafică și simulare (FBD - Function Block Diagram) utilizat pentru a dezvolta și testa logica de control a PLC-ului.
* **Automat Programabil (PLC)**: Proiectul se bazează pe principiile și capacitățile unui Automat Programabil, care primește intrări de la senzori și butoane și controlează ieșirile (motoare, LED-uri, uși).
* **Blocuri Funcționale LOGO!**: Logica a fost construită utilizând blocuri standard precum relee Set/Reset (SR), porți logice (AND, OR, NOT) și temporizatoare (Timers) pentru a implementa funcționalitățile necesare.

---

## Intrări și Ieșiri

Sistemul interacționează cu mediul prin următoarele intrări și ieșiri, simulate în LOGO! Soft Comfort:

| Intrare | Descriere             | Ieșire | Descriere         |
| :------ | :-------------------- | :----- | :---------------- |
| `I1`    | Senzor poziție Parter | `Q1`   | Motor Sus         |
| `I2`    | Senzor poziție Etaj 1 | `Q2`   | Motor Jos         |
| `I3`    | Buton Apel Parter     | `Q3`   | LED Poziție Parter |
| `I4`    | Buton Apel Etaj 1     | `Q4`   | LED Poziție Etaj 1 |
|         |                       | `Q5`   | LED Direcție Sus  |
|         |                       | `Q6`   | LED Direcție Jos  |
|         |                       | `Q7`   | Deschidere Ușă    |
|         |                       | `Q8`   | Închidere Ușă     |

---

## Logica Sistemului

Logica de control a fost dezvoltată sub formă de scheme cu blocuri funcționale (FBD) în LOGO! Soft Comfort. Aceasta gestionează:

* **Activarea Motoarelor**: Pe baza cererilor de apel și a poziției curente, se activează motorul de urcare sau cel de coborâre.
* **Memorarea Apelurilor**: Utilizarea releelor Set/Reset pentru a reține cererile de apel până când liftul ajunge la etajul respectiv.
* **Controlul Ușilor**: Temporizatoarele sunt folosite pentru a menține ușile deschise un anumit interval de timp după sosire și pentru a asigura închiderea acestora înainte de o nouă cursă.
* **Indicarea Stării**: LED-urile de poziție și direcție sunt activate corespunzător, oferind feedback vizual utilizatorului.
* **Interblocări**: Logica include interblocări pentru a preveni funcționarea simultană a motoarelor de urcare și coborâre, asigurând siguranța.

---

## Simulare și Validare

Întregul sistem a fost simulat extensiv în mediul LOGO! Soft Comfort. Procesul de simulare a permis:

* **Verificarea Corectitudinii Logice**: S-a asigurat că toate cererile de apel sunt gestionate corect și că liftul se deplasează la etajul solicitat.
* **Validarea Stabilității**: S-a confirmat că sistemul funcționează într-o manieră stabilă și previzibilă în diverse scenarii de utilizare, inclusiv apeluri multiple.
* **Testarea Secvențialității**: S-a verificat succesiunea corectă a operațiunilor (plecare, oprire, deschidere/închidere uși).

Simulările au demonstrat că obiectivele propuse au fost atinse și că sistemul este capabil să asigure o operare fiabilă a liftului.

---

## Rulare și Utilizare

Pentru a vizualiza logica și a rula simularea sistemului de control al liftului:

1.  **Descărcați fișierele**: Clonați repository-ul sau descărcați toate fișierele proiectului într-un director local.
2.  **Instalați LOGO! Soft Comfort**: Asigurați-vă că aveți instalat mediul de programare și simulare LOGO! Soft Comfort (versiunea V8 sau compatibilă) pe computerul dumneavoastră.
3.  **Deschideți proiectul**: Deschideți fișierul de proiect LOGO! (ex: `[NumeProiectLift].lsc`) direct din LOGO! Soft Comfort.
4.  **Rulați simularea**: Utilizați funcționalitățile de simulare din LOGO! Soft Comfort (iconița cu ochelari) pentru a testa comportamentul sistemului. Puteți activa intrările (butoanele de apel `I3`, `I4`, senzorii `I1`, `I2`) și observa răspunsul ieșirilor (motoare, LED-uri, uși).

---

## Capturi

Mai jos sunt câteva capturi de ecran din mediul LOGO! Soft Comfort, ilustrând logica de control și simularea sistemului.

**Diagrama logică principală:**
![Diagrama logică principală](assets/logica_control_lift.png)

**Exemplu de simulare (Liftul ajunge la Parter și deschide ușa):**
![Simulare lift ajuns la etaj](assets/simulare_lift_rulare.png)

---

##Realizat de

Proiect realizat de [bogdanch7](https://github.com/bogdanch7)

An universitar 2024–2025

---

##Licență

Acest proiect este creat pentru uz educațional.
