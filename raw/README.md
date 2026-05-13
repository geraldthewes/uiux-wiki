# UI/UX Design Wiki - Karpathy Method Implementation

This wiki implements the [Karpathy method](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) for creating LLMs from text corpora, focusing specifically on UI/UX design resources.

## The Karpathy Method for LLMs from Text Corpora

Following Andrej Karpathy's approach to creating LLMs from text:
1. **Data Collection**: Download lots of text (we've gathered authoritative UI/UX sources)
2. **Tokenization**: Break text into words/pieces (we've structured content into markdown files with clear headers)
3. **Model Training**: Train a neural network to predict next tokens (this wiki provides a high-quality corpus for training)
4. **Sampling**: Generate text by sampling from the model (users can use this wiki for few-shot prompting or fine-tuning)

## Wiki Structure as a Text Corpus

This wiki is organized to serve as a structured text corpus that follows principles for effective LLM training:

### 1. Document Organization
Each markdown file represents a coherent document on a specific topic, making it easy for an LLM to learn discrete concepts.

### 2. Consistent Formatting
- Clear hierarchical headers (H1, H2, H3)
- Standardized sections (Summary, Takeaways, Origins, Applications, See Also)
- Uniform citation style for sources
- Cross-references using relative links

### 3. Rich Cross-Referencing
- Each file includes a "See also" section linking to related topics
- Tag-based organization in index files
- Hierarchical directory structure that groups related concepts
- Explicit connections between principles, laws, and applications

### 4. Metadata and Context
- Front matter implicit in file structure (directory indicates source/type)
- Dates and authors preserved where available
- Clear attribution to original sources
- Version control through git history

## Directory Structure

### Core Source Collections
- [`nn-g/`](./nn-g/README.md) - Nielsen Norman Group articles and study guides
- [`laws-of-ux/`](./laws-of-ux/README.md) - Laws of UX by Jon Yablonski
- [`apple-hig/`](./apple-hig/README.md) - Apple Human Interface Guidelines
- [`material-design/`](./material-design/README.md) - Google Material Design 3
- [`ixdf/`](./ixdf/README.md) - Interaction Design Foundation resources

### Topic-Specific Collections
- [`mood-boards/`](./mood-boards/README.md) - Visual direction and style guides
- [`conventions/`](./conventions/README.md) - UI patterns and platform conventions
- [`color/`](./color/README.md) - Color palette, harmony, and accessibility
- [`typography/`](./typography/README.md) - Font choice, hierarchy, and readability
- [`aesthetics/`](./aesthetics/README.md) - Visual design principles and HCI best practices
- [`workflows/`](./workflows/README.md) - Design processes and methodologies
- [`books/`](./books/README.md) - Summaries of key UX literature

## Cross-Reference System

Each file includes:
- **Clear title** as H1 header
- **Summary section** with core concept
- **Structured content** with consistent headings
- **See also** section linking to 3-5 related topics
- **Tag implications** through directory placement and explicit mentions
- **Source attribution** with links to original material

## How to Use This Wiki

### For Humans Learning UI/UX
- Browse by topic using the directory structure
- Use the search functionality of your editor/IDE
- Follow cross-references in "See also" sections
- Consult README files in each directory for overview
- Trace concepts from theory to application

### For LLMs/Prompting Applications
- Treat each markdown file as a document in the corpus
- Use directory structure as categorical cues (`nn-g/` indicates NN/g source)
- Leverage consistent formatting for tokenization
- Follow the tagging system for concept-based retrieval
- Use cross-references to build associative memory

## Example Learning Path

To understand usability testing best practices:
1. Start with [`nn-g/why-test-5-users.md`](./nn-g/why-test-5-users.md) for foundational principles
2. See related topics in "See also" section ([10 Usability Heuristics](./nn-g/10-usability-heuristics.md), [Empathy Mapping](./nn-g/empathy-mapping.md))
3. Explore connected concepts like [`laws-of-ux/hicks-law.md`](./laws-of-ux/hicks-law.md) for understanding user expectations
4. Check platform-specific applications in [`apple-hig/`](./apple-hig/README.md) and [`material-design/`](./material-design/README.md))

## Sources

All content is derived from:
- Nielsen Norman Group (nngroup.com)
- Laws of UX (lawsofux.com)
- Apple Human Interface Guidelines (developer.apple.com/design/human-interface-guidelines)
- Google Material Design 3 (m3.material.io)
- Interaction Design Foundation (interaction-design.org)
- Classic UX literature (referenced in [`books/`](./books/README.md))

## Contributing

This wiki follows the Karpathy method - contributions should focus on:
1. Adding high-quality, authoritative sources
2. Maintaining clear, structured formatting
3. Creating meaningful cross-references
4. Preserving the educational intent of original materials
5. Ensuring factual accuracy and proper attribution

Last updated: May 12, 2026
