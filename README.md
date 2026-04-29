# Library Search Engine

A browser-based library search interface inspired by the original Qt desktop
prototype. The current version runs as a static HTML/CSS/JavaScript app and
keeps the data-structures focus of the project: fast prefix search, smart
ranking, detailed filtering, graph-style book connections, and undo/redo for
library edits.

## Contributors

- Ismail Taner Erdogan
- Nisa Goksen

## Screenshots

### Main Search

<img width="2624" height="1888" alt="Library search main screen" src="https://github.com/user-attachments/assets/4dfb63b9-ff02-463f-a008-ef4ea6bdb3e1" />

### Filter Panel

<img width="2624" height="1888" alt="Library search filter panel" src="https://github.com/user-attachments/assets/53864cdd-0d9c-443d-ac49-b456b3d7e4e0" />

### Book Connection Search

<img width="2624" height="1888" alt="Book connection search mode" src="https://github.com/user-attachments/assets/ddca904b-43c0-48f2-9abb-bd6c2f70e77f" />

## Features

- Normal search and full library listing
- Trie-backed prefix search for book titles, authors, and tags
- TF-IDF style fallback search for smarter matching
- Detailed filters for author, tag, year range, and score range
- Merge Sort / Quick Sort selection for filtered results
- Sorting by smart relevance, score, year, author, or title
- BFS-style connection mode between two books
- Add, update, and delete books from the interface
- Undo and redo support for book changes
- CSV seed dataset loaded from `kitaplar.csv`
- Browser persistence through `localStorage`

## Tech Stack

- HTML
- CSS
- JavaScript
- CSV data file

No build step or package installation is required.

## Run Locally

```bash
python3 -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

## Project Structure

```text
.
├── app.js
├── index.html
├── kitaplar.csv
├── README.md
└── styles.css
```

## Data Format

Each row in `kitaplar.csv` follows this structure:

```text
id,title,author,isbn,year,tagCount,score,tags
```

Tags are separated with `|`.

## Notes

The earlier repository version documented the C/C++ and Qt prototype. This
repository now reflects the current web version shown in the screenshots.
