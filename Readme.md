You are an expert frontend developer and GitHub README template designer.

Update my existing “AI GitHub README Creator” project.

IMPORTANT:
Do not rebuild the project.
Do not remove existing features.
Do not change the form, preview editor, copy button, download button, ZIP export, Pyodide integration, backend integration, or compatibility checker.
Only improve the visual design and widget structure of all existing README templates.

CURRENT PROBLEMS

1. The background colour and text colour are too similar in some templates.
2. Headings, normal text, labels, and cards do not have enough contrast.
3. All templates look almost identical.
4. Widgets have the same rectangular design in every template.
5. Only the widget colours are changing.
6. The widget structure, layout, shape, icon, chart style, and arrangement are not changing.
7. It is difficult to identify which template is selected because the designs are too similar.

MAIN GOAL

Redesign all 10 templates so that each template has:

- A unique colour palette
- High contrast between background and text
- A different heading style
- A different section structure
- A different widget layout
- Different widget shapes
- Different chart styles
- Different icons or decorations
- Different spacing and alignment
- A clearly recognisable visual identity

The templates must not look like colour variations of the same design.

FILES TO CHECK

Search the entire project, especially:

- readme_generator.py
- generator.py
- script.js
- style.css
- index.html
- all README template functions
- all preview card functions
- all local widget fallback functions
- createLocalStatsFallback
- createLocalLanguagesFallback
- createLocalTrophyFallback
- activity graph generators
- any SVG widget generators
- any template configuration objects

FIRST: FIND THE REAL ROOT CAUSE

Before editing, inspect how the templates and widgets are currently generated.

Check whether:

- Every template calls the same widget-rendering function
- Only CSS variables or colours are changed
- The same HTML structure is reused in every template
- The same local fallback widget is displayed for every template
- Template information is not passed to widget-rendering functions
- The preview uses one shared widget design
- The README export uses a different design from the preview

Fix the root cause instead of applying random CSS changes.

==================================================
PART 1 — FIX COLOUR CONTRAST
==================================================

Create a separate theme configuration for every template.

Each configuration must include:

- pageBackground
- sectionBackground
- cardBackground
- primaryText
- secondaryText
- headingColor
- accentColor
- borderColor
- progressTrack
- progressFill
- iconColor
- linkColor

Example structure:

const TEMPLATE_THEMES = {
  minimal: {
    pageBackground: "#ffffff",
    sectionBackground: "#f8fafc",
    cardBackground: "#ffffff",
    primaryText: "#111827",
    secondaryText: "#475569",
    headingColor: "#0f172a",
    accentColor: "#2563eb",
    borderColor: "#dbeafe",
    progressTrack: "#e2e8f0",
    progressFill: "#2563eb",
    iconColor: "#2563eb",
    linkColor: "#1d4ed8"
  }
};

Do not copy the same values between templates.

Contrast requirements:

- Dark backgrounds must use light text.
- Light backgrounds must use dark text.
- Heading colours must be clearly visible.
- Secondary text must still be readable.
- Cards must be distinguishable from the main background.
- Progress bars must be visible against their tracks.
- Borders must be visible but not excessively bright.
- Never use dark purple text on a dark purple background.
- Never use light grey text on a white background.
- Never use identical colours for headings and backgrounds.

Use approximately WCAG AA readability standards:

- Normal text contrast should be at least 4.5:1.
- Large heading contrast should be at least 3:1.

Add a helper function if necessary:

function getContrastText(backgroundColor) {
  // Return a readable light or dark text colour.
}

==================================================
PART 2 — GIVE ALL 10 TEMPLATES UNIQUE IDENTITIES
==================================================

Redesign the existing 10 templates using these identities.

1. MINIMAL CLEAN

Visual identity:
- White or soft grey background
- Dark charcoal text
- Blue accent
- Large clean heading
- Spacious vertical layout
- Thin borders
- Very little decoration

Widget style:
- Flat statistic tiles
- Thin horizontal language bars
- Simple contribution grid
- Small technology badges
- No gradients
- No glowing effects

Structure:
- Header
- About
- Skills
- Statistics
- Languages
- Activity

2. PROFESSIONAL BLUE

Visual identity:
- Deep navy background
- White text
- Bright blue accent
- Corporate dashboard appearance
- Strong section dividers
- Symmetrical layout

