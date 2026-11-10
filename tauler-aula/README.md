# Tauler d'aula

Eina web per fer grups d'alumnes a l'atzar a partir d'una llista copiada de Google Sheets, situar-los en un plànol d'aula i recollir-ne observacions amb un semàfor. Els grups surten equilibrats i es poden retocar a mà. Després es poden descarregar en una imatge o en un PDF per imprimir.

👉 **Fes-la servir aquí:** **https://jchoucin-creator.github.io/gestioaula/tauler-aula/**

---

## Privacitat

- Els noms **només existeixen a la pestanya del navegador** on els enganxes.
- **No es desen enlloc**: ni al navegador, ni a GitHub, ni a cap servidor. En tancar o recarregar la pàgina, desapareixen.
- L'única cosa que el navegador recorda és el **banc de rúbriques**, que no conté cap dada de l'alumnat.
- **No s'envien a cap servidor.** Tot el càlcul es fa a l'ordinador de qui fa servir l'eina.
- La pàgina només carrega dos recursos externs: les tipografies de Google Fonts i la llibreria [jsPDF](https://github.com/parallax/jsPDF), que genera el PDF. Cap dels dos rep els noms.

---

## Ús bàsic

1. A Google Sheets, selecciona la columna dels noms i copia-la (Ctrl+C).
2. Enganxa-la al quadre **Llista de noms**.
3. Tria com vols fer els grups:
   - **Nombre de grups**: per exemple, 6 grups.
   - **Persones per grup**: per exemple, grups de 4. Si no surt exacte, tries si algun grup té una persona més o una de menys.
4. Prem **Fes els grups**. Cada cop que el prems, es fa un repartiment nou.

### Presentació

Al bloc **Presentació** hi ha el **Títol** i la **Classe** (nivell i grup, per exemple «1r ESO B»). La classe surt a la línia de dalt dels grups, a la imatge, als PDF i al nom dels fitxers. El navegador recorda les classes que ja has escrit i te les proposa en començar a escriure. Si el camp és buit quan exportes o imprimeixes, l'eina t'ho recorda.

La resta d'opcions (nom dels grups, format dels noms, girar «Cognoms, Nom», portaveu i ordre alfabètic) són a **Més opcions de presentació**, plegat per defecte.

### Format dels noms

- Si els noms són en format **«Cognoms, Nom»** (com a l'exportació d'iEduca), l'eina els mostra com a «Nom Cognoms». Es pot desactivar.
- Pots mostrar els noms complets, el nom i la inicial del cognom o només el nom. Això va bé per projectar a classe.
- Si copies també una columna de números (per exemple, el NIA), s'ignora.

### Retocar els grups

- **Arrossega** un nom a un altre grup.
- **Toca dos noms** per intercanviar-los.
- **Toca un nom i després un grup** per moure'l.
- **Clica el nom d'un grup** per canviar-lo.

Cada nom porta un número d'ordre dins del grup. Si actives **Marca un portaveu per grup**, el portaveu és el número 1.

### Exportar

| Botó | Resultat |
|---|---|
| **Desa o imprimeix** | Mostra la imatge dels grups (o del plànol) i permet **desar-la** en PNG o generar un **PDF per imprimir** en A4 |
| **Copia notes per a Sheets** | Obre la revisió de les notes de l'observació (vegeu més avall) |
| **Amaga la configuració** | Plega la barra lateral perquè els grups o el plànol ocupin tota l'amplada, per projectar-los. **Mostra la configuració** la torna a obrir |

---

## Plànol d'aula

Amb el botó **Plànol d'aula** (a dalt), els grups es mostren com a taules sobre un plànol, amb la pissarra a dalt i la taula del professor.

- **Arrossega cada grup per la capçalera** (o la taula del professor) per situar-lo on és a l'aula.
- Si tornes a barrejar amb el mateix nombre de grups, **les taules no es mouen**: només hi canvien les persones.
- **Reorganitza les taules** les torna a col·locar automàticament.
- La imatge i el PDF reprodueixen la disposició del plànol.

---

## Observació d'aula (semàfor)

Serveix per valorar ràpidament una activitat i passar les valoracions a un full de notes.

### Nivells

| Nivell | Color | Significat |
|---|---|---|
| **AE** | Verd | Assoliment excel·lent |
| **AN** | Verd clar | Assoliment notable |
| **AS** | Groc | Assoliment satisfactori |
| **NA** | Vermell | No assoliment |
| **Absent** | Blanc | No hi era |

### Com s'utilitza

1. Prem **Observació** (a dalt). Tothom comença en **AN**.
2. Escriu el nom de l'**activitat** i comprova la **data** (barra lateral, apartat *Observació d'aula*).
3. A cada targeta, els botons **Tot el grup: AE · AN · AS · NA** posen el mateix nivell a tots els membres del grup (els absents no canvien).
4. **Toca el nom d'un alumne** per matisar-ne el nivell o marcar-lo com a **Absent**.
5. Per valorar una altra activitat a la mateixa sessió, prem **Desa l'activitat i comença'n una altra**. Tothom torna a AN i els absents es mantenen.

