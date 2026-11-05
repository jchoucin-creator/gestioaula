# Creador de grups

Eina web per fer grups d'alumnes a l'atzar a partir d'una llista copiada de Google Sheets. Els grups surten equilibrats i es poden retocar a mà. Després es poden descarregar en una imatge o en un PDF per imprimir.

👉 **Fes-la servir aquí:** **https://jchoucin-creator.github.io/gestioaula/creador-grups/**

---

## Privacitat

- Els noms **només existeixen a la pestanya del navegador** on els enganxes.
- **No es desen enlloc**: ni al navegador, ni a GitHub, ni a cap servidor. En tancar o recarregar la pàgina, desapareixen.
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
| **Descarrega imatge** | Un PNG amb fons blanc |
| **PDF per imprimir** | Un PDF en mida A4 |
| **Veure la imatge** | Obre la imatge en gran. Amb clic dret (o mantenint-la premuda al mòbil) es pot desar o copiar |
| **Copia per a Sheets** | Copia els grups en columnes, per enganxar-los a Google Sheets |
| **Pantalla completa** | Mostra els grups en gran, per projectar-los |

---

## Separar i ajuntar alumnes

Pots indicar que algunes persones **no coincideixin** en el mateix grup o que **vagin juntes**. Les condicions s'escriuen en una columna del full de càlcul, al costat dels noms, i s'enganxen juntament amb els noms.

### Els codis

| Codi | Significat |
|---|---|
| `S` + número (`S1`, `S2`, `S3`…) | **Separar**: les persones amb el mateix codi aniran a grups diferents |
| `J` + número (`J1`, `J2`, `J3`…) | **Junts**: les persones amb el mateix codi aniran al mateix grup |

### Normes

- Cada codi és **una lletra (S o J) seguida d'un número**, sense res més.
- Cada codi és un conjunt independent: `S1` i `S2` no tenen cap relació, i `S1` i `J1` tampoc.
- Si una persona té més d'una condició, posa els codis a la **mateixa cel·la** separats per un espai: `S1 J2`.
- És igual si escrius majúscules o minúscules.
- No facis servir `+1` ni `-1`: Google Sheets els converteix en números i el codi es perd.
- Si escrius directament al quadre de l'eina en comptes d'enganxar des del full, separa el nom del codi amb una barra vertical: `Anna Ferrer | S1`.

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
  - En moure noms a mà, s'ha trencat alguna condició.

Els codis **no apareixen mai** a les targetes dels grups, a la imatge ni al PDF.

---

## Publicar-la a GitHub Pages

L'eina és a la carpeta `creador-grups/` del repositori [`gestioaula`](https://github.com/jchoucin-creator/gestioaula).

1. Activa GitHub Pages una sola vegada: **Settings → Pages**. A *Branch*, tria `main` i la carpeta `/ (root)`, i fes **Save**.
2. Cada eina del repositori té la seva carpeta, amb un `index.html` i un `README.md`.
3. Cada carpeta es publica a `https://jchoucin-creator.github.io/gestioaula/NOM-DE-LA-CARPETA/`.

No cal instal·lar res: cada eina és un sol fitxer HTML.

---

## Llicència

Codi sota llicència [MIT](https://opensource.org/licenses/MIT). El pots fer servir, modificar i compartir lliurement.