Widget style:
- Three equal rectangular statistic cards
- Compact percentage bars
- Calendar-style contribution chart
- Professional outlined icons
- Repository widget with status indicators

Structure:
- Professional banner
- Career summary
- Expertise
- Statistics row
- Languages panel
- Activity calendar
- Contact section

3. CYBERPUNK NEON

Visual identity:
- Near-black background
- Neon pink and cyan accents
- Terminal or futuristic typography
- Sharp borders
- Decorative corner lines
- High contrast neon headings

Widget style:
- Angular or clipped cards
- Neon outlined statistic panels
- Segmented language bars
- Pixel-based activity graph
- Tech stack shown as terminal commands
- Glowing appearance in website preview only

Structure:
- Command-line header
- System profile
- Stats command output
- Languages terminal
- Activity matrix
- Connection links

Do not export unsupported glow CSS to GitHub.

4. NATURE GREEN

Visual identity:
- Cream or very light green background
- Dark forest-green text
- Leaf-green accent
- Soft organic sections
- Nature-inspired icons
- Calm and readable design

Widget style:
- Circular statistic badges
- Leaf-marked language bars
- Hill or area-style activity graph
- Rounded skill badges
- Project cards with plant icons

Structure:
- Organic header
- About section
- Growth statistics
- Language garden
- Activity landscape
- Social links

5. DARK PURPLE

Visual identity:
- Black-purple background
- White text
- Lavender headings
- Violet accent
- Elegant dark card layout
- Clear borders

Widget style:
- Ring or donut-style language representation
- Purple statistic cards
- Badge-based activity summary
- Trophy cards
- Skill icons inside outlined containers

Structure:
- Hero banner
- Profile summary
- Achievements
- Statistics
- Donut language widget
- Technology gallery
- Contact links

6. OCEAN WAVE

Visual identity:
- Deep ocean-blue background
- White and pale-cyan text
- Cyan accent
- Wave-inspired separators
- Different blue shades for layers

Widget style:
- Wave-shaped section header in preview
- Water-drop statistic cards
- Cyan language bars
- Wave or area activity chart
- Skill icons shown as floating bubbles

Structure:
- Ocean header
- About voyage
- Statistics bubbles
- Language depths
- Activity wave
- Project islands
- Contact dock

Keep the exported README GitHub-safe by using SVG assets or Markdown-compatible images for wave decorations.

7. RETRO TERMINAL

Visual identity:
- Black or very dark green background
- Bright green text
- Monospace appearance
- Command prompts
- Retro computer style
- No purple or blue accents

Widget style:
- ASCII-style bordered statistic boxes
- Green terminal progress bars
- Block contribution grid
- Skills displayed as package names
- Activity displayed like terminal output

Structure:
- Boot message
- User information
- Installed technologies
- System statistics
- Process activity
- Network links

8. PASTEL SOFT

Visual identity:
- Soft pink, peach, cream, and lavender background
- Dark brown or charcoal text
- Pastel blue and pink accents
- Gentle rounded sections
- Friendly and modern design

Widget style:
- Rounded soft statistic cards
- Pill-shaped progress bars
- Compact pastel skill tags
- Timeline-style activity
- Project cards with soft shadows in preview only

Structure:
- Friendly introduction
- About card
- Skills pills
- Statistics cards
- Languages
- Learning timeline
- Contact

9. MONOCHROME ELEGANT

Visual identity:
- Black, white, and grey only
- Strong contrast
- Elegant typography
- Thin white or grey borders
- No coloured gradients
- Editorial design

Widget style:
- Icon-led statistic blocks
- Black-and-white bar chart
- Vertical activity histogram
- Numbered project list
- Simple technology labels

Structure:
- Editorial title
- Biography
- Numbered expertise list
- Statistics
- Language chart
- Activity histogram
- Contact footer

10. SOLAR SYSTEM / ORBIT

Visual identity:
- Midnight navy background
- White text
- Orange, violet, and cyan accents
- Space-themed decoration
- Orbit lines and planet elements
- Strong contrast

Widget style:
- Circular planet statistic widgets
- Orbital language indicators
- Star-map activity graph
- Skill icons arranged like planets
- Projects shown as mission cards

Structure:
- Space hero
- Mission profile
- Orbit statistics
- Language planets
- Activity star map
- Project missions
- Communication signal links

Animations may be used only in the website preview.
The exported GitHub README must use static GitHub-compatible SVG or image assets.

