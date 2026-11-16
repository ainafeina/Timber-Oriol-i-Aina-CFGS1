# 🪓 Timber V2 - Projecte de Programació Estructurada

[![C++](https://shields.io)](https://isocpp.org) 
[![SFML](https://shields.io)](https://sfml-dev.org)
[![Release](https://shields.io)](../../releases/tag/v1.0)

Projecte desenvolupat per a l'assignatura **0485 - Programació** (Curs 2026–2027) partint del codi base `TimberSFML3.cpp`. El joc transforma el clàssic *Timber* incorporant nous recursos gràfics i sonors, gestió avançada d'estructures de dades, múltiples modes de joc i persistència de rècords.

🌐 **[Visita la web del projecte (GitHub Pages)](https://[el-vostre-usuari].github.io/[nom-del-repositori]/)** | 📦 **[Descarrega l'executable (v1.0)](../../releases/tag/v1.0)**

---

## 👥 Autors i Metodologia (Pair Programming)

El desenvolupament s'ha dut a terme seguint la metodologia de **programació en parella**, alternant els rols de **Pilot** (implementació de codi) i **Copilot** (revisió, documentació i proves) a cada sessió:

* **[Oriol Serra ]** - [@oriolserra](https://github.com)
* **[Aina Pages]** - [@ainafeina1](https://github.com)

---

## 🎯 Reptes Implementats

El projecte s'ha estructurat en **9 reptes progressius** dividits per nivells de dificultat:

### 🟢 Nivell Bàsic
* **Repte 1. Recursos propis:** Substitució completa dels gràfics, tipografies i àudio (`background`, `tree`, `cloud`, `bee`, `branch`, `player`, `axe`, `rip`, `log`, `KOMIKAB_.ttf`, `chop.wav`) amb control d'errors en temps de càrrega (`loadFromFile`).
* **Repte 2. Més personatges decoratius:** Ampliació de l'escena amb múltiples NPC (abelles, ocells, núvols) gestionats mitjançant l'estructura `struct NPC` i la funció `updateNPC()`.

### 🟡 Nivell Mitjà
* **Repte 3. Bosc d'arbres:** Creació d'un entorn amb profunditat visual mitjançant un array estàtic d'estructures `struct Tree` amb diferents posicions, escales i capes de dibuix.
* **Repte 4. Sistema de vides:** Implementació de 3 vides per partida amb indicador visual al HUD (`livesText`), panell semitransparent i control per evitar descomptes múltiples en un mateix impacte.
* **Repte 5. Indicador d'FPS:** Càlcul i visualització en pantalla dels fotogrames per segon amb interval d'actualització, prevenció de divisió per zero, conversions explícites (`static_cast<float>`) i registre d'esdeveniments per consola.

### 🔴 Nivell Avançat i Ampliacions
* **Repte 6. Estructura de les branques:** Migració dels vectors paral·lels originals a un únic contenidor dinàmic (`std::vector<Branch>`) recorregut amb bucles basats en intervals (*range-based for*).
* **Repte 7. Dos modes de joc:** Definició d'un tipus enumerat `enum GameMode` i menú de selecció amb `switch` per triar entre dos nivells de dificultat amb diferent temps inicial (`timeRemaining`).
* **Repte 8. Rècord persistent en fitxer:** Lectura i escriptura de la millor puntuació en fitxer extern (amb gestió d'excepcions `try/catch`, validació i visualització al HUD).
* **Repte 9. Enduriment i depuració:** Optimització de bucles mitjançant sentències de salt (`break` i `continue`) i validació del codi mitjançant punts de ruptura i inspecció de variables a l'IDE.

---

## 🛠️ Tecnologies i Conceptes Aplicats

* **Llenguatge:** C++
* **Llibreria Gràfica:** SFML 3.0
* **Resultats d'Aprenentatge coberts:**
  * **RA1:** Tipus de dades, constants, operadors i conversions explícites.
  * **RA3:** Estructures de control (`if/else`, `switch`, `for`, `while`), salts (`break`, `continue`) i gestió d'excepcions (`try/catch`).
  * **RA5:** Entrada/sortida per consola, fitxers persistents i renderitzat gràfic.
  * **RA6:** Arrays estàtics, estructures (`struct`), enumeracions (`enum`), `std::vector` i iteradors.

---

## 🚀 Instal·lació i Execució

### Opció 1: Executar la versió compilada (Recomanat)
1. Aneu a l'apartat de **[Releases](../../releases)** d'aquest repositori.
2. Descarregueu el fitxer `.zip` de la versió **`v1.0`**.
3. Descomprimiu-lo (assegureu-vos que les carpetes `graphics/`, `fonts/` i `sound/` estiguin al mateix directori que l'executable).
4. Executeu `TimberV2.exe`.

### Opció 2: Compilar des del codi font
1. Cloneu el repositori:
   ```bash
   git clone https://github.com[el-vostre-usuari]/[nom-del-repositori].git
   ```
2. Obriu el projecte al vostre IDE (Visual Studio / Code::Blocks / CLion) amb **SFML 3.0** configurat.
3. Compileu i executeu el fitxer principal `TimberSFML3.cpp`.

---

## 📂 Estructura del Repositori

```text
├── src/                # Codi font del projecte (TimberSFML3.cpp)
├── assets/             # Recursos propis (imatges, tipografies i sons)
├── docs/               # Fitxers de la web (GitHub Pages), diagrames i vídeo
├── data/               # Fitxer de persistència del rècord (highscore)
└── README.md           # Documentació principal del projecte
```
