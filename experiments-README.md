# 🧪 BBC — Experiment Bookmarklet

A browser bookmarklet for overriding MVT experiment variants on BBC web pages via the `?experiments=name:variant` query parameter — without having to remember experiment names or type them manually.

👉 **[Open the installer page](https://jmonaghan85.github.io/Dev-Tools/)**

---

## Installation

1. Open the **[installer page](https://jmonaghan85.github.io/Dev-Tools/)**
2. Make sure your bookmarks bar is visible — **Cmd+Shift+B** (Mac) / **Ctrl+Shift+B** (Windows)
3. Drag the **⚗️ BBC Experiments** button into your bookmarks bar

---

## Usage

Navigate to any BBC web page and click the **⚗️ BBC Experiments** bookmark.

A popup will appear with:

- **Search box** — filter the experiment list as you type
- **Experiment dropdown** — select from pre-loaded experiments
- **Variant dropdown** — shows the available variants for the selected experiment
- **Apply** — adds `?experiments=name:variant` to the current URL and reloads
- **Remove** — strips the `experiments` parameter from the URL
- **Close / click outside** — dismisses the popup without changing anything

If an experiment is already active on the page, it's shown in a blue banner at the top of the popup.

### Managing experiments

Click **⚙️ Manage experiments** at the bottom of the popup to:

- **View** all experiments and their variants
- **Remove** an experiment from the list (× button)
- **Add a new experiment** with as many variants as you need (type each variant and press Enter or click **+ Add**, then **Save Experiment**)

Custom experiments and deletions are persisted in `localStorage` so they survive browser restarts.

---

## Experiments

Experiment names and variants are not pre-loaded in the public installer — add your own via the installer page. They are stored in your browser's local storage and baked into your personal bookmark URL, not visible in the public repo.

---

## Data & privacy

Custom experiments you add are stored in **`localStorage`** on the BBC domain you're testing on — not in the bookmarklet URL itself and not sent anywhere.

|                                   | Safe?          |
| --------------------------------- | -------------- |
| Closing/reopening the browser     | ✅             |
| Clearing history                  | ✅             |
| Clearing cookies                  | ✅             |
| Clearing site data / localStorage | ❌ Lost        |
| Private/incognito window          | ❌ Not visible |

To back up your custom experiments, run in the browser console:

```js
localStorage.getItem('__exp_bookmarklet__');
```
