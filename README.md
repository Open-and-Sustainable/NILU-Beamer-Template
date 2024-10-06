# Unofficial LaTeX Beamer Template for NILU

This LaTeX Beamer theme is designed for use in presentations at the Climate and Environmental Research Institute - NILU. The theme allows users to switch between two different templates (Template A and Template B) depending on their presentation needs. 

## Features
- Two customizable templates: **Template A** and **Template B**.
- Consistent NILU branding with logo and color schemes.
- Custom fonts and colors.
- Automatic Table of Contents at the start of each section.
- Multiple configuration options, including customized footers and block styles.

## Getting Started

### Installation

To use this theme, download the `beamerthemenilu.sty` file and place it in the same directory as your presentation `.tex` file. 

Alternatively, you can add it to your LaTeX environment's path so that it can be accessed globally.

### Basic Usage

To use this NILU Beamer theme, include the following in the preamble of your LaTeX presentation:

```latex
\documentclass{beamer}
\usepackage[templateA]{beamerthemenilu} % Select templateA (default)
```

or

```latex
\usepackage[templateB]{beamerthemenilu} % Select templateB
```

### Switching Between Templates

There are two templates available:
- **Template A**: The default template with bold, larger fonts and a more structured layout.
- **Template B**: A more lightweight, minimal template with slightly smaller fonts and a simpler footline.

To select a template, use one of the following commands in your preamble:

#### Template A (default)
```latex
\usepackage[templateA]{beamerthemenilu}
```

#### Template B
```latex
\usepackage[templateB]{beamerthemenilu}
```

If no option is provided, Template A will be used by default.

### Customization Options

- **Logo**: The NILU logo is automatically added to the title page and footer of all slides.
- **Title Page Background**: Both templates allow you to have a custom background image on the title page (`image1.jpg` for Template A and `ice.jpg` for Template B). You can replace these images in the `graphics` folder or modify the `.sty` file to point to different images.
- **Fonts**: The templates use the [Source Sans Pro](https://fonts.google.com/specimen/Source+Sans+Pro) font by default. Font sizes differ between the two templates but can be customized further in the `.sty` file.
- **Color Scheme**: The theme uses a consistent color scheme with NILU branding. You can adjust the color definitions by modifying the following lines in `beamerthemenilu.sty`:
  
```latex
\definecolor{seagreen}{rgb}{0.031, 0.251, 0.333} % Main theme color
\definecolor{azurro}{rgb}{0.624, 0.824, 0.996}   % Light blue
\definecolor{uau}{rgb}{0.329, 0.996, 0.859}      % Bright green
\definecolor{rusa}{rgb}{0.914, 0.235, 0.675}     % Pink accent
```

### Example Usage

Here is a simple example of a LaTeX document using Template A:

```late
\documentclass{beamer}
\usepackage[templateA]{beamerthemenilu} % Use Template A (default)

\title{NILU Research Presentation}
\subtitle{Air Pollution Monitoring and Analysis}
\author{John Doe}
\date{\today}

\begin{document}

\begin{frame}
  \titlepage
\end{frame}

\section{Introduction}

\begin{frame}
  \frametitle{Overview}
  \framesubtitle{Scope of Research}
  This is an example slide.
\end{frame}

\end{document}
```

To use Template B instead, just replace the `\usepackage[templateA]{beamerthemenilu}` line with:

```latex
\usepackage[templateB]{beamerthemenilu}
```

### Files

- **beamerthemenilu.sty**: The main style file containing the Beamer theme logic.
- **graphics/**: This folder contains image assets such as logos and background images for the title slides.

### Customizing the Theme

You can modify `beamerthemenilu.sty` to change the following aspects of the theme:
- **Footline**: Customize the footline for either template by modifying the `\setbeamertemplate{footline}` sections.
- **Block Styles**: Modify the appearance of blocks (rounded corners, shadows, etc.) by adjusting the block template:

```latex
\setbeamertemplate{blocks}[rounded][shadow=true]
```
---
## Author
Riccardo Boero - ribo@nilu.no

## License
This template is published under the MIT License. This Beamer theme is not an official NILU product. You are free to extend, modify, and adapt it to your institution’s visual identity and the needs of your presentations.
