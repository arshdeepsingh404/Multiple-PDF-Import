# Multiple PDF Import for AutoCAD

A powerful, high-productivity AutoCAD plugin designed to automate the process of importing multiple PDF files simultaneously. Bypassing the native AutoCAD limitation of importing PDF sheets one-by-one, this tool allows users to bulk-import pages or export them as individual drawings quickly and cleanly.

---

## Key Features

* **Batch PDF Processing**: Import multiple PDF files or select specific page ranges to process from multi-page documents.
* **Smart Geometry Packaging**: Automatically package imported geometries into AutoCAD **Groups** or **Block Definitions** to keep drawings organized.
* **Auto-Arrangement Layout**: Arrange imported pages in clean horizontal or vertical rows based on page sizing parameters and grid offsets.
* **Non-Destructive Individual Exports**: Convert PDF pages directly into separate standalone AutoCAD drawing (`.dwg`) files in a designated folder without altering your active drawing.
* **Multi-Version AutoCAD Support**: Built for AutoCAD versions 2021 through 2027 using target framework outputs for `.NET 4.8`, `.NET 8.0`, and `.NET 10.0`.

---

## Installation & Deployment

### Option 1: Autodesk App Store (Recommended)
1. Download the installer from the **Autodesk App Store**.
2. Run the executable; the installer handles all bundle folder placements and configuration automatically.
3. Open AutoCAD and run the command `MPDFIMPORT`.

### Option 2: Manual Installation (GitHub)
1. Download the `MultiplePDFImport.bundle` folder.
2. Copy the folder to your local Autodesk plugins directory:  
   `%APPDATA%\Autodesk\ApplicationPlugins\`
3. Launch or restart AutoCAD.
4. Click **Always Load** on the security prompt.
5. Enter `MPDFIMPORT` at the command prompt to open the dialog window.

---

## Workflow & Usage

1. **Add PDF Files**: Click **Add PDF Files** to select the documents you want to process. Select duplicates or unneeded files and click **Remove** to exclude them.
2. **Configure Packaging & Range**:
   * **Import each page as Group**: Groups the vectors for each imported page to avoid overlapping lines.
   * **Import each page as Block**: Creates a distinct block definition in the database for each page.
   * **Page Range**: Choose to import all pages or specify a custom range.
3. **Choose Placement Option Mode**:
   * **Insert into Current DWG**: Layout pages in a grid within your active model space. You can select standard paper size formats (ANSI, ISO, ARCH), set max sheets per row, horizontal/vertical spacing offsets, scale, rotation, and specify the insertion point on-screen.
   * **Export as Individual DWGs**: Specify an output folder where the plugin will save each PDF page as its own `.dwg` file (fully non-destructive).
4. **Execute**: Click **Import PDF** to run the batch process. Press the `F1` key at any point in the dialog to open the help documentation.

---

## Supported Options Reference

| Option | Description |
| :--- | :--- |
| **Import each page as Group** | Puts imported geometry for each page into a separate AutoCAD Group, preventing overlapping vector selections. |
| **Import each page as Block** | Creates an AutoCAD Block Definition for each imported page and places references in model space. |
| **All Pages / Custom Range** | Limits import to specific pages of multi-page PDFs. |
| **Imperial / Metric Radios** | Updates the Paper Size dropdown list with appropriate formats (e.g. ANSI/ARCH or ISO formats). |
| **Paper Size ComboBox** | Automatically sets default Width and Height dimensions for calculating positioning. Can also be overridden manually. |
| **Specify insertion point on screen** | When checked, prompts you to select where the drawings should start loading in AutoCAD. When unchecked, uses static X/Y coordinates. |
| **Max drawings in a row** | Wraps layout to start a new row after the specified number of sheets are inserted side-by-side. |
| **Horizontal / Vertical Offset** | Defines horizontal and vertical spacing margins between adjacent sheet frames. |
| **Scale / Rotation** | Sets a scaling factor multiplier and rotation degrees for imported vectors. |

---

## Compatibility Matrix

| AutoCAD Version | internal Series | Target Framework | Runtime Requirement |
| :--- | :--- | :--- | :--- |
| **AutoCAD 2021 – 2024** | `R24.0` – `R24.3` | `net48` | **.NET Framework 4.8** (Legacy) |
| **AutoCAD 2025 – 2026** | `R25.0` – `R25.1` | `net8.0-windows` | **.NET 8.0** (Core) |
| **AutoCAD 2027** | `R26.0` | `net10.0-windows` | **.NET 10.0** (Core) |

---

## Privacy Policy

This plugin operates entirely locally on your workstation. We do not collect, store, or transmit any personal data, telemetry, or drawing information.

For the full detailed terms, please review our [Privacy Policy](PRIVACY.md).

---

## Developer
**Arshdeep Singh**  
Full-Stack Industrial Automation Developer  
*Autodesk Expert Elite* | C. Tech | CMSE® | CAPM®
