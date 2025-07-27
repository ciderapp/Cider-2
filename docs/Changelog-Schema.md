# Changelog Schema Documentation

This document describes the unified changelog format for Cider releases. All changelog files must follow this schema to be properly processed by the Rise API Module and displayed correctly in the application.

## File Naming Convention

Changelog files should be named using the version number with `.md` extension:
- `2.3.2.md`
- `3.0.0.md`
- `2.4.1.md`

## File Structure

Each changelog file consists of two main parts:
1. **YAML Front Matter** - Structured metadata
2. **Markdown Content** - Detailed changelog content

## YAML Front Matter Schema

The YAML front matter must be enclosed between `---` markers and contain the following required fields:

```yaml
---
version: "2.3.2"
shortDesc: "Brief description of the release"
thumbnail: "https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/2.3.2.png"
highlights:
  - name: "Feature Name"
    desc: "Description of the feature"
    icon: "icon-identifier"
  - name: "Another Feature"
    desc: "Description of another feature"
    icon: "another-icon"
---
```

### Required Fields

#### `version` (string, required)
- The version number as a string
- Must match the filename (without `.md` extension)
- Examples: `"2.3.2"`, `"3.0.0"`, `"2.4.1"`

#### `shortDesc` (string, required)
- A brief, one-sentence description of the release
- Should summarize the main themes or most important changes
- Typically 50-100 characters
- Examples:
  - `"Major UI improvements with new queue system and redesigned library views"`
  - `"Bug fixes and security improvements with enhanced RPC controls"`

#### `thumbnail` (string, optional)
- URL to a preview image for the release
- Should use the format: `https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/filename`
- Images should be stored in the `changelogs/images/` directory
- Recommended formats: PNG, JPG
- Example: `"https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/2.3.2.png"`

#### `highlights` (array, required)
- An array of the most important features/changes in the release
- Should contain 3-8 items maximum for best UX
- Each highlight must contain `name`, `desc`, and `icon` fields

### Highlight Object Schema

Each highlight in the `highlights` array must contain:

```yaml
- name: "Feature Name"           # required: string
  desc: "Feature description"    # required: string  
  icon: "icon-identifier"        # required: string
```

#### `name` (string, required)
- Short, descriptive name of the feature
- Should be 2-6 words maximum
- Examples: `"New Queue List"`, `"Plugin Support"`, `"Light Mode"`

#### `desc` (string, required)
- Brief description explaining what the feature does
- Should be 1-2 sentences maximum
- Focus on user benefits rather than technical implementation
- Examples:
  - `"Replaces the current queue with a new, more powerful queue list. Featuring multi-selection and a new UI."`
  - `"Cider can now read the system accent color and apply it to the client for a more consistent look and feel."`

#### `icon` (string, required)
- Icon identifier for the feature
- Supports multiple icon systems:
  - **Ionicons**: `"ion-ios-star"`, `"ion-ios-list"`, `"ion-ios-albums"`
  - **FontAwesome**: `"fa-solid fa-gamepad"`
  - **Custom SVG**: `"svguse:cider-assets/cider-icons/icons.svg#lyrics"`

## Markdown Content

After the closing `---` of the YAML front matter, include the full changelog content in standard Markdown format.

### Content Guidelines

1. **Start with H1 heading** using the version number:
   ```markdown
   # Cider 2.3.2
   ```

2. **Organize content with sections** using H2 and H3 headings:
   ```markdown
   ## New Features
   ### Feature Name
   
   ## Bug Fixes
   ### Fixed Issues
   
   ## Performance Improvements
   ```

3. **Use bullet points** for lists of changes:
   ```markdown
   - Fixed issue where playlist listings would not load properly
   - Resolved animated artwork not playing correctly
   - Improved performance for media loading
   ```

4. **Include detailed explanations** for major features
5. **Credit contributors** when appropriate
6. **Link to external resources** if available (complete changelogs, documentation)

## Complete Example

