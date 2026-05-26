# Obsidian Style CaseMap Database

A comprehensive, extensible Obsidian vault and workflow inspired by LexisNexis CaseMap.  
Includes advanced fileClass design, custom field templates, evidence/chronology/matrix management, automation scripts, and plugin-neutral organization.  
**Works great on desktop and iPad (see iPad instructions below).**

---

## 📂 Folder Structure

```
obsidian-style-case-map-database/
├── .obsidian/
├── templates/
│   ├── fileClass/
│   │   ├── Case.fileclass.md
│   │   ├── Fact.fileclass.md
│   │   ├── Person.fileclass.md
│   │   ├── Evidence.fileclass.md
│   │   ├── Issue.fileclass.md
│   │   └── Chronology.fileclass.md
│   ├── Case Template.md
│   ├── Fact Template.md
│   ├── Person Template.md
│   ├── Evidence Template.md
│   ├── Issue Template.md
│   └── Chronology Item Template.md
├── scripts/
│   ├── generate-index.js
│   ├── generate-chronology.js
│   ├── generate-evidence-matrix.js
│   └── generate-fileclass-fields.js
├── vault/
│   ├── Cases/
│   ├── Facts/
│   ├── People/
│   ├── Evidence/
│   ├── Issues/
│   ├── Chronology/
│   ├── Matrix/
│   └── FileClasses/
│       ├── Case.fileclass.md
│       ├── Fact.fileclass.md
│       ├── Person.fileclass.md
│       ├── Evidence.fileclass.md
│       ├── Issue.fileclass.md
│       └── Chronology.fileclass.md
└── README.md
```

---

## 🚀 Features

- **FileClass System:**  
  Every entity gets its own `fileClass` specification (`/FileClasses/`) for structured notes, automation, and compatibility with YAML-aware plugins like Dataview & Properties.
- **Ready-to-use Markdown Templates:**  
  Find starter templates for every entity in `/templates/`.
- **Evidence Management:**  
  Handle PDF/image evidence, link notes, annotate, and generate an evidence matrix.
- **Chronology Timeline:**  
  Maintain a sortable, linked timeline of all facts, evidence, and events.
- **Evidence Matrix:**  
  Auto-generated matrix showing relationships between evidence, facts, issues, people, and cases.
- **Scripted Automation:**
    - Section indexes (`generate-index.js`)
    - FileClass field documentation (`generate-fileclass-fields.js`)
    - Chronology updater (`generate-chronology.js`)
    - Evidence matrix updater (`generate-evidence-matrix.js`)
- **iPad-friendly:**  
  All organizational and linking features work on iPad (some desktop-only scripts, see below).

---

## 📝 Getting Started

1. **Copy/repo clone the project to your computer or iPad (see iPad instructions below).**
2. Open the vault in Obsidian.
3. Use templates for all new notes.  
   Each note starts with YAML frontmatter tying it to the correct `fileClass`.
4. Interlink notes with `[[WikiLinks]]`.
5. To run automation scripts, use Node.js on desktop or laptop.

---

## 🔧 Scripts & Automation

- **`generate-index.js`** – Master index files in every main folder.
- **`generate-fileclass-fields.js`** – Lists all fileClasses and their defined fields (see `/vault/FileClasses/_fileclass_index.md`).
- **`generate-chronology.js`** – Updates a master timeline in `/vault/Chronology/master_chronology.md`.
- **`generate-evidence-matrix.js`** – Updates evidence matrix in `/vault/Matrix/evidence_matrix.md`.
- _Usage:_ Run from terminal with `node scripts/scriptname.js`  
  *(Not supported directly on iPad — see workflow below.)*

---

## 📚 FileClass & Custom Fields

Every note begins with YAML frontmatter, for example:

```yaml
---
fileClass: Case
CaseName:
DateOpened:
Court:
...
---
```

- Use `/vault/FileClasses/*.fileclass.md` to define schema for each entity.
- Customize fields at will.

---

## 📱 Obsidian on iPad Instructions

1. **Install [Obsidian on iOS](https://obsidian.md/mobile).**
2. **Transfer this project:**
   - ZIP on computer, send to iPad via AirDrop, iCloud Drive, or email.
   - Unarchive in the Files app. Open as a new vault in Obsidian (“Open folder as vault”).
   - Or, use Working Copy app to clone/sync from GitHub and link the folder to Obsidian.
3. **Templates & Daily Use:**
   - Use templates (move/copy `/templates/`) as needed to your Vault, or Templates plugin folder.
   - Add notes with YAML and fileClass fields.
   - Interlink notes.
4. **Syncing Between Devices:**
   - Use iCloud, Dropbox, or GitHub (plus Working Copy) to sync your vault between iPad and desktop.
5. **Scripts:**
   - Scripts **cannot run on iPad/iOS directly** (no Node.js runtime).
   - To update indexes, timeline, or matrix: run scripts on your computer and sync updated `.md` files back to iPad using cloud storage or GitHub.

**Tip:** Core features (linking, templates, note schema) work natively on iPad. Use plugins like [Dataview](https://github.com/blacksmithgu/obsidian-dataview) and [Templater](https://github.com/SilentVoid13/Templater) for extra power.

---

## 🛠️ Plugins (Optional but Recommended)

- [Dataview](https://github.com/blacksmithgu/obsidian-dataview): query, table, and summary views by YAML fields.
- [Properties](https://help.obsidian.md/Editing+and+formatting/Properties): visual field management.
- [Templater](https://github.com/SilentVoid13/Templater): powerful template fills.
- Most plugins work on iPad, but confirm compatibility if using non-core plugins.

---

## ✅ Example Workflow

- Open vault in Obsidian (iPad or desktop).
- When creating a Case/Fact/Person/Evidence/Issue/Chronology/Event, start from the proper template.
- Fill YAML fields!
- Link notes using `[[ ]]`.
- On desktop, run scripts for smart indexes and reporting, then re-sync your vault to mobile.

---

## 💡 Tips

- You can extend any entity or fileClass with more fields as needed.
- The matrix and chronology let you get a 360° view of case facts, issues, and supporting evidence.
- If using GitHub to sync, always pull before running scripts and push after updating your indexes/timelines.

---

## 👩‍💻 Support, Ideas, & Feedback

Open a GitHub issue at [https://github.com/carlymariec](https://github.com/carlymariec) or submit a pull request for improvements or fixes.

*This project is not affiliated with LexisNexis. It’s for creative, research, and educational use.*
