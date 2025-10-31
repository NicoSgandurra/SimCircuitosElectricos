# Oswald Triangle Simulator

A comprehensive single-file web application for combustion analysis using the Oswald Triangle method.

## Overview

The Oswald Triangle is a graphical method used in combustion engineering to analyze fuel combustion efficiency and determine optimal air-fuel ratios. This simulator provides an interactive tool for engineers and students to visualize and analyze combustion processes.

## Features

### 🔥 **Core Functionality**
- **Single HTML File**: Complete implementation with inline CSS and vanilla JavaScript
- **No External Dependencies**: Runs entirely in the browser without external libraries
- **Bilingual Support**: Spanish (ES) and English (EN) with persistent language selection
- **Real-time Calculations**: Instant computation of combustion parameters
- **High-Quality Export**: Download charts as high-resolution JPEG images

### 📊 **Oswald Triangle Analysis**
- **Point Definitions**:
  - **Point A**: (21% O₂, 0% CO₂) - Maximum excess air condition
  - **Point C**: (0% O₂, kCO₂%) - Complete combustion, no excess air
  - **Point D**: (qO₂%, 0% CO₂) - Incomplete combustion limit
  - **Experimental Point**: From Orsat analysis data
  - **D⊥ Point**: Perpendicular intersection for analysis

- **Lines and Relationships**:
  - **Line AC**: Complete combustion line (blue, solid)
  - **Line CD**: Incomplete combustion line (orange, solid)
  - **Perpendicular D⊥AC**: Green dashed line from D perpendicular to AC

### 🧮 **Mathematical Calculations**
- **Fuel Composition Analysis**: C, H, O, N, S, H₂O percentages
- **Orsat Data Processing**: CO₂ and O₂ measurements
- **Key Parameters**:
  - kCO₂: Maximum CO₂ percentage in dry flue gas
  - qO₂: Oxygen percentage for incomplete combustion
  - pCO: CO percentage for incomplete combustion
  - Excess air calculations
  - Combustion efficiency metrics

### 🎨 **Visual Features**
- **1:1 Aspect Ratio**: True square geometry maintained at all sizes
- **High Contrast Colors**: Optimized for visibility and printing
- **Dynamic Margins**: Automatic calculation to prevent text clipping
- **Semantic Labels**: Human-readable point descriptions
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Fullscreen Mode**: Expanded view for detailed analysis

## Usage

### Getting Started
1. Open `oswald.html` in any modern web browser
2. The simulator loads with default values and displays the chart immediately
3. Modify fuel composition and Orsat data as needed
4. Click "Calcular" (Calculate) to update the analysis

### Default Values
- **Fuel Composition**: 85% C, 12% H, 2% O, 0.8% N, 0.2% S, 0% H₂O
- **Orsat Data**: 9.8% CO₂, 4.8% O₂

### Controls
- **Calcular/Calculate**: Compute combustion parameters
- **Ver Gráfico/View Chart**: Display the Oswald Triangle
- **Limpiar/Clear**: Reset all input fields
- **Pantalla Completa/Fullscreen**: Expand chart for detailed view
- **Descargar JPG/Download JPG**: Export chart as high-quality image
- **ES/EN Toggle**: Switch between Spanish and English

### Input Parameters

#### Fuel Composition (%)
- **Carbon (C)**: Carbon content in fuel
- **Hydrogen (H)**: Hydrogen content in fuel
- **Oxygen (O)**: Oxygen content in fuel
- **Nitrogen (N)**: Nitrogen content in fuel
- **Sulfur (S)**: Sulfur content in fuel
- **Water (H₂O)**: Moisture content in fuel

#### Orsat Analysis Data (%)
- **CO₂ Measured**: Carbon dioxide percentage in dry flue gas
- **O₂ Measured**: Oxygen percentage in dry flue gas

## Technical Implementation

### Architecture
- **Single File Design**: All code contained in one HTML file
- **Vanilla JavaScript**: No external frameworks or libraries
- **Canvas Rendering**: High-performance 2D graphics using HTML5 Canvas
- **CSS Grid Layout**: Responsive design with modern CSS

### Mathematical Model
The simulator implements the complete Oswald Triangle methodology:

```javascript
// Key calculations
H_available = moles.H - 2 × moles.H₂O
O₂_complete = moles.C + H_available/4 + moles.S - moles.O/2
O₂_incomplete = moles.C/2 + H_available/4 + moles.S - moles.O/2

// Perpendicular line mathematics
m_AC = -kCO₂_frac / 0.21
m_perp = 0.21 / kCO₂_frac
```

### Canvas Rendering Features
- **Dynamic Margins**: Automatic calculation based on text dimensions
- **1:1 Aspect Ratio**: Ensures accurate geometric relationships
- **High-DPI Support**: Crisp rendering on high-resolution displays
- **Anti-aliasing**: Smooth lines and text rendering

## Browser Compatibility

- **Chrome**: 60+
- **Firefox**: 55+
- **Safari**: 12+
- **Edge**: 79+

## File Structure

```
oswald.html          # Complete single-file application
README.md           # This documentation file
```

## Language Support

The application supports two languages with complete UI translation:

### Spanish (ES) - Default
- Interface labels in Spanish
- Axis titles: "% O₂ (volumen)", "% CO₂ (volumen)"
- Button labels: "Calcular", "Ver Gráfico", "Limpiar", etc.

### English (EN)
- Interface labels in English
- Axis titles: "% O₂ (volume)", "% CO₂ (volume)"
- Button labels: "Calculate", "View Chart", "Clear", etc.

Language preference is automatically saved and restored on subsequent visits.

## Export Features

The **Download JPG** function provides:
- High-resolution export (uses device pixel ratio)
- Solid white background for printing
- Complete chart with all visual elements
- Filename: `oswald-triangle.jpg`

## Educational Use

This simulator is ideal for:
- **Engineering Students**: Learning combustion analysis principles
- **Combustion Engineers**: Quick analysis and verification
- **Research**: Comparative studies and parameter optimization
- **Training**: Interactive demonstration of Oswald Triangle concepts

## Technical Notes

### Coordinate System
- **Display**: 0-21% on both axes for user clarity
- **Internal**: 0-0.21 fractions for mathematical precision
- **Mapping**: Linear transformation between display and calculation coordinates

### Perpendicular Validation
The simulator validates perpendicularity with high precision:
```javascript
perpendicular_check = |m_AC × m_perp + 1| < 1e-6
```

### Performance Optimization
- Efficient canvas rendering with minimal redraws
- Optimized mathematical calculations
- Responsive design with hardware acceleration

## License

This project is provided as-is for educational and professional use in combustion analysis.

## Version History

- **v1.0**: Initial release with complete Oswald Triangle implementation
- **v1.1**: Added bilingual support and improved UI
- **v1.2**: Enhanced canvas rendering and export functionality
- **v1.3**: Improved layout, clipping fixes, and semantic labels

---

**Created by**: Rubio, Pablo and Sgandurra, Nicolas
**Last Updated**: 09-27-2025  
**File Size**: ~45KB (complete single-file implementation)
