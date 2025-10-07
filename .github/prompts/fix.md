Fix any issues in the following code from file path ${filePath}:${startLine}-${endLine}
${diagnosticText}
${userInput}

```
${selectedText}
```

Please follow these steps systematically:

1. **Address Detected Problems**: Correct all issues identified in the diagnostic text provided above. If no diagnostics are listed, confirm that no issues were detected based on the code snippet.

2. **Identify Additional Issues**: Scan the code for potential bugs, security vulnerabilities, performance inefficiencies, code smells, or best-practice violations (e.g., unused variables, improper error handling, or lack of input validation). Use static analysis tools or manual review if applicable.

3. **Provide Corrected Code**: Output the fully revised code snippet, ensuring it compiles/runs without errors. Present it in a code block with syntax highlighting appropriate to the language (e.g., ```python for Python code).

4. **Explain Fixes**: For each change, provide a clear, concise explanation including what was wrong, why it was problematic, and how the fix improves the code (e.g., "Fixed null pointer exception by adding a null check, preventing runtime crashes and improving robustness").

Next, provide a complete, fully detailed, and objective comparison of the projects against each other, covering similarities, differences, overlapping functionalities, complementary aspects, conflicting elements, and trade-offs. Structure this comparison using quantifiable metrics such as:

- **Feature Sets**: Detail core functionalities (e.g., authentication, data processing) versus extended ones (e.g., plugins, integrations), quantifying coverage with percentages or feature counts (e.g., Project A has 80% core features implemented vs. Project B's 95%). Include a breakdown of shared, unique, and overlapping features with examples.

- **Performance Benchmarks**: Include comparative data from standardized tests, such as load testing with tools like JMeter or Artillery, measuring metrics like response times (e.g., Project A: 200ms avg under 1k users vs. Project B: 150ms), throughput (e.g., requests per second), memory usage (e.g., RAM consumption in MB), and scalability (e.g., handling up to 10k concurrent users). Source data from publicly available benchmarks or simulated tests.

- **Maintenance Overhead**: Evaluate code churn (e.g., lines of code changed per month via Git history analysis), update frequency (e.g., release cadence: Project A bi-weekly vs. Project B monthly), bug rates (e.g., issues per 1000 lines of code), and dependency management (e.g., number of outdated packages). Use metrics from repositories like GitHub.

- **Extensibility**: Assess modularity (e.g., number of pluggable components), plugin architecture (e.g., support for third-party extensions with APIs), and customization ease (e.g., configuration options scored on a 1-10 scale based on documentation and user reviews).

- **Overall Suitability for Use Cases**: Analyze fit for scenarios like enterprise deployment (e.g., compliance with standards like SOC 2), rapid prototyping (e.g., setup time in hours), and others (e.g., mobile app development), with scores or rankings based on user feedback, case studies, or benchmarks. Include pros/cons for each project per use case.

Enhance clarity with visualizations, such as bar charts for feature comparisons (e.g., using ASCII art or links to generated charts if possible), tables summarizing metrics (e.g., a Markdown table with columns for each project and rows for metrics), and heatmaps for trade-offs (e.g., color-coded grids showing strengths/weaknesses, using simple text-based representations).

Then, offer a professional, strategic, and honest insight into the recommended actions required to implement the best elements from each project into a single, unified version. This should include a detailed step-by-step plan with specifics such as:

- **Prioritization of Features to Merge**: Rank features by merging priority (e.g., Phase 1: Retain superior UI/UX from Project A for intuitive design, backend logic from Project B for robustness, with rationale based on user adoption metrics like 40% higher engagement in A vs. 20% better reliability in B). Prioritize based on impact, feasibility, and dependencies.

- **Refactoring Strategies**: Outline conflict resolution, e.g., harmonizing authentication by adopting OAuth 2.0 from Project B while integrating Project A's custom roles, or unifying database schemas through migration scripts and API endpoint standardization using OpenAPI specs. Address code quality improvements like refactoring for SOLID principles.

- **Integration Techniques**: Specify methods like RESTful API bridging for services, containerization with Docker/Kubernetes for modular deployment, or component libraries (e.g., React components from A integrated into B's framework) to ensure seamless combination. Recommend tools for integration (e.g., Apache Camel for middleware).

- **Timelines for Development Phases**: Break down into milestones, e.g., Month 1: Planning and prototyping; Month 2-3: Core merging; Month 4: Testing and optimization, with estimated durations adjusted for team size (e.g., assuming a team of 5-10 developers).

- **Resource Allocation**: Define tools (e.g., GitHub Actions for CI/CD, Jira for tracking), team roles (e.g., 2 architects for design, 3 developers for coding, 1 QA engineer for testing), and budgets (e.g., $50k for tooling, including licensing and hardware).

- **Risk Assessments and Mitigation Plans**: Identify risks like integration conflicts (mitigated by phased rollouts) or data migration issues (addressed with backups and rollback scripts), with contingency plans. Include legal risks (e.g., licensing compatibility) and mitigation via open-source audits.

- **Validation Methods**: Include comprehensive testing (e.g., unit tests for merged code, regression tests post-merge, performance benchmarks matching pre-merge levels, user acceptance testing with beta groups). Recommend automated testing suites and monitoring tools.

Ensure the insight emphasizes feasibility (e.g., leveraging open-source overlaps), cost-effectiveness (e.g., reusing 60% of code to reduce development by 40%), alignment with long-term goals (e.g., scalability for enterprise growth), potential ROI (e.g., projected 25% efficiency gains), and considerations like migration paths (e.g., backward-compatible APIs) and compatibility (e.g., supporting legacy data formats). Provide a cost-benefit analysis summary.

After presenting the plan, verify user approval by explicitly asking for confirmation (e.g., "Do you approve this plan to proceed?"). If they do not approve, inquire whether they would like an alternative plan generated, prefer to edit specific parts of the current plan, or provide custom modifications, then iterate accordingly based on their detailed response, refining the plan until approval is granted. Ask clarifying questions if responses are ambiguous.

Once the plan is approved, ask if they would like to initiate the creation of the new, improved project version immediately in a new folder within the workspace (specify the directory if provided, e.g., /workspace/new-unified-project) or save the plan as a document for later use. If they choose to start creation, begin building the new project incrementally following the approved plan's steps, providing real-time progress updates (e.g., "Step 1 complete: Dependencies installed"), intermediate outputs (e.g., code snippets for merged authentication module, diagrams for architecture overview using ASCII or simple text), and opportunities for mid-course adjustments (e.g., "Would you like to tweak the UI integration before proceeding?"). If they choose to save the plan, generate a detailed document (e.g., in Markdown or PDF format, customizable based on user preference) containing all reviews, comparisons, insights, and the full plan, saving it in the user-specified directory (e.g., /workspace/plans/). In both cases, confirm successful completion with a summary of deliverables (e.g., "Project created with 5 modules merged; plan saved as unified-plan.md") and offer further assistance, such as implementation support (e.g., debugging sessions), additional analyses (e.g., cost-benefit reviews), or follow-up consultations (e.g., quarterly check-ins). Ensure all interactions are interactive, transparent, and user-centric throughout the process, adapting to user feedback for optimal outcomes. Maintain neutrality and base recommendations on data.
