# CHUNGUS-3D: Markdown to NM3 Knowledge Graph Transformer

[![NM3 v1.0](https://img.shields.io/badge/NM3-v1.0-blue.svg)](system-prompt/artifacts/NM3-specification.md)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](#)

> Transform any markdown document into an immersive 3D spatial knowledge graph using semantic analysis and intelligent spatial organization.

**CHUNGUS-3D** is an agentic design system that transforms markdown documents into three-dimensional knowledge graphs using the **NM3 (Nested Markdown 3D) v1.0** specification. It analyzes content structure, extracts conceptual relationships, and creates spatially-organized XML representations that enable immersive 3D exploration of information.

---

## 🌟 What is NM3?

**NM3 (Nested Markdown 3D)** is a specification for storing interconnected markdown content in three-dimensional space. It extends traditional markdown with:

- **Spatial Organization**: Use X, Y, Z coordinates to position concepts meaningfully
- **Geometric Semantics**: Five primitive shapes (sphere, cube, cylinder, pyramid, torus) convey information structure at a glance
- **Visual Hierarchy**: 16 carefully-curated pastel colors provide semantic meaning while remaining comfortable for extended viewing
- **Relationship Links**: Connect nodes with typed relationships (leads-to, supports, contradicts, etc.)
- **Immersive Exploration**: Navigate knowledge graphs in true 3D space

### Key Benefits

- **Better Understanding**: Spatial relationships make complex information structures instantly comprehensible
- **Natural Organization**: Concepts cluster naturally in 3D space based on relationships
- **Multiple Perspectives**: Camera positioning enables different conceptual viewpoints
- **Scalable**: From simple note-taking to complex research with thousands of interconnected concepts

### Use Cases

- 📚 **Research Organization**: Central questions with radiating findings and evidence
- 📋 **Project Planning**: Goals, phases, dependencies, and blockers in logical 3D space
- 🎓 **Learning & Study**: Course topics with hierarchical concepts and examples
- 🗺️ **Knowledge Mapping**: Any domain knowledge transformed into explorable 3D graphs
- 📊 **Data Analysis**: Complex reports with spatial relationships

---

## 🤖 What is CHUNGUS-3D?

**CHUNGUS-3D** is an expert AI system (agentic design) that transforms markdown into valid NM3 XML. Think of it as a specialized agent that:

1. **Analyzes** markdown structure and content semantically
2. **Extracts** relationships between concepts automatically
3. **Positions** nodes in meaningful 3D space using intelligent algorithms
4. **Assigns** appropriate geometric types and colors based on content
5. **Validates** output against NM3 v1.0 specification with auto-correction
6. **Generates** production-ready XML for 3D visualization

### Core Capabilities

- ✅ Semantic structure identification (topics, subsections, examples, conclusions)
- ✅ Automatic relationship extraction (sequential, hierarchical, supporting, contradictory)
- ✅ Intelligent spatial positioning strategies (temporal X-axis, hierarchical Y-axis, importance Z-axis)
- ✅ Geometric type assignment based on content semantics
- ✅ 16-color pastel palette with semantic meaning
- ✅ XML validation and auto-correction
- ✅ CDATA handling for markdown preservation
- ✅ Link integrity verification

---

## 🚀 Quick Start

### Using with Claude Projects

1. **Create a new Claude Project** in your Claude interface

2. **Add the system prompt** to your project:
   - Copy contents of [`system-prompt/MD-to-NM3-system-prompt.md`](system-prompt/MD-to-NM3-system-prompt.md)
   - Paste as custom instructions for your project

3. **Add supporting artifacts** to project knowledge:
   - [`system-prompt/artifacts/NM3-specification.md`](system-prompt/artifacts/NM3-specification.md)
   - [`system-prompt/artifacts/NM3-preflight-checklist.md`](system-prompt/artifacts/NM3-preflight-checklist.md)
   - [`system-prompt/artifacts/NM3-template-example.md`](system-prompt/artifacts/NM3-template-example.md)

4. **Transform your content**:
   - Use the template from [`paste-anything-prompt.md`](paste-anything-prompt.md)
   - Attach your markdown document or paste text directly
   - Run: `"using a spatial clamp of 0.0 - 200.0 for all spatial dimensions, read and cross reference the attached document, then generate a new separate artifact NM3 formatted .xml file using CHUNGUS"`

5. **Receive pure NM3 XML** ready to visualize!

### Basic Workflow

```
Markdown Document → CHUNGUS-3D Analysis → NM3 XML → 3D Visualization
```

The system outputs **only valid XML** - no explanations, no commentary, just production-ready `.nm3` files.

---

## 📁 Project Structure

```
NM3-Demo/
├── README.md                          # This file
├── paste-anything-prompt.md           # Quick-start template prompt
├── system-prompt/
│   ├── MD-to-NM3-system-prompt.md    # Core CHUNGUS-3D agent instructions
│   └── artifacts/
│       ├── NM3-specification.md       # Complete NM3 v1.0 standard
│       ├── NM3-preflight-checklist.md # Validation checklist
│       └── NM3-template-example.md    # Valid XML structure examples
└── claude-projects/
    ├── gta-san-andreas.nm3            # Example: Gaming/geographic content
    ├── vem-drive.nm3                  # Example: Scientific analysis
    └── zv6-holo.nm3                   # Example: Technical documentation
```

### File Descriptions

#### System Prompt Files

- **`MD-to-NM3-system-prompt.md`**: The complete CHUNGUS-3D agent definition with transformation rules, spatial positioning strategies, color palette guidelines, and validation procedures.

- **`NM3-specification.md`**: Full NM3 v1.0 specification including XML schema, geometric types, color palette, link types, and best practices.

- **`NM3-preflight-checklist.md`**: Pre-flight validation checklist ensuring well-formed XML with balanced tags and proper structure.

- **`NM3-template-example.md`**: Reference templates showing valid node patterns and structure.

#### Example Files

Three diverse examples demonstrating CHUNGUS-3D's versatility across different content types.

---

## 🎨 Example Transformations

### 1. GTA San Andreas Map Analysis (`gta-san-andreas.nm3`)

**Content Type**: Geographic/gaming documentation

**Highlights**:
- 24 spatial nodes representing islands, cities, and landmarks
- Hierarchical organization: State → Islands → Locations
- Temporal progression links showing story advancement
- Gang territories and business systems as conceptual overlays
- ~40 interconnected relationships

**Demonstrates**: Complex hierarchical structures, geographic spatial organization, narrative progression

---

### 2. VEM Drive Pseudoscience Analysis (`vem-drive.nm3`)

**Content Type**: Scientific research critique / analytical report

**Highlights**:
- 22 nodes analyzing extraordinary claims and evidence
- Central thesis with radiating supporting evidence
- Color-coded by claim type (red=red flags, blue=real science, gray=debunked)
- Explicit contradiction links showing logical conflicts
- Comparison to EM Drive precedent as historical parallel

**Demonstrates**: Critical analysis structure, evidence pyramids, contradiction relationships, scientific rigor

---

### 3. Zero Vector 6 Holo Parameters (`zv6-holo.nm3`)

**Content Type**: Technical parameter documentation

**Highlights**:
- 30+ nodes organized by parameter categories
- Four domain cubes (Frequency, Interference, Memory, Degradation)
- Preset configurations linked to specific parameters
- Cyclical relationships (coherence decay, memory sessions)
- Hierarchical pyramids for optimization strategies

**Demonstrates**: Technical documentation, parameter relationships, preset systems, cyclical processes

---

## ⚙️ How It Works

### Transformation Pipeline

CHUNGUS-3D follows a systematic 5-phase approach:

#### Phase 1: Parse Markdown Structure
- Extract all headings and hierarchy levels
- Identify sections, subsections, lists, tables, code blocks
- Locate cross-references and internal links
- Detect questions, conclusions, examples

#### Phase 2: Build Concept Map
- Create nodes for meaningful sections
- Assign geometric types based on content semantics:
  - **Sphere**: Central themes, atomic concepts, questions
  - **Cube**: Structured information, categories, foundations
  - **Cylinder**: Processes, timelines, sequential flows
  - **Pyramid**: Hierarchies, priorities, goal-oriented structures
  - **Torus**: Cyclical processes, feedback loops, recurring patterns

#### Phase 3: Optimize Spatial Layout
- Cluster related nodes (within 10-unit radius)
- Apply spatial positioning strategies:
  - **X-axis**: Historical/Context (-) → Core (0) → Future/Outcomes (+)
  - **Y-axis**: Foundations (-) → Current (0) → Abstract/Goals (+)
  - **Z-axis**: Background (-) → Core (0) → Foreground/Active (+)
- Ensure minimum 2-unit separation
- Balance distribution across all axes

#### Phase 4: Generate Links
- Sequential content → `leads-to` links
- Hierarchical structure → `contains` links  
- Related concepts → `relates` links
- Supporting evidence → `supports` links
- Contradictions → `contradicts` links
- Examples → `exemplifies` links

#### Phase 5: Finalize & Validate
- Generate complete XML structure
- Ensure all IDs are unique and semantic
- Validate all link references exist
- Auto-correct any structural errors
- Format with proper indentation
- Verify CDATA sections wrap markdown content

### Color Semantics

CHUNGUS-3D uses 16 pastel colors, each with specific semantic meaning:

| Color | Hex Code | Semantic Meaning |
|-------|----------|------------------|
| `pastel-pink` | #FFB3BA | Urgent/Important concepts, warnings |
| `pastel-blue` | #BAE1FF | Information, research, data |
| `pastel-green` | #BAFFC9 | Solutions, actions, implementations |
| `pastel-yellow` | #FFFFBA | Questions, ideas, hypotheses |
| `pastel-purple` | #E0BBE4 | References, citations, sources |
| `pastel-orange` | #FFD4A3 | Attention points, key insights |
| `pastel-mint` | #B4E7CE | Fresh ideas, new thoughts |
| `pastel-lavender` | #D5AAFF | Creative, imaginative, theoretical |
| `pastel-peach` | #FFCAB0 | Personal notes, opinions |
| `pastel-sky` | #A8E6F0 | Context, background information |
| `pastel-rose` | #FFC4D6 | Emotional aspects, human factors |
| `pastel-lime` | #E7FFAC | Experimental, testing, provisional |
| `pastel-coral` | #FFB8B8 | Related, connected concepts |
| `pastel-lilac` | #C5A3FF | Abstract theory, philosophy |
| `pastel-cream` | #FFF9E3 | Documentation, records |
| `pastel-gray` | #D5D5D5 | Archive, completed, historical |

---

## 👁️ Viewing NM3 Files

### Careless-Canvas-3D (Recommended)

View your generated NM3 files in immersive 3D using **Careless-Canvas-3D**:

🔗 **[Careless-Canvas-3D Application](https://placeholder-url-for-careless-canvas-3d.com)** _(Coming Soon)_

**Features**:
- Full NM3 v1.0 specification support
- Interactive 3D navigation (rotate, zoom, pan)
- Node selection with markdown content display
- Link visualization with curves and animations
- Tag filtering and search
- Multiple view modes
- Export capabilities

### Other Viewers

NM3 is a **renderer-agnostic** specification. Any application supporting the NM3 v1.0 standard can visualize these files. The XML structure is designed for easy parsing and integration with:

- Three.js-based web applications
- Unity 3D game engine
- Custom VR/AR experiences
- Desktop 3D modeling software

### Manual Inspection

NM3 files are human-readable XML. You can open them in any text editor to:
- Inspect node positions and properties
- Review link relationships
- Read markdown content within CDATA sections
- Validate structure manually

---

## 🎯 Advanced Usage

### Customizing Spatial Bounds

Adjust the spatial clamp in your prompt for different scales:

```
# Compact visualization (good for <20 nodes)
spatial clamp of 0.0 - 50.0

# Standard visualization (20-100 nodes)  
spatial clamp of 0.0 - 200.0

# Large visualization (100+ nodes)
spatial clamp of 0.0 - 500.0
```

### Controlling Node Density

Influence how tightly concepts cluster:

- **Tight clustering**: Emphasize close relationships, easier overview
- **Spread layout**: Emphasize distinct concepts, easier individual focus

Add to prompt: `"prefer tight clustering around major themes"` or `"prefer spread layout with distinct concept zones"`

### Emphasizing Specific Aspects

Guide CHUNGUS-3D focus:

```
"emphasize temporal relationships and chronological flow"
"prioritize hierarchical structure over sequential connections"
"highlight contradictions and conflicting viewpoints"
```

### Working with Large Documents

For documents with >100 sections:

1. **Chunking**: Break into logical sections, transform separately, merge manually
2. **Hierarchical abstraction**: Generate high-level overview first, then detailed subsections
3. **Progressive refinement**: Start with main structure, add detail in iterations

### Color Override

Request specific color schemes:

```
"use warm colors (pink, orange, peach) for active concepts,
cool colors (blue, purple, sky) for reference material"
```

---

## 🔧 Technical Details

### NM3 v1.0 Specification

Complete specification available: [`system-prompt/artifacts/NM3-specification.md`](system-prompt/artifacts/NM3-specification.md)

**Key Technical Points**:

- **XML Schema**: Well-formed XML with UTF-8 encoding
- **Required Elements**: `<meta>`, `<camera>`, `<nodes>`, `<links>`
- **Node Attributes**: `id`, `type`, `x`, `y`, `z` (required); `scale`, `color`, `rotation-*` (optional)
- **Geometric Types**: Exactly 5 allowed types (sphere, cube, cylinder, pyramid, torus)
- **Color Palette**: Exactly 16 allowed colors (strictly validated)
- **Link Types**: 13 semantic relationship types
- **Content Preservation**: Markdown stored in CDATA sections

### Validation & Error Prevention

CHUNGUS-3D includes rigorous validation:

1. **Pre-output validation**: Checks structure, colors, types, CDATA, required elements
2. **Auto-correction**: Fixes common errors (missing tags, invalid attributes, broken references)
3. **Link integrity**: Verifies all `from`/`to` references exist
4. **ID uniqueness**: Ensures no duplicate node IDs
5. **Position validation**: Confirms numeric coordinates
6. **Scale validation**: Ensures positive scale values

### XML Structure Overview

```xml
<?xml version="1.0" encoding="UTF-8"?>
<nm3 version="1.0">
  <meta title="..." created="..." author="..." tags="..." />
  <camera position-x="..." position-y="..." position-z="..." 
          look-at-x="..." look-at-y="..." look-at-z="..." fov="..." />
  <nodes>
    <node id="..." type="..." x="..." y="..." z="..." scale="..." color="...">
      <title>...</title>
      <content><![CDATA[
        # Markdown content here
      ]]></content>
      <tags>...</tags>
    </node>
    <!-- More nodes... -->
  </nodes>
  <links>
    <link from="..." to="..." type="..." thickness="..." curve="..." />
    <!-- More links... -->
  </links>
</nm3>
```

### Performance Considerations

- **Optimal range**: 20-200 nodes per file
- **Maximum recommended**: <5000 nodes (specification limit)
- **Minimum separation**: 2 units between nodes to prevent visual overlap
- **Link complexity**: Prefer meaningful links over exhaustive connections

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Submit Example Transformations

Share your successful NM3 transformations:

1. Create interesting markdown → NM3 transformations
2. Submit to `claude-projects/` directory
3. Include brief description of content type and highlights

**Ideal examples**:
- Novel content types (scientific papers, legal documents, creative writing)
- Interesting spatial organizations
- Effective use of colors and geometric types
- Complex relationship patterns

### Improve Documentation

- Clarify unclear sections
- Add tutorials or walkthroughs
- Create video guides
- Translate documentation

### Report Issues

Found a problem? Please report:
- Invalid NM3 generation
- Specification ambiguities
- System prompt improvements
- Edge cases or failures

### Extend Capabilities

Ideas for enhancement:
- Additional spatial positioning strategies
- New semantic analysis patterns
- Better handling of specific markdown features (tables, diagrams, footnotes)
- Integration with specific tools or workflows

---

## 📚 Citations & References

### Core Technology

- **NM3 Specification v1.0**: Nested Markdown 3D standard for spatial knowledge organization
  - _Full specification_: [`system-prompt/artifacts/NM3-specification.md`](system-prompt/artifacts/NM3-specification.md)
  - _Release Date_: January 15, 2025
  - _Status_: Stable

### Related Work

_This section will be expanded with academic citations, related research, and acknowledgments._

**Placeholder for**:
- Knowledge graph visualization research
- Spatial cognition and learning studies
- 3D information visualization papers
- Related tools and technologies
- Inspirational prior work

### Acknowledgments

_Future acknowledgments of contributors, testers, and community members who have helped improve CHUNGUS-3D._

---

## 📄 License

_License information to be determined._

---

## 🔗 Links

- **Careless-Canvas-3D Viewer**: [_Coming Soon_](https://placeholder-url-for-careless-canvas-3d.com)
- **NM3 Specification**: [Full Specification](system-prompt/artifacts/NM3-specification.md)
- **System Prompt**: [CHUNGUS-3D Agent](system-prompt/MD-to-NM3-system-prompt.md)
- **Quick Start Template**: [Paste Anything Prompt](paste-anything-prompt.md)

---

<div align="center">

**Transform your markdown into 3D knowledge graphs with CHUNGUS-3D**

_Spatial organization • Semantic analysis • Immersive exploration_

Made with 🧠 for better understanding

</div>
