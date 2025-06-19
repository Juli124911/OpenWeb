# OpenWebUI im ChatGPT-Stil

Dieses Projekt basiert auf OpenWebUI und wurde vollständig optisch und strukturell an das Design von ChatGPT angepasst – sowohl für Web als auch Mobile.

## 🎯 Ziel

Die Benutzeroberfläche soll sich exakt so anfühlen und aussehen wie ChatGPT von OpenAI:

- Optisch identisch (Farben, Layout, Sidebar, Eingabefeld, Chatblasen, etc.)
- Vollständig responsive (mobil nutzbar wie die ChatGPT-App)
- Umschaltbar zwischen Darkmode und Lightmode
- Navigation, Chats, Modelle, Eingabe und Einstellungen wie in ChatGPT
- Animationen und moderne UI-Elemente mit TailwindCSS & Svelte

---

## 📁 Projektstruktur (`/src`)

Nur die wichtigsten UI-Strukturen – bereits in der ZIP enthalten:

src/
├── routes/
│ ├── +layout.svelte → Hauptlayout mit Sidebar & Chatansicht
│ ├── +page.svelte → Einstiegspunkt: Chat direkt beim Start
│
├── lib/
│ └── components/
│ ├── layout/
│ │ ├── Sidebar.svelte → Linke Navigation wie in ChatGPT
│ │ └── Navbar.svelte → Oben, z. B. Modellwahl
│ │
│ ├── chat/
│ │ ├── Chat.svelte → Haupt-Chatansicht
│ │ ├── Messages/
│ │ │ ├── Message.svelte → Einzelne Chatnachricht (Blasenform)
│ │ │ └── UserMessage.svelte → Nachricht vom Nutzer
│ │ └── MessageInput.svelte → Eingabefeld unten
│
│ └── common/
│ ├── Loader.svelte → Ladeanimation
│ └── Modal.svelte → z. B. für Einstellungen
│
├── app.css → Globales Styling (Tailwind)
├── tailwind.config.js → Design-Farben, Darkmode, etc.
└── app.d.ts → Typdefinitionen

yaml
Kopieren
Bearbeiten

---

## 🛠️ Tech Stack

- **SvelteKit** – modernes Webframework
- **TailwindCSS** – für 1:1-Design wie ChatGPT
- **Framer Motion / Svelte Transitions** – für Animationen
- **Darkmode/Lightmode-Support**
- **Responsives Design für Mobilgeräte (PWA ready)**

---

## 🚀 Lokale Entwicklung

```bash
npm install
npm run dev
