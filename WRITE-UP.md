# Gt — Colour Gamut

## Turning Images into Colour Systems

**Gt — Colour Gamut** is a browser-based colour exploration tool that turns an image into an interactive colour system.

The central idea is simple:

> **Pull a palette from any image, isolate a gamut. Build combinations and name them.**

Instead of treating an image as a static reference, Gt lets the user inspect it as a field of colour. Colours can be sampled directly from the image, explored through the extracted palette, combined into deliberate sets, named, saved and exported.

---

## The Design Question

How can a designer move from visual inspiration to a deliberate, reusable colour system without losing the relationship between the colours and the original image?

Traditional colour-picking tools usually reduce the process to selecting an individual pixel or generating a fixed palette. Gt approaches the image more spatially.

The image remains visible while its colour structure is extracted alongside it. Selecting a colour creates a relationship between the chosen swatch and the places where related colours occur in the source image.

The workflow becomes:

**Look → Isolate → Select → Combine → Name → Save → Share**

This positions Gt somewhere between a colour picker, palette generator and creative instrument.

---

## How Gt Works

### 1. Upload an image

A PNG or JPEG can be selected or dropped into the interface.

Gt reads the image in the browser and samples its pixels locally. The image is then analysed into a set of representative colours.

### 2. Extract the colour gamut

The extraction process groups sampled pixels into representative colour clusters and separates chromatic colours from neutral tones.

An additional accent pass looks for sufficiently saturated colours so that smaller but visually important accents have a better chance of appearing in the extracted gamut.

This matters because a colour can occupy a relatively small area of an image while still being important to the visual composition.

### 3. Explore the image and palette

The image and extracted palette are interactive.

Users can click the image or colour swatches to select colours. A selected colour can be used to reveal similar colour regions in the source image, connecting the abstract palette back to its visual origin.

### 4. Control sampling

Gt provides four sampling modes:

- **Fine** — detailed sampling
- **Balanced** — general-purpose sampling
- **Grouped** — more clustered colour representation
- **Blocky** — deliberately coarse sampling

The sampling control is intended to make the relationship between image detail and palette abstraction visible rather than hiding it behind a conventional slider.

### 5. Build a combination

Users can select up to six colours and place them into the **Combination** rail.

HEX values can be copied directly from the combination.

A combination can also be given a name manually or through the **Suggest name** function.

### 6. Save and export

A saved combination stores:

- Combination name
- HEX values
- RGB values
- CMYK conversion
- Nearest Pantone screen-reference approximation
- Pantone reference HEX

The export makes the palette useful outside the browser while preserving the relationship between the visual combination and its colour specifications.

CMYK values are mathematical sRGB-to-CMYK conversions. Pantone values are treated as nearest screen-reference approximations and are intended to be checked against a physical colour guide when production accuracy is required.

### 7. Share

Saved combinations can be shared through available platform interfaces and device storage workflows.

The share experience is intended to extend the palette beyond the tool, allowing a generated combination to become a visual artefact that can be passed between design, social and reference contexts.

---

# UX / UI Development

Gt developed as a visual-design exercise but became increasingly concerned with interaction design.

The interface was designed around a restrained editorial structure:

- Strong typographic hierarchy
- Fine borders and clear grouping
- Black-and-white interface treatment
- Responsive desktop and mobile behaviour
- Direct manipulation of image and colour
- Persistent relationship between source image and extracted palette
- Explicit states for selection, saving and exporting

The intention was to avoid turning the tool into a conventional settings panel. The colour itself remains the primary interface.

The interaction model is deliberately short:

> **Source image → colour field → palette → combination → specification**

This structure allowed the project to become a practical study of how visual design decisions affect usability.

---

# Usability Study

## Testing Gt With Designers

To validate the tool outside the assumptions made while building it, the prototype was shared with friends and designers and observed through actual use.

The study focused on:

- Discoverability
- Interaction clarity
- Colour extraction quality
- Sampling behaviour
- Similar-colour feedback
- Navigation
- HEX accessibility
- Saving and exporting
- General perceived usability

The objective was not simply to confirm that the interface worked technically. It was to find the points where the experience broke down for someone who had not built it.

---

## Feedback

### Val — Identity System Designer

Val responded positively to the overall concept and particularly to the interaction where clicking the image isolates colours.

The testing also exposed several issues:

- The instruction describing similar-colour revelation was not always reflected clearly in the observed interaction.
- Smaller bright or saturated colours were sometimes missed during extraction.
- The original sampling slider felt disproportionately large for four sampling states and initially made the control appear less responsive.

This feedback directly informed changes to the colour-extraction strategy, the sampling interaction and the communication of interactive states.

---

### Alexis

Alexis found the tool generally straightforward and did not encounter major navigation problems.

The main issue identified was the TXT download workflow. The interface reported that the file had downloaded, but the user could not immediately locate it in the expected downloads folder.

