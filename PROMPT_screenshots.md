# Prompt for Generating Simulation Screenshots

**Objective:**
Automatically generate high-quality, standardized screenshots for a list of HTML physics simulations.

**Instructions:**
1.  **Tool:** Use the `browser_subagent` tool.
2.  **Viewport:** Set the browser viewport size to **1280x720** pixels (16:9 aspect ratio). This is critical for consistency.
3.  **Process:**
    *   Open each target HTML file in the browser.
    *   Wait for the page to fully load (ensure any initial animations or canvas rendering are complete).
    *   Capture a screenshot of the entire viewport.
    *   Save the screenshot to the `screenshots/` directory in the repository root.
    *   **Naming Convention:** Use the exact filename of the simulation but with a `.png` extension (e.g., `micro-ecosystem.html` -> `micro-ecosystem.png`).
4.  **Verification:** After the subagent completes, verify that the files exist in the correct directory and have the correct dimensions.

**Example Task Description for Subagent:**
"For each of the following HTML files, open them in the browser, set the viewport size to 1280x720 (16:9 aspect ratio), and take a screenshot. Save the screenshots to the '/Users/harrycslau/Documents/Git Repositories/physics-simulations/screenshots/' directory using the filename of the simulation (e.g., 'micro-ecosystem.png').

Files:
[List of absolute paths to HTML files]"
