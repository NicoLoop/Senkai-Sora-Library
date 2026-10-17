
# Senkai Sora Library

**A growing anime data library for anime discovery, metadata, and API-powered applications.**

Senkai Sora Library is a structured collection of anime and movie data designed to support anime-related applications, websites, and discovery platforms. It organizes entries into predictable paths, making it easier for developers to retrieve anime identifiers, metadata, and other associated information through their own integrations.

The library includes anime series and movies, with a growing catalog of titles ranging from classic favorites to newer releases.

## Library Statistics

| Metric | Count |
|---|---:|
| Total anime entries | 337 |
| Total episodes | 9,871 |
| Completed anime entries | 337 |
| Data pagination | 34 pages |

*Statistics reflect the current library data and may change as the collection grows.*

## Features

- **Structured anime catalog** — organized paths for series and movies.
- **Anime identifiers** — consistent, URL-friendly identifiers for individual entries.
- **Metadata storage** — JSON-based data files for easy integration.
- **Series and movie separation** — distinct directories for different content types.
- **Developer-friendly format** — works with JavaScript, TypeScript, Python, PHP, and other languages that support JSON.
- **Scalable organization** — designed to accommodate additional titles and metadata over time.

## Repository Structure

```text
Senkai-Sora-Library/
├── series/
│   ├── solo-leveling/
│   │   └── data.json
│   ├── one-piece/
│   │   └── data.json
│   └── ...
├── movies/
│   ├── your-name/
│   │   └── data.json
│   └── ...
└── README.md
```

Each anime entry is stored in its own directory, with `data.json` containing the associated data for that title.

The exact fields available depend on the individual entry.

## Accessing the Data

You can access the repository through GitHub or retrieve individual JSON files using GitHub's raw content URLs.

**Example:**

```text
https://raw.githubusercontent.com/NicoLoop/Senkai-Sora-Library/main/series/solo-leveling/data.json
```

This URL points to the raw JSON file for *Solo Leveling*. Replace the path with another entry's path to retrieve its data.

### JavaScript Example

```javascript
const url =
  "https://raw.githubusercontent.com/NicoLoop/Senkai-Sora-Library/main/series/solo-leveling/data.json";

async function getAnimeData() {
  const response = await fetch(url);

  if (!response.ok) {
    throw new Error(`Failed to fetch anime data: ${response.status}`);
  }

  return response.json();
}

getAnimeData()
  .then((anime) => console.log(anime))
  .catch(console.error);
```

### Python Example

```python
import requests

url = (
    "https://raw.githubusercontent.com/NicoLoop/"
    "Senkai-Sora-Library/main/series/solo-leveling/data.json"
)

response = requests.get(url, timeout=15)
response.raise_for_status()

anime_data = response.json()
print(anime_data)
```

These examples retrieve an individual JSON file directly. They do not represent a separate hosted API service.

## Anime Identifiers

Entries use structured paths as identifiers.

Examples:

```text
series/solo-leveling
series/one-piece
series/death-note
movies/your-name
movies/weathering-with-you
```

The path identifies the entry's location within the library and can be used by applications to reference the corresponding data file.

## Catalog Index

The repository's catalog index tracks completed entries and aggregate statistics. An index may include fields such as:

```json
{
  "last_page": 34,
  "completed_animes": [
    "series/solo-leveling",
    "series/one-piece",
    "movies/your-name"
  ],
  "stats": {
    "total_animes": 337,
    "total_episodes": 9871
  }
}
```

*The snippet above illustrates the index format; the actual index may contain additional entries and fields.*

## Use Cases

Senkai Sora Library can be useful for:

- Anime discovery and catalog websites.
- Anime search and recommendation interfaces.
- Metadata-driven applications.
- Personal anime databases and watchlist projects.
- Learning projects involving APIs, JSON, HTTP requests, and data organization.
- Frontend applications that consume structured anime metadata.

## Data Accuracy and Availability

This is a community-oriented data library, and its completeness, accuracy, and availability may vary between entries. Developers should validate the data they consume and handle missing files, unavailable fields, and HTTP errors gracefully.

Because the files are hosted through GitHub, requests are subject to GitHub's availability, caching behavior, and applicable usage limits. For production applications with substantial traffic, consider implementing caching or maintaining a local copy where permitted.

## Contributing

Contributions that improve the library's structure, data quality, documentation, and consistency are welcome.

1. Fork the repository.
2. Create a branch for your changes.
3. Add or update the relevant JSON data.
4. Verify that the JSON is valid and follows the existing directory structure.
5. Submit a pull request describing your changes.

Please avoid duplicate entries and ensure that metadata is accurate and appropriately sourced.

## Copyright and Attribution

Senkai Sora Library is intended to organize anime-related metadata for developers. The repository should not be assumed to own or license the underlying anime, characters, artwork, episode footage, or other third-party intellectual property.

Contributors should only submit data and assets they have the right to redistribute. Any third-party material remains subject to its applicable rights and licenses.

## License

The repository's code, original documentation, and original contributions may be licensed separately from third-party data or assets. Check the repository's `LICENSE` file for the applicable terms before redistributing or adapting its contents.

---

**Senkai Sora Library** — structured anime data for developers building anime experiences.

Repository: [NicoLoop/Senkai-Sora-Library](https://github.com/NicoLoop/Senkai-Sora-Library)
