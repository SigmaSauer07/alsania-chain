# rebrand.md

---

description: Automatically performs a full rebrand of a specified project using a provided brand kit, with enhanced error handling, asset optimization, and verification to ensure seamless integration and functionality.
auto_execution_mode: 3

---

## Steps

**Objective:** To execute a complete and seamless rebrand of a software project. This includes updating names, text, code variables, color themes, and all visual assets (logos, icons, images) according to a specified brand kit, ensuring the project remains fully functional. Enhancements include automatic backups, better handling of dependencies, support for multi-language projects, and deep verification with rollback options.

### Phase 1: Setup and Analysis

1.  **Identify Targets:**

    - **Project Path:** The root directory of the project to be rebranded.
    - **Brand Kit Path:** The directory containing the new branding assets.
    - **Backup Path:** Create a timestamped backup of the entire project in a separate directory (e.g., `project_backup_YYYYMMDD_HHMMSS`) before any changes.

2.  **Analyze Brand Kit:**

    - Scan the brand kit for a `rebrand.json` or similar configuration file. This file should define:
      - **Text Replacements:** A map of old values to new values (e.g., `"OldProjectName": "NewProjectName"`, `"old-company": "new-company"`, wallet addresses, specific dialogue). Include regex patterns for complex replacements if needed.
      - **Theme/Style Definitions:** Color palettes, font families, gradients, and other visual parameters.
      - **Asset Mappings:** Explicit mappings for asset replacements (e.g., `{ "old_logo.png": "new_logo.svg" }`).
      - **Localization:** If applicable, specify language-specific replacements.
    - Index all image assets (logos, icons, favicons, banners) available in the brand kit, noting their metadata (dimensions, format, resolution).
    - Validate the brand kit for completeness; if `rebrand.json` is missing, generate a template or halt with an error message.

3.  **Analyze Project:**

    - Scan the entire project to identify all files containing text to be replaced, focusing on file types like `.js`, `.ts`, `.py`, `.html`, `.css`, `.md`, and configuration files.
    - Identify all theme/styling files (e.g., `tailwind.config.js`, `theme.css`, CSS-in-JS files, SCSS variables, and build tool configs like `webpack.config.js` or `vite.config.js`).
    - Locate all existing image assets and document their paths, dimensions, file formats, and usages (e.g., via imports or HTML references).
    - Detect dependencies and external references (e.g., package.json names, API endpoints) that might need updates.
    - For multi-language projects, scan for i18n files or folders and note locales.

4.  **Generate Rebranding Plan:**
    - Create a detailed step-by-step plan detailing which files will be modified for text, style, and asset replacement, grouped by file type and directory.
    - For image assets, create a replacement map. If an asset in the brand kit is not a perfect match for an existing project asset (in size, format, or aspect ratio), flag it for processing and suggest optimizations.
    - Include potential risks (e.g., code breakage) and mitigation steps (e.g., regex filters for whole-word matches).
    - Estimate total changes and processing time.
    - Present the plan to the user for approval before proceeding, with options to customize or exclude certain files.

### Phase 2: Asset Processing

For each image asset that needs to be replaced in the project:

1.  **Find Best Match:** Locate the most suitable source image from the brand kit, prioritizing exact matches by name, then by type (e.g., logo variants).
2.  **Check for Mismatch:** Compare the source asset's properties (dimensions, format, aspect ratio, DPI) with the target asset's requirements. Assess quality and compatibility.
3.  **Process if Necessary:**
    - **Resize:** If dimensions differ, resize the source image to match the target's exact dimensions, using algorithms that preserve quality (e.g., Lanczos resampling). Maintain aspect ratio where possible; if cropping is needed, center-crop intelligently.
    - **Reformat:** Convert the image to the required format (e.g., from `.png` to `.svg` using vectorization tools if applicable). Optimize for web (e.g., minify SVGs, compress PNGs/JPGs).
    - **Enhance:** Apply brand-consistent filters (e.g., color adjustments to match new palette) if specified in `rebrand.json`.
    - **Create:** If no suitable source image exists, generate a new version using the primary logo or brand mark, scaling, cropping, or compositing as needed. For favicons, create multiple sizes (e.g., 16x16, 32x32, 192x192).
    - Handle special cases like animated assets or vector graphics.
4.  **Save New Asset:** Save the newly processed (resized, reformatted, enhanced, or created) image into the brand kit directory, using a descriptive name (e.g., `logo_128x128.png`). Update or create the asset mapping in `rebrand.json` to enrich the brand kit for future use. Generate variants if multiple formats are needed.

### Phase 3: Execution

Once the plan is approved and all assets are processed, execute the rebrand:

1.  **Text & Code Replacement:**

    - Perform a project-wide search-and-replace for all text, names, and addresses defined in the `rebrand.json` map, using whole-word matching and case sensitivity by default (with overrides for regex patterns).
    - Avoid replacements in comments, strings, or code blocks where it could break functionality; use context-aware tools to skip inappropriate matches.
    - Update dependencies (e.g., rename npm package in package.json, update imports).
    - For multi-language projects, apply replacements per locale.

2.  **Theme & Style Update:**

    - Modify the project's styling and theme configuration files to apply the new color palette, fonts, gradients, and other style rules from the brand kit.
    - Ensure compatibility with frameworks (e.g., update CSS variables, React theme providers).
    - Rebuild style outputs if using preprocessors (e.g., run SCSS compilation).

3.  **Image Asset Replacement:**
    - Replace all old image assets in the project with their newly processed counterparts. Update file paths, import statements, and references in code/HTML accordingly.
    - If asset names change, update all dependent files automatically.

### Phase 4: Verification

1.  **Build & Test:**

    - Attempt to build the project using its standard build scripts (e.g., `npm run build`), checking for errors.
    - If a test suite exists, run it (e.g., `npm test`) to verify core functionality, and perform manual checks on key features if automated tests are insufficient.
    - Validate visual assets by rendering pages or components to ensure they load correctly.
    - Test for accessibility and responsiveness.

2.  **Rollback if Needed:**

    - If errors are detected, offer to restore from the backup and provide a diff report of changes.
    - Log all modifications for easy reversion.

3.  **Report Completion:**
    - Provide a comprehensive summary of all changes made, including file counts, asset updates, and any skipped items.
    - Report the results of the build and tests, with screenshots or logs if visual verification was performed.
    - Confirm that all newly created assets have been saved back to the brand kit directory, and suggest archiving the backup after user confirmation.
    - Offer to generate updated documentation or changelogs reflecting the rebrand.

---

**Example `rebrand.json` structure:**

```json
{
  "text_replacements": {
    "OldProjectName": "NewProjectName",
    "old-company": "new-company",
    "0x123...abc": "0x456...def"
  },
  "theme": {
    "colors": {
      "primary": "#5A48E3",
      "secondary": "#F3F1FF",
      "accent": "#E34875",
      "gradient": "linear-gradient(45deg, #5A48E3, #E34875)"
    },
    "fonts": {
      "body": "Inter, sans-serif",
      "heading": "Poppins, sans-serif"
    }
  },
  "asset_mappings": {
    "old_logo.png": "new_logo.svg",
    "favicon.ico": "favicon_32x32.png"
  },
  "localization": {
    "en": {
      "welcome": "Welcome to NewProjectName"
    },
    "es": {
      "welcome": "Bienvenido a NewProjectName"
    }
  },
  "options": {
    "case_sensitive": true,
    "whole_word_only": true,
    "regex_patterns": {
      "wallet_address": "0x[a-fA-F0-9]{40}"
    }
  }
}
```
