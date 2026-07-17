# 🔧 BBC — Toggle Bookmarklet

A browser bookmarklet for overriding feature toggle values on BBC web pages via the `?toggles=name:true,name:false` query parameter.

👉 **[Open the installer page](https://jmonaghan85.github.io/Dev-Tools/toggles.html)**

** This has been made utilising Aii agents and is in a public repo **

---

## Installation

1. Open the **[installer page](https://jmonaghan85.github.io/Dev-Tools/toggles.html)**
2. Add your toggle names to the list on the page
3. Make sure your bookmarks bar is visible — **Cmd+Shift+B** (Mac) / **Ctrl+Shift+B** (Windows)
4. Drag the **🔧 BBC Toggles** button into your bookmarks bar

Toggle names are baked into the bookmarklet URL so they're available on any domain without needing to be re-added.

---

## Usage

Navigate to any BBC web page and click the **🔧 BBC Toggles** bookmark.

A popup will appear with:

- **Search box** — filter the toggle list as you type
- **Checkboxes** — select one or more toggles to apply at once
- **true / false dropdown** — set the value for each toggle
- **Apply** — adds `?toggles=name:true,name2:false` to the current URL and reloads
- **Remove** — strips the `toggles` parameter from the URL
- **Close / click outside** — dismisses the popup without changing anything

If toggles are already active on the page, they're shown in a green banner at the top and their checkboxes are pre-checked.

### Managing toggles and adding new toggles

Click **⚙️ Manage toggles** at the bottom of the popup to:

- **View** all toggles in your list
- **Remove** a toggle (× button)
- **Add a new toggle** name directly in the popup

Any toggles added via the popup are also persisted to `localStorage` as a supplement to the baked-in list.

---

## Toggle names

Toggle names are not stored in the public GitHub repo. They are added via the installer page, stored in your browser's local storage, and baked into your personal bookmark URL.

> **Note:** The `?toggles=` override is ignored on live (production) environments — it only works on `localhost` and test/staging environments.

---

## Data & privacy

Toggle names you add are stored in **`localStorage`** on the installer page and baked into the bookmarklet URL in your browser — not sent anywhere or stored publicly.

| | Safe? |
|---|---|
| Closing/reopening the browser | ✅ |
| Clearing history | ✅ |
| Clearing cookies | ✅ |
| Clearing site data / localStorage | ❌ Lost (re-add on installer page) |
| Private/incognito window | ✅ Names travel with the bookmark URL |
