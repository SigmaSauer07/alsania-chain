---
description: description: Create, update, and organize project documentation, moving outdated files to 'olddocs'. auto_execution_mode: 3
auto_execution_mode: 3
---

---
description: Create, update, and organize project documentation, moving outdated files to 'olddocs'.
auto_execution_mode: 3
---

**Objective:** To ensure all project documentation is comprehensive, up-to-date, professionally organized, and easily understandable, by creating new documents, updating existing ones, and archiving irrelevant materials.

**Default Scope:** If no specific project path is provided, target the current workspace.

### Phase 1: Setup and Analysis

1.  **Identify Project Path:** Determine the root directory of the project for documentation management.
2.  **Scan Existing Documentation:**
    *   Identify all existing documentation files (e.g., `README.md`, `CONTRIBUTING.md`, `LICENSE`, files within `docs/` directories, inline code comments, design documents, user guides, etc.).
    *   Assess the current state of each document for relevance, accuracy, completeness, and adherence to best practices.
3.  **Identify Documentation Gaps:** Determine what essential documentation is missing based on the project's scope, technology, and target audience (e.g., API reference, installation guide, troubleshooting, design principles, architecture overview).
4.  **Identify Outdated/Irrelevant Documents:** Flag any documents that are no longer accurate, superseded, or not relevant to the current project state for archiving.

### Phase 2: Documentation Plan Generation

1.  **Propose Standard Structure:** Suggest a logical and professional directory structure for current documentation (e.g., a `docs/` folder at the project root with subfolders like `api/`, `user-guide/`, `design/`, `contributing/`).
2.  **List New Documents:** Detail each new document that needs to be created, including its proposed title, purpose, and location within the new structure.
3.  **List Documents for Update:** Specify which existing documents require updates, outlining the key areas of improvement or expansion.
4.  **List Documents for Archiving:** Provide a clear list of files that will be moved to the `olddocs` folder.
5.  **Seek User Approval:** Present the comprehensive documentation plan to the user for review and approval before proceeding with any modifications.

### Phase 3: Execution - Document Creation & Update

1.  **Create New Documents:**
    *   Generate content for all new documents as outlined in the approved plan.
    *   Ensure content is clear, concise, accurate, and professionally formatted (Markdown is preferred for readability and version control).
    *   Include relevant code examples, diagrams, and screenshots where appropriate.
2.  **Update Existing Documents:**
    *   Revise and expand existing documentation to reflect the project's current state, features, and best practices.
    *   Correct any inaccuracies, fill in missing information, and improve clarity and readability.
    *   Ensure consistency in terminology, formatting, and tone across all documentation.
3.  **Generate Code-based Documentation (if applicable):**
    *   If the project uses tools like JSDoc, TSDoc, Sphinx, or similar, generate API reference documentation directly from code comments.

### Phase 4: Execution - Document Organization & Archiving

1.  **Create `olddocs` Folder:**
    *   Check if an `olddocs` directory exists at the project root.
    *   If not, create the `olddocs` directory.
2.  **Archive Outdated Files:**
    *   Move all documents identified for archiving in Phase 2 into the `olddocs` folder.
    *   Maintain their original relative paths within `olddocs` if logical, or flatten if they are truly standalone.
3.  **Organize Current Documentation:**
    *   Move all newly created and updated documentation into the proposed standard structure (e.g., within the `docs/` directory).
    *   Ensure all internal links and references within the documentation are updated to reflect the new file paths.

### Phase 5: Verification and Finalization

1.  **Comprehensive Review:**
    *   Perform a final review of all current documentation for completeness, accuracy, clarity, and adherence to the established standards.
    *   Verify that all internal and external links are functional.
    *   Confirm that the `olddocs` folder contains only the intended archived files and that no critical current documentation was accidentally moved.
2.  **Report Completion:**
    *   Provide a summary report to the user detailing all actions taken:
        *   List of new documents created.
        *   List of documents updated.
        *   List of documents moved to `olddocs`.
        *   Confirmation of the new documentation structure.
    *   Offer to generate a `docs/README.md` to serve as an entry point to the new documentation structure.