```yaml
---
version: "2.3.2"
shortDesc: "Major UI improvements with new queue system and redesigned library views"
thumbnail: "https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/2.3.2.png"
highlights:
  - name: "New Queue List"
    desc: "Replaces the current queue with a new, more powerful queue list. Featuring multi-selection and a new UI."
    icon: "ion-ios-list"
  - name: "Revamped What's New"
    desc: "The What's New dialog has been improved to show the biggest changes in the latest version of Cider at a glance."
    icon: "ion-ios-star"
  - name: "Redesigned Library Albums"
    desc: "Library albums have been redesigned with a new rich album view layout that can display the albums inline."
    icon: "ion-ios-albums"
---

# Cider 2.3.2

This release focuses on major UI improvements, particularly around queue management and library browsing experiences.

## New Features

### New Queue List
Replaces the current queue with a new, more powerful queue list. The new queue features:
- Multi-selection capabilities
- Improved user interface
- Better performance with large queues

### Redesigned Library Albums
Library albums have been redesigned with a new rich album view layout that can display the albums inline:
- Album content is displayed underneath cover art when clicked
- Improved scrolling performance
- Better visual hierarchy

## User Interface Improvements

### Revamped What's New
The What's New dialog has been improved to show the biggest changes in the latest version of Cider at a glance, providing a better onboarding experience for new features.

## Bug Fixes

- Fixed issue where selected update branch notification preference wouldn't save properly
- Fixed bug where switching between Queue and History directly would not work
- Various styling consistency improvements throughout the application

## Performance Improvements

- Improved Artist page loading code
- Enhanced scrolling performance in library views
- Better responsive appearance for media item grids
```

## API Response Format

When processed by the Rise API Module, the changelog will be served as JSON with this structure:

```json
{
  "version": "2.3.2",
  "shortDesc": "Major UI improvements with new queue system and redesigned library views",
  "longDesc": "# Cider 2.3.2\n\n- Various changes to Library Artists...",
  "thumbnail": "https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/2.3.2.png",
  "highlights": [
    {
      "name": "New Queue List",
      "desc": "Replaces the current queue with a new, more powerful queue list. Featuring multi-selection and a new UI.",
      "icon": "ion-ios-list"
    }
  ],
  "lastUpdated": "1705312200000"
}
```

## Best Practices

### Highlights Selection
- Choose the **most impactful** features that users will notice
- Focus on **user-facing changes** rather than internal improvements
- Limit to **3-8 highlights** for optimal readability
- Order by **importance** (most important first)

### Writing Guidelines
- Use **clear, user-friendly language**
- Focus on **benefits to the user** rather than technical details
- Keep descriptions **concise but informative**
- Use **consistent terminology** across changelogs

### Icon Selection
- Choose **relevant icons** that represent the feature type
- Use **consistent icon styles** (prefer Ionicons for consistency)
- **Test icon availability** before committing
- Consider **visual balance** when selecting multiple icons

## Validation

Before committing a changelog file, ensure:

1. ✅ YAML front matter is valid and properly formatted
2. ✅ All required fields are present (`version`, `shortDesc`, `highlights`)
3. ✅ Version number matches filename
4. ✅ Highlights array contains 3-8 items
5. ✅ Each highlight has all required fields (`name`, `desc`, `icon`)
6. ✅ If `thumbnail` is provided, it uses the correct GitHub URL format
7. ✅ Markdown content starts with H1 heading
8. ✅ Content is well-organized with appropriate headings
9. ✅ No syntax errors in YAML or Markdown

## Migration from WhatsNew.vue

When migrating existing entries from `WhatsNew.vue`:

1. Extract version number and use as filename
2. Convert `items` array to `highlights` array
3. Create appropriate `shortDesc` based on the features
4. Add `thumbnail` URL if an image exists in `changelogs/images/`
5. Expand content from brief descriptions to full markdown
6. Ensure icon identifiers are preserved correctly
7. Add any missing changelog URLs or references

## Migration from Legacy Changelogs

When migrating from legacy changelog files:

1. Convert existing `image` field to full `thumbnail` URL format using `https://raw.githubusercontent.com/ciderapp/Cider-2/main/changelogs/images/filename`
2. Extract key features from content to create `highlights` array
3. Create `shortDesc` summarizing the main changes
4. Preserve version numbers and existing content structure
5. Update any relative image paths to full GitHub raw URLs

## Git Integration

The Rise API Module automatically extracts the `lastUpdated` timestamp from Git commit history. No manual timestamp management is required - simply commit the changelog file and the API will handle timestamp extraction.

## Support

For questions about the changelog schema or assistance with migration, please contact @cryptofyre or refer to existing changelog files as examples. 