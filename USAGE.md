# Usage Guide

## Getting Started

This tool analyzes PDF files to provide detailed information about page dimensions, DPI, and print suitability.

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Active internet connection (to load pdf.js from CDN)

### Quick Start

1. Open `index.html` in your web browser
2. Upload a PDF file using one of these methods:
   - Click the upload area
   - Drag and drop a PDF file onto the upload area
3. Wait for the analysis to complete
4. Review the results for each page

## Understanding the Results

### Document Summary

At the top of the results, you'll see three key statistics:

- **Total Pages**: The number of pages in your PDF
- **Print Ready**: Pages with DPI ≥ 300 (suitable for printing)
- **Low DPI Warning**: Pages with DPI < 300 (not recommended for printing)

### Page Analysis

Each page card shows:

#### Status Badge
- **High Quality** (Green): DPI ≥ 600 - Excellent for professional printing
- **Print Ready (Min)** (Yellow): 300 ≤ DPI < 600 - Acceptable for printing
- **Low Quality** (Red): DPI < 300 - Not recommended for printing

#### Orientation
- **Portrait**: Height > Width
- **Landscape**: Width > Height  
- **Square**: Width = Height

#### DPI (Dots Per Inch)
- **Horizontal DPI**: Resolution in the horizontal direction
- **Vertical DPI**: Resolution in the vertical direction
- **Average DPI**: Mean of horizontal and vertical DPI

#### Dimensions

Your page dimensions are shown in four different units:

1. **Pixels (px)**: Screen resolution
2. **Points (pt)**: PDF native unit (72 points = 1 inch)
3. **Inches (in)**: Imperial measurement
4. **Millimeters (mm)**: Metric measurement

#### Print Quality Warning/Info

Based on the DPI, you'll see one of:
- **Excellent Print Quality**: Your page exceeds recommended standards
- **Minimum Print Quality**: Your page meets minimum standards but could be better
- **Low DPI Warning**: Your page may not print well

## Common Page Sizes

Here are some standard page sizes for reference:

### US Paper Sizes
- **Letter**: 8.5 × 11 inches (215.9 × 279.4 mm)
- **Legal**: 8.5 × 14 inches (215.9 × 355.6 mm)
- **Tabloid**: 11 × 17 inches (279.4 × 431.8 mm)

### International (ISO) Paper Sizes
- **A4**: 210 × 297 mm (8.27 × 11.69 inches)
- **A3**: 297 × 420 mm (11.69 × 16.54 inches)
- **A5**: 148 × 210 mm (5.83 × 8.27 inches)

## DPI Guidelines

### Recommended DPI by Use Case

- **Web/Screen Display**: 72-96 DPI
- **Basic Home Printing**: 150-200 DPI
- **Good Quality Printing**: 300 DPI (minimum standard)
- **Professional/Commercial Printing**: 600+ DPI
- **High-End Publications**: 1200+ DPI

### Why DPI Matters

DPI (Dots Per Inch) determines how many pixels are packed into each inch of your document when printed:

- **Higher DPI** = More detail and sharper prints
- **Lower DPI** = Less detail, potential pixelation when printed

A PDF with 72 DPI will look fine on screen but may appear blurry or pixelated when printed, especially at larger sizes.

## Tips for Best Results

1. **Always check DPI** before sending documents to print
2. **Re-create low DPI documents** at higher resolution if possible
3. **Consider your output size** - Larger prints need higher DPI
4. **Screen vs Print** - Remember that screen display (72-96 DPI) looks different from print (300+ DPI)

## Troubleshooting

### "PDF.js Library Not Loaded" Error

This error appears when:
- You don't have an internet connection
- Content blockers are preventing CDN access
- Corporate firewall is blocking external resources

**Solutions:**
1. Ensure you have an active internet connection
2. Temporarily disable ad blockers or content blockers
3. Check your firewall settings
4. Reload the page after making changes

### File Upload Doesn't Work

If file upload fails:
1. Ensure you're selecting a valid PDF file
2. Check that the PDF isn't password-protected
3. Try a smaller PDF file first
4. Check browser console for error messages (F12 → Console tab)

### Unexpected Results

If the analysis seems incorrect:
- Some PDFs may have unusual internal dimensions
- Scanned documents may report DPI differently than designed PDFs
- Vector-based PDFs may show different DPI than raster-based PDFs

## Demo Mode

If you can't load `index.html` with internet access, you can view `demo.html` to see what the tool looks like with sample data. This demo doesn't require pdf.js and shows the UI with three example pages.

## Privacy

This tool runs entirely in your browser:
- No files are uploaded to any server
- All processing happens locally on your device
- No data is collected or transmitted
- Your PDFs remain completely private
