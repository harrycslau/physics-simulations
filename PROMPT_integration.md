**Task:** Integrate new simulation files into the main project structure and register them in the system.

**Strict Requirements:**

1.  **File Renaming & Relocation:**
    *   **Source:** Identify files in the `.new/` directory.
    *   **Naming Convention:** Rename files to **kebab-case** (lowercase, hyphen-separated).
        *   Remove generic prefixes (e.g., `BL_`) if present.
        *   Replace spaces and underscores with hyphens.
        *   Example: `BL_Photoelectric Effect.html` -> `photoelectric-effect.html`
        *   Example: `Newton 2nd law of motion.html` -> `newton-2nd-law-of-motion.html`
    *   **Destination:** Move files to the appropriate subdirectory within `simulations/` based on their content:
        *   Physics -> `simulations/physics/`
        *   Biology -> `simulations/biology/`
        *   Chemistry -> `simulations/chemistry/`
        *   (Create directories if they do not exist).

2.  **Registration (`simulations.json`):**
    *   **Target File:** `data/simulations.json`.
    *   **Entry Format:** Add a new object for each simulation to the `simulations` array.
    *   **Required Fields:**
        *   `id`: Unique string ID (kebab-case, matching the filename).
        *   `title`: Object with `en-US` and `zh-HK` keys.
        *   `description`: Object with `en-US` and `zh-HK` keys (extract from file metadata or content if possible).
        *   `category`: The subject category (e.g., "Physics", "Biology", "Chemistry").
        *   `simulationUrl`: The relative path to the file (e.g., `/simulations/physics/photoelectric-effect.html`).
        *   `screenshotUrl`: Use a default placeholder (e.g., `/images/thumbnails/default.png`) or a specific one if available.
        *   `createdAt`: Current date (YYYY-MM-DD).
        *   `updatedAt`: Current date (YYYY-MM-DD).

3.  **Verification:**
    *   Ensure no duplicate IDs exist.
    *   Ensure `simulationUrl` paths are accurate.
