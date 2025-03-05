# 🎨 Marp Styles für VS Code & Marp-CLI

## 📌 Verwendung des Themes in VS Code

1️⃣ Öffne **VS Code** und gehe zu `settings.json`:  
   - Öffne die **Einstellungen** (`Cmd + ,` auf macOS, `Ctrl + ,` auf Windows).  
   - Suche nach `settings.json` und öffne die Datei.

2️⃣ Füge folgende Zeile hinzu, um das Marp-Theme global verfügbar zu machen:

```json
{
    "markdown.marp.themes": [
        "https://raw.githubusercontent.com/MeanDeanFWI/marpstyles/main/thws.css"
    ]
}
```

3️⃣ **Theme in Markdown-Dateien verwenden**:

```markdown
---
theme: thws
---
```

---

## 📌 Nutzung mit Marp-CLI

Falls du das Theme auch in der **Marp-CLI** verwenden willst, nutze diesen Befehl:

```sh
marp --theme "https://raw.githubusercontent.com/MeanDeanFWI/marpstyles/main/thws.css" meine_folie.md
```

---

## 📌 Verwendung von Bildern in `thws.css`

**❗ Wichtig: GitHub unterstützt keine relativen Pfade zu Bildern in CSS.**  
**Verwende immer „Raw“-Links statt relativer URLs!**  

1️⃣ **Richtiger Bild-Link auf GitHub**  
   - **Falsch:**  
     ```
     url("thws-logo_horiz_de_white.png");
     ```
   - **Richtig:**  
     ```
     url("https://raw.githubusercontent.com/MeanDeanFWI/marpstyles/main/thws-logo_horiz_de_white.png");
     ```

2️⃣ **Beispiel für CSS mit korrekt eingebundenem Bild**:

```css
section.titlepage::before {
    content: "";
    background: url("https://raw.githubusercontent.com/MeanDeanFWI/marpstyles/main/thws-logo_horiz_de_white.png") no-repeat left top;
    background-size: 6.5cm 1.5cm;
    position: absolute;
    top: 0.5cm;
    left: 0.5cm;
    width: 6.5cm;
    height: 1.5cm;
    z-index: 10;
}
```

---

## 📌 Fehler vermeiden ✅

🔹 **Nutze immer `raw.githubusercontent.com` für Bilder und CSS!**  
🔹 **Teste die URL im Browser** – Sie muss das Bild direkt anzeigen.  
🔹 **Speichere die Bilder im Haupt-Branch (`main`)** und achte darauf, dass sie öffentlich zugänglich sind.  
🔹 **Falls VS Code das Theme nicht lädt, überprüfe `settings.json` und starte VS Code neu.**  

---

## 🚀 Viel Spaß mit Marp!
Dieses Repository macht es einfach, schöne und konsistente Präsentationen mit Marp zu erstellen. 🎨✨