This highlighted an important distinction:

> A successful browser action is not necessarily a successful user experience.

The feedback prompted closer attention to export feedback and discoverability.

---

### Kelvin Nzioka

Kelvin tested the sampling and image interaction and questioned whether the pixelated visual treatment was intentional.

The interaction became useful beyond simple palette extraction. The tool could also be understood as a visualiser for observing how colours occupy an image and how different colours relate to one another.

This revealed another possible interpretation of Gt: a creative instrument for painters, illustrators and designers interested in colour relationships and mixing.

Kelvin also shared the tool with friends, creating another useful test of whether the experience could communicate itself outside the original development context.

---

### Mwatika

Mwatika initially reported difficulty downloading HEX codes.

At that stage, the bottom portion of the tool was still under development. The feedback reinforced the need to make colour specifications explicit and accessible rather than assuming that users would infer where or how the values could be retrieved.

Subsequent work added more direct access to HEX values and clearer export pathways.

---

### Alice Gachuhi

Alice reacted positively to the concept and asked how the tool had been developed.

Her response was useful in a different way: it indicated that the concept communicated enough of its purpose to generate curiosity before a detailed explanation of the underlying implementation.

---

# What the Testing Changed

The usability study moved Gt from being primarily a visual experiment toward being a more deliberate interaction-design project.

The feedback contributed to work around:

- Small saturated-colour extraction
- Similar-colour highlighting
- Sampling controls
- HEX accessibility
- Saving and export behaviour
- Instructional clarity
- Social sharing
- Device-storage workflows
- Cross-device testing

The broader lesson was that **technical functionality and perceived usability are different things**.

A feature can work correctly in code and still fail to communicate what happened, what the user should do next, or where the result went.

That distinction became part of the design process itself.

---

# UI/UX Learning & Design Education

## Interaction Design Foundation (IxDF)

The development of Gt was informed by ongoing study of UI/UX and interaction design through the **Interaction Design Foundation (IxDF)**.

IxDF learning became particularly relevant as the project moved beyond visual design into questions of:

- Usability
- Interaction
- Feedback
- Accessibility
- User behaviour
- Validation
- Human-centred design

The project provided a practical environment in which interaction-design principles could be tested against a working product and real user feedback.

Rather than designing the interface only around what looked visually appropriate, the development process increasingly considered whether controls were understandable, whether system feedback was visible, and where users encountered friction.

### Portfolio credit

**UI/UX Learning & Design Education**  
*Interaction Design Foundation (IxDF)*

UI/UX and interaction-design principles informed the research, prototyping, usability testing and iterative development of Gt — Colour Gamut.

Learn more: https://ixdf.org/

> IxDF is credited here as a design-education institution and learning source, not as a collaborator, sponsor or co-developer of Gt.

---

# Technical Direction

Gt is deliberately lightweight.

The current implementation is designed as a single browser-based HTML application using:

- HTML
- CSS
- JavaScript
- Canvas
- FileReader / browser file APIs
- Local storage
- Browser download APIs
- Native sharing capabilities where supported

The image-processing and palette-generation work happens in the browser rather than requiring an external image-processing service.

This keeps the prototype portable and makes it possible to test the tool simply by opening the HTML application.

---

# Product Interpretation

Gt started as a colour extraction tool.

Through development and user testing, its interpretation became broader.

It can function as:

### A colour picker
Select colour directly from an image.

### A palette generator
Extract representative colours from visual references.

### A colour visualiser
Reveal relationships between colours and their locations in the source image.

### A palette-building instrument
Select, combine and name up to six colours.

### A colour specification tool
Export HEX, RGB, CMYK and Pantone screen-reference information.

### A creative reference instrument
Use images to study colour relationships, contrast, accents and combinations.

The project therefore sits at the intersection of **visual design, colour exploration and interaction design**.

---

# Design Principle

The development process reinforced a simple principle:

> **Build it. Put it in someone's hands. Watch where it breaks. Then redesign it.**

The usability study was not an end-stage validation exercise. It became part of the design method.

Every point of friction became information about the relationship between the interface and the person using it.

That is the larger purpose of Gt: not only to generate colour palettes, but to make the process of seeing, selecting and organising colour more tangible.

---

# Credits

### Usability Study

- Alexis
- Alice Gachuhi
- Kelvin Nzioka
- Mwatika
- Val — Identity System Designer

### Design Education

**Interaction Design Foundation (IxDF)**  
UI/UX and interaction-design learning informing the development process.

---

# Project

**Gt — Colour Gamut**

Live site: https://colourgamut.edgeone.dev/

Repository: https://github.com/markmakelele/Gt---Colour-Gamut

---

*Gt is an ongoing design and development project. The interface, extraction behaviour, export workflows and interaction model continue to evolve through testing and iteration.*