Mentre l'observació està activa, tocar un nom serveix per valorar-lo. Per moure o intercanviar alumnes, desactiva-la.

En desar una activitat, el nom es manté (seleccionat, per si el vols canviar). Així pots avaluar un **segon criteri de la mateixa activitat**: desa-la, tria una altra rúbrica i torna a valorar. Cada criteri és una columna a l'Excel i a Sheets.

L'apartat **Activitats desades** és la llista de les activitats valorades durant aquesta sessió. Cada una és una columna a l'exportació, i es pot esborrar amb la ×. L'activitat en curs no hi surt, però també s'exporta si hi has valorat algú o si encara no n'has desat cap.

### Rúbrica (opcional)

Cada activitat pot tenir **un criteri d'avaluació** i **un indicador per a cada nivell** (AE, AN, AS, NA). Es posen al bloc *Rúbrica* de l'apartat d'observació.

- A la pantalla, el criteri surt sota el títol, i en tocar un nom cada botó mostra l'indicador del nivell.
- Des de la revisió de notes, **Imprimeix (PDF)** d'una activitat amb rúbrica genera una **graella de rúbrica** de tot el grup en A4 horitzontal: criteri a dalt, una columna per nivell amb l'indicador, la casella del nivell de cada alumne marcada i la nota. Si tries **Totes**, el PDF té **una pàgina de graella per a cada criteri**.
- Amb **Totes**, *Copia les notes* copia una columna per activitat.
- A l'Excel, la segona fila porta el criteri de cada activitat, i la pestanya **Rúbriques** recull els quatre indicadors.
- *Copia notes per a Sheets* no canvia: notes en números i cel·la buida per als absents.

### Banc de rúbriques

Fes un full de càlcul amb una rúbrica per fila i sis columnes: **Nom · Criteri · AE · AN · AS · NA** (la fila de capçalera és opcional). Hi ha tres maneres de portar-lo al Tauler:

1. **Des del full publicat al web** (recomanat, només a la versió de GitHub). Al full, **Fitxer → Comparteix → Publica al web**, tria el full del banc i el format **CSV**, i copia l'adreça. Enganxa-la a *Importa o copia el banc* i prem **Actualitza des del full**. El Tauler la recorda i, si deixes marcat *Cada cop que obro la pàgina*, llegeix el banc cada vegada. Qualsevol persona amb l'adreça pot llegir el full: no hi posis res més que les rúbriques.
2. **Copiant i enganxant** les files a *Afegeix al banc*. Si una rúbrica ja hi és amb el mateix nom, s'actualitza.
3. **Escrivint-la** al Tauler i prement **Desa al banc**.

A cada activitat, tria la rúbrica a **Banc de rúbriques**. Les rúbriques que vénen del full s'hi substitueixen cada vegada que s'actualitza: per canviar-les, edita el full.

