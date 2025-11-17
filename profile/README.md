# Naming Principles
The best global naming convention for files across Altium, SolidWorks, and C++ projects emphasizes clarity, consistency, and avoiding problematic characters, adaptable to each domain's specifics.

## General Global Naming Principles
- Use lowercase letters for consistency and ease of search.
- Separate words with hyphens (-) rather than underscores or spaces, as hyphens improve readability and search engine compatibility.
- Avoid special characters that can cause errors or compatibility issues: < > : " \ | ? * and spaces should be avoided.
- Include meaningful descriptors in filenames to capture project, component, type, and version information.
- Keep filenames concise, ideally under 30 characters, but descriptive enough for identification.
- Use ISO 8601 format for dates (YYYYMMDD) if dates are included.
- Version files with clear incremental suffixes like v01, v02.
- For projects involving multiple configurations or revisions, incorporate those identifiers in filenames.
- Maintain consistency within a project or directory, even if it means tolerating minor exceptions to rules.

## Git Repositories
- Use all lowercase letters to avoid case sensitivity issues across platforms.
- Use hyphens (-) instead of underscores (_) or spaces to separate words for better readability and URL compatibility.
- Include a prefix for project, team, or product name if managing multiple repos within an organization.
- Add descriptive terms reflecting the repository contents or technology stack (e.g., frontend, backend, python, react).
- Keep names concise but informative enough to convey purpose at a glance.
- Avoid special characters and version numbers in the repo name; rely on version tags/releases instead.

## Altium Files
- Avoid spaces and restricted special characters.
- Use parameters such as ProjectName, PartNumber, and Date in the filename.
- A typical pattern: `<ProjectName>-<PartNumber>-<YYYYMMDD>.SchDoc` or `.PcbDoc`.
- Use no spaces, and stick with hyphens or camel case if needed.
- Leverage Altium's parameter and variant naming for auto-generated filenames.

## SolidWorks Files
- Incorporate company or project abbreviations, part identifiers, and revision numbers.
- Example pattern: `<CompanyCode>_<FiscalYear>_<ProjectCode>_<PartName>_Rev<Number>.sldprt`
- Use underscores or hyphens consistently as word separators.
- Include configuration or display state names in file names for different variants.
- Keep part names short but descriptive.

## C++ Files
- Name files after primary classes or modules they contain (e.g., `network_manager.cpp` for a NetworkManager class).
- Use lowercase with underscores or hyphens separating words (e.g., `sensor_reading.cpp`).
- Avoid spaces and special characters.
- Use typical extensions `.cpp` for source, `.h` or `.hpp` for headers.
- Include version or date info if useful, but generally file names focus on content.
- Follow language-specific conventions for variables and classes within the code but keep filenames simple and clear.

## Example Unified Naming Template
`<project>-<component>-<description>-<date>-v<version>.<extension>`

- `project`: short project code or company abbreviation
- `component`: module, part number, or subproject
- `description`: brief descriptor (e.g., schematic, board, class name)
- `date`: YYYYMMDD (optional)
- `version`: v01, v02, etc. (optional)
- `extension`: file extension for file type

This approach can be adapted to all file types, ensuring names remain unique, discoverable, and informative.