==================================================
PART 3 — MAKE WIDGETS STRUCTURALLY DIFFERENT
==================================================

Do not use one common widget structure for all templates.

Create a widget layout or renderer selection system.

Example:

const TEMPLATE_WIDGET_TYPES = {
  minimal: {
    stats: "flatTiles",
    languages: "thinBars",
    activity: "simpleGrid",
    skills: "smallBadges"
  },
  professional: {
    stats: "corporateCards",
    languages: "dashboardBars",
    activity: "calendarGrid",
    skills: "outlinedIcons"
  },
  cyberpunk: {
    stats: "neonPanels",
    languages: "segmentedBars",
    activity: "pixelMatrix",
    skills: "terminalCommands"
  },
  nature: {
    stats: "circleBadges",
    languages: "leafBars",
    activity: "areaLandscape",
    skills: "organicPills"
  },
  darkPurple: {
    stats: "violetCards",
    languages: "donutChart",
    activity: "badgeTimeline",
    skills: "iconContainers"
  },
  ocean: {
    stats: "waterDrops",
    languages: "depthBars",
    activity: "waveChart",
    skills: "floatingBubbles"
  },
  terminal: {
    stats: "asciiBoxes",
    languages: "terminalBars",
    activity: "blockGrid",
    skills: "packageList"
  },
  pastel: {
    stats: "softCards",
    languages: "pillBars",
    activity: "timeline",
    skills: "pastelTags"
  },
  monochrome: {
    stats: "iconBlocks",
    languages: "monoBars",
    activity: "histogram",
    skills: "textLabels"
  },
  orbit: {
    stats: "planetCircles",
    languages: "orbitalChart",
    activity: "starMap",
    skills: "planetIcons"
  }
};

Create separate renderer functions, for example:

renderFlatStats()
renderCorporateStats()
renderNeonStats()
renderCircleStats()
renderPlanetStats()

renderThinLanguageBars()
renderSegmentedLanguageBars()
renderLanguageDonut()
renderTerminalLanguageBars()
renderOrbitalLanguages()

renderSimpleActivityGrid()
renderCalendarActivity()
renderPixelActivityMatrix()
renderWaveActivity()
renderTerminalActivity()
renderTimelineActivity()
renderHistogramActivity()
renderStarMapActivity()

Do not simply pass a different colour to one shared renderer.

Bad implementation:

renderStats(accentColor);

Correct implementation:

renderStatsByTemplate(templateName, data);

Each renderer should produce a genuinely different DOM or SVG structure.

==================================================
PART 4 — PREVIEW AND EXPORTED README
==================================================

Maintain two separate but visually related rendering modes:

1. Website Preview Mode
2. GitHub Export Mode

Preview mode may use:

- CSS animations
- Gradients
- Shadows
- Rounded cards
- Transitions
- Hover effects
- Grid and flexbox
- Decorative layers

GitHub export mode must use only GitHub-compatible content:

- Markdown
- Supported HTML
- Static SVG images
- PNG images
- GIF images when reliable
- Tables only when necessary
- Standard image links

Do not export:

- style attributes
- <style> tags
- JavaScript
- CSS animations
- display:flex
- display:grid
- unsupported HTML
- website-only component markup

The preview and exported README should have the same theme identity, but they do not need to use identical HTML.

For advanced widgets such as:

- donut charts
- planet widgets
- wave graphs
- circular badges
- histograms
- orbital charts

generate static SVG assets for GitHub export.

Save them using unique template-specific names, for example:

assets/minimal-stats.svg
assets/minimal-languages.svg
assets/professional-stats.svg
assets/professional-activity.svg
assets/cyberpunk-languages.svg
assets/nature-activity.svg
assets/dark-purple-language-donut.svg
assets/ocean-activity-wave.svg
assets/terminal-stats.svg
assets/pastel-timeline.svg
assets/monochrome-histogram.svg
assets/orbit-planets.svg

Make sure the ZIP download includes all required assets.

==================================================
PART 5 — FIX THE CURRENT SCREENSHOT DESIGN
==================================================

The current preview shown in the screenshot has these problems:

- The main page and cards use nearly the same dark colours.
- Purple headings do not contrast enough against the background.
- Top Languages uses the same horizontal-bar layout as other templates.
- Activity Graph uses the same contribution-square design.
- Statistics cards use the same rectangle structure.
- Large empty gaps appear between widgets.
- The layout does not feel connected.
- The footer is placed too close to the activity widget.
- The content does not clearly represent a unique theme.

