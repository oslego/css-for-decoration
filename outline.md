# Outline: CSS For Decoration

25 min
Practical reusable solutions to decoration using CSS.

- Intro
  - bio
  - CSS use cases: layout, typography, decoration
    - layout: Floats, Flexbox, Grids
    - typography: Fonts, type scale, hierarchy
    - decoration: colors, backgrounds, shadows, borders, filters, blending
  - "X" done only in CSS
    - caution: heavy use of empty, non-semantic HTML elements, pseudo-elements for layers (::before, ::after), CSS side effects (quirks, black magic).
    - fragile, not very portable
    - good as exercises
    - not practical, should use SVG instead
  - this talk:
    - underused / overlooked CSS features (gradients, shadows, multi-background)
    - examples of practical use cases
    - NOT AN EXCUSE to avoid SVG

- Agenda
  - multi-background decoration
  - skeleton interfaces
  - image & multi-color borders
  - rulers, grids, range inputs
  - blend modes (Spotify)

- CSS Gradients
  - overlooked because of design trends (flat design), poor documentation online (bad example)
  - crash-course:
    - [DEMO] linear-gradient(angle, <color-stop>, <color-stop>)
    - [DEMO] radial-gradient()

  - KEY LEARNING: sudden-jump color-stops = hard lines
    - [DEMO] solid rectangles, solid circles

  - KEY LEARNING:
    - CSS gradients are images, not colors;
    - background properties apply: size, position, repeat

  - [ILLUSTRATION OF STACKED BACKGROUNDS]

  - [tentative] multi-color bottom border (Italian flag);
  - Angled background + animation;
  - Polygon mesh background (stack overflow);
  - SWISS in CSS
    - show examples gallery
    - [DEMO] one example

- Skeleton interfaces
  - better alternative to loading spinners
    - perceived improved performance (impression of progress)
    - Facebook, Medium, Slack
    - Luke Wroblewsky @Intel course
    - effective now because of novelty; will become the next "loading spinner".
  - [DEMO] Medium skeleton
    - animation a la Facebook app
  - "cheap", no asset downloads, no unnecessary JS cycles used

- Borders: images, gradients
  - KEY LEARNING: background-origin
  - [ILLUSTRATION OF BOXES: border, padding, content]
  - [DEMO] gradient border
  - [DEMO] image border + background-size cover

- Tool UI decoration
  - Grid (blueprint)
    - [DEMO] 2D grid
  - Rulers
    - [KEY LEARNING]: repeating-linear gradient
    - [DEMO] ruler
  - Range input
    - caution: targeting non-standard pseudo-elements ::-webkit-, ::-moz-, ::-ms-
    - [DEMO] simple range input
    - [LINK] examples from Ana Tudor's sliders

- CSS Blend Modes + CSS Gradients
  - intro to CSS Blend Modes (comparison to simple alpha)
  - [DEMO] tshirt blend modes
  - [DEMO] "target" + image + blend modes
  - [DEMO] Spotify album covers

- References:
  - Ana Tudor, @thebabydino
  - CSS Secrets by Lea Verou
  - Sara Soueidan's articles on SVG and CSS

- Conclusion
  - lots of power in CSS for decoration: CSS Gradients, multi-bg, CSS Blend Modes
  - complexity is an issue; specialized tools are needed to achieve full potential
    - for naysayers: complex SVG without vector editors like Illustrator or Sketch is also a pain
  - good for simple use cases:
    - portable, resilient (contained, not very fragile)
    - performance++ (no assets downloaded, no needless HTML elements)
    - DO restrict to decoration (do not create false expectations)
  - when in doubt, always use SVG