El banc es desa **en aquest navegador** (no conté cap dada de l'alumnat). La versió de GitHub i la de Claude, o dos ordinadors diferents, tenen bancs separats: **Copia el banc** el copia en format de full de càlcul, per guardar-lo o passar-lo a un altre navegador.

### Exportar

- **Descarrega Excel** genera un fitxer `.xlsx` amb una fila per alumne i una columna per activitat (`Nom de l'activitat (dd/mm/aaaa)`).
- **Copia notes per a Sheets** obre primer una **revisió**: la llista d'alumnes en ordre alfabètic per cognoms amb la nota de cada un. Tries l'activitat (o totes) i prems **Copia les notes**. Es copien **només les notes, en format numèric**, una per fila:

  | Nivell | AE | AN | AS | NA | Absent |
  |---|---|---|---|---|---|
  | Nota | 4 | 3 | 2 | 1 | *(cel·la buida)* |

  A Google Sheets, clica la cel·la de la nota del primer alumne i enganxa.

  Cal que la llista del full també estigui en ordre alfabètic per cognoms.

  Des de la mateixa revisió, **Imprimeix (PDF)** genera la llista d'alumnes amb el nivell i la nota de l'activitat triada, per arxivar-la o imprimir-la.
- A l'Excel, les files poden anar en **ordre alfabètic per cognoms** o en **el mateix ordre que la llista enganxada**. Si copies la llista des del teu llibre de notes i tries aquesta segona opció, les files coincidiran exactament amb les del llibre.
- Si enganxes també la columna del **NIA**, apareix a l'Excel com a primera columna. No es mostra mai a la pantalla.
- Columnes: `NIA` (si n'hi ha) · `Alumne` · `Grup` · una columna per activitat amb `AE`, `AN`, `AS`, `NA` o `Absent`.

### Privacitat

Les observacions **no es desen enlloc**. Si intentes tancar la pestanya sense haver exportat, el navegador t'avisa. Els colors del semàfor no surten mai a la imatge ni al PDF dels grups.

---

## Separar i ajuntar alumnes

Pots indicar que algunes persones **no coincideixin** en el mateix grup o que **vagin juntes**. Les condicions s'escriuen en una columna del full de càlcul, al costat dels noms, i s'enganxen juntament amb els noms.

### Els codis

| Codi | Significat |
|---|---|
| `S` + número (`S1`, `S2`, `S3`…) | **Separar**: les persones amb el mateix codi aniran a grups diferents |
| `J` + número (`J1`, `J2`, `J3`…) | **Junts**: les persones amb el mateix codi aniran al mateix grup |
| `V` + número (`V1`, `V2`, `V3`…) | **Veu o categoria**: per exemple, `V1` veus agudes i `V2` veus greus |
| `A` (sense número) | **Absent**: vegeu l'apartat següent |

### Absents (codi A)

Posa una `A` a la columna de codis dels alumnes que no hi són (amb els altres codis, si en tenen: `A S1`).

- Els absents **no entren als grups**. Els grups es fan només amb els presents i respecten les condicions `S`, `J` i `V`.
- A l'observació, a la revisió de notes i a l'Excel surten com a **Absent** (a les notes copiades, la cel·la queda buida).
- Si un absent arriba tard, **esborra-li la `A`** a la llista: s'afegeix al grup més petit on no trenqui cap condició, i la resta de grups no canvia. Si marques una `A` nova, aquella persona surt del seu grup.
- El recompte de sota la llista i la línia de dalt dels grups indiquen quants absents hi ha.

### Veus (codi V)

Quan la llista té codis `V`, apareix el selector **Veus** a la barra lateral, amb dues opcions:

- **Grups barrejats, amb les veus repartides**: cada grup té una proporció semblant de cada veu.
- **Grups separats per veu**: cada grup només té alumnes d'una veu. Els grups es reparteixen entre les veus segons quants alumnes hi ha a cada una (com a mínim un grup per veu). Amb *Persones per grup*, la mida s'aplica dins de cada veu.

Cada persona té **una sola** veu. Els codis `S` i `J` continuen funcionant alhora: `V1 S1` vol dir veu aguda i separat dels altres `S1`. En mode separat, una unió `J` entre veus diferents no es pot complir i l'eina ho avisa.

### Normes

- Cada codi és **una lletra (S, J o V) seguida d'un número**, sense res més. L'única excepció és `A` (absent), que va sola.
- Cada codi és un conjunt independent: `S1` i `S2` no tenen cap relació, i `S1` i `J1` tampoc.
- Si una persona té més d'una condició, posa els codis a la **mateixa cel·la** separats per un espai: `S1 J2`.
- És igual si escrius majúscules o minúscules.
- No facis servir `+1` ni `-1`: Google Sheets els converteix en números i el codi es perd.
- Si escrius directament al quadre de l'eina en comptes d'enganxar des del full, separa el nom del codi amb una barra vertical: `Anna Ferrer | S1`. També es reconeixen els codis escrits al final del nom, a la mateixa cel·la: `Anna Ferrer S1`.
- `S01` i `S1` són el mateix codi.

### Exemple

Al full de càlcul:

| Nom | Codi |
|---|---|
| Ferrer Serra, Anna | `S1` |
| Puig Vidal, Biel | `S1` |
| Soler Pons, Dídac | `S1` |
| Vila Casas, Elna | `J1 S2` |
| Camps Oliver, Irene | `J1` |
| Pujol Sala, Jan | `S2` |
| Martí Roca, Carla | |

Resultat:

- Anna, Biel i Dídac aniran a **tres grups diferents** (`S1`).
- Elna i Irene aniran al **mateix grup** (`J1`).
- Elna i Jan **no coincidiran** (`S2`). Com que Elna va amb Irene, Jan tampoc no anirà al grup d'Irene.
- Carla no té cap condició.

*(Els noms són inventats.)*

### Comprovació

Sota la llista, l'eina mostra un requadre amb l'estat de les condicions. Només hi apareixen els codis, mai els noms:

- **✓ Totes es compleixen**: tot és correcte.
- **⚠ amb el motiu**: hi ha alguna condició que no es pot complir o que s'ha trencat. Pot passar per aquests motius:
  - Un codi `S` té més persones que grups. Per exemple, cinc persones amb `S1` i només quatre grups.
  - Un codi `J` uneix més persones de les que caben en un grup.
  - Dues condicions es contradiuen. Per exemple, dues persones unides amb `J1` que també tenen el mateix codi `S`.
  - Un codi només té una persona, de manera que no la separa ni l'ajunta amb ningú.
  - Un codi està mal escrit (per exemple, `X3`).
  - En grups separats per veu, un codi `S` té més persones d'una veu que grups té aquella veu.
  - En moure noms a mà, s'ha trencat alguna condició.

Quan una condició no es compleix, apareix un avís a dalt, i el botó **Mostra la configuració** porta el senyal ⚠ si la barra lateral està amagada.

Els codis **no apareixen mai** a les targetes dels grups, a la imatge ni al PDF.

---

## Publicar-la a GitHub Pages

L'eina és a la carpeta `tauler-aula/` del repositori [`gestioaula`](https://github.com/jchoucin-creator/gestioaula).

1. Activa GitHub Pages una sola vegada: **Settings → Pages**. A *Branch*, tria `main` i la carpeta `/ (root)`, i fes **Save**.
2. Cada eina del repositori té la seva carpeta, amb un `index.html` i un `README.md`.
3. Cada carpeta es publica a `https://jchoucin-creator.github.io/gestioaula/NOM-DE-LA-CARPETA/`.

No cal instal·lar res: cada eina és un sol fitxer HTML.

L'eina abans es deia *Creador de grups*. L'adreça antiga (`/gestioaula/creador-grups/`) redirigeix automàticament a la nova.

---

## Llicència

Codi sota llicència [MIT](https://opensource.org/licenses/MIT). El pots fer servir, modificar i compartir lliurement.