Fix this by:

- Increasing contrast between the main background, sections, cards, headings, and secondary text.
- Reducing excessive empty vertical space.
- Using consistent section spacing.
- Giving each widget a theme-specific structure.
- Aligning widgets correctly.
- Ensuring the content stays inside the preview container.
- Preventing widgets from being cut off by the toolbar or scrollbar.
- Adding suitable bottom padding above the footer.
- Making responsive layouts work on desktop, tablet, and mobile.

==================================================
PART 6 — DO NOT BREAK DATA OR FUNCTIONALITY
==================================================

All widget designs must continue to use real or existing data:

- GitHub username
- Stars
- Forks
- Repository count
- Commit count
- Streak
- Followers
- Top languages
- Activity information
- Skills
- Projects

Do not replace dynamic data with permanently hardcoded values.

Mock data may be used only when:

- Preview fallback mode is enabled
- An external GitHub service fails
- The user has not entered a username

Clearly separate mock fallback data from real fetched data.

Do not modify:

- Form input names
- Existing element IDs
- Existing event listeners
- Pyodide startup
- Python-to-JavaScript conversion
- Copy Markdown
- Download README
- ZIP generation
- Username validation
- Widget API handling
- Cache handling
- Retry handling
- External preview toggle
- Compatibility checker rules

==================================================
PART 7 — GITHUB COMPATIBILITY
==================================================

Every generated README must pass:

✓ No inline CSS
✓ No <style> tags
✓ No JavaScript
✓ No unsupported HTML
✓ No flex/grid
✓ No animation CSS
✓ All checks passed

There must be zero occurrences of:

style=
<style
<script
display:flex
display:grid
flex:
grid:
animation:
position:
onclick=
onload=

inside exported README Markdown.

Important:
Do not weaken or bypass the compatibility checker.
Fix the generated output itself.

==================================================
PART 8 — IMPLEMENTATION QUALITY
==================================================

Use reusable functions without forcing every theme into the same design.

Recommended architecture:

- Shared data layer
- Template theme configuration
- Template widget configuration
- Preview renderers
- GitHub-safe SVG renderers
- Export asset manager
- Compatibility validation

Suggested function flow:

getTemplateTheme(templateName)
getWidgetConfiguration(templateName)
fetchGitHubData(username)
renderPreviewTemplate(templateName, data)
renderPreviewWidget(widgetType, data, theme)
generateGitHubSafeAssets(templateName, data)
generateReadmeMarkdown(templateName, data, assetPaths)
runCompatibilityCheck(markdown)

Add safe fallback handling.

If an individual widget fails:

- Show a theme-matching fallback
- Do not break the entire preview
- Do not produce an empty section
- Do not leave broken image icons

Clean up old object URLs when regenerating widgets to avoid memory leaks.

==================================================
PART 9 — TESTING
==================================================

Test every template separately.

For each template verify:

1. Background and text have strong contrast.
2. Heading is readable.
3. Cards are clearly separated from the background.
4. Statistics widgets have a unique structure.
5. Top Languages has a unique structure.
6. Activity widget has a unique structure.
7. Skills widget has a unique structure.
8. Layout differs from other templates.
9. Preview updates when the template changes.
10. Dynamic user data is preserved.
11. Mobile layout is readable.
12. No horizontal overflow.
13. No widgets are cut off.
14. README export includes required assets.
15. Compatibility checker passes.

Also compare every template pair and ensure no two templates share the exact same:

- Header structure
- Statistics structure
- Language chart structure
- Activity structure
- Skill layout

==================================================
PART 10 — FINAL REPORT
==================================================

After implementation, provide a report containing:

1. Root cause of identical widgets
2. Files modified
3. New theme configuration added
4. Widget renderers added
5. SVG assets added
6. Contrast improvements for each template
7. Layout differences for all 10 templates
8. Preview-mode changes
9. GitHub-export changes
10. Compatibility test results
11. Responsive test results
12. Any fallback behaviour retained

Do not only describe the solution.
Directly inspect and modify the project files.
Do not stop after changing colours.
The task is complete only when all 10 templates have clearly different colours, layouts, widget structures, and GitHub-safe exported outputs.
