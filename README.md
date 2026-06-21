# Multiple PDF Import for AutoCAD

A powerful, high-productivity AutoCAD plugin designed to automate the process of importing multiple PDF files simultaneously. Bypassing the native AutoCAD limitation of importing PDF sheets one-by-one, this tool allows users to bulk-import pages or export them as individual drawings quickly and cleanly.

<br>

<p align="center">
  <img width="80%" height="633" alt="MultiplePDFImport" src="https://github.com/user-attachments/assets/7088e3a6-0254-4707-8b00-c96dc2fadf65" />
</p>

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Key Features

* **Batch PDF Processing**: Import multiple PDF files or select specific page ranges to process from multi-page documents.
* **Smart Geometry Packaging**: Automatically package imported geometries into AutoCAD **Groups** or **Block Definitions** to keep drawings organized.
* **Auto-Arrangement Layout**: Arrange imported pages in clean horizontal or vertical rows based on page sizing parameters and grid offsets.
* **Non-Destructive Individual Exports**: Convert PDF pages directly into separate standalone AutoCAD drawing (`.dwg`) files in a designated folder without altering your active drawing.
* **Multi-Version AutoCAD Support**: Built for AutoCAD versions 2021 through 2027 using target framework outputs for `.NET 4.8`, `.NET 8.0`, and `.NET 10.0`.

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Download from Autodesk App Store
For the simplest experience, download the Custom Object Snap add-in directly from the Autodesk App Store. The installer handles all configuration automatically.

1. Download the installer from the **Autodesk App Store**.
2. Run the executable, and the installer will handle all bundle folder placements and configuration automatically.
3. Open AutoCAD and run the command **MPDFIMPORT**.

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Download from GitHub
If you prefer to manage your plugins manually or are using the version from GitHub, use the Autoloader method. This ensures the add-in is loaded automatically every time you open AutoCAD.

1. Navigate to the Releases tab on the right side of this GitHub repository.
2. Download the **CustomObjectSnap.bundle** zipped folder.
3. Copy and extract the folder to: %APPDATA%\Autodesk\ApplicationPlugins\
4. Launch or restart AutoCAD.
5. Approve the security prompt by clicking “Always Load.”
6. Enter `MPDFIMPORT` at the command prompt to open the dialog window.

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Workflow & Usage

### Step 1: Add PDF Files
Click **Add PDF Files** to select the documents you want to process. Select duplicates or unneeded files and click **Remove** to exclude them.
### Step 2: Configure Packaging & Range
   * **Import each page as Group**: Creates a group for each imported page.
   * **Import each page as Block**: Creates a block for each imported page.
   * **Page Range**: Choose to import all pages or specify a custom range.
### Step 3: Choose Placement Option Mode
   * **Insert into Current DWG**: Layout pages in a grid within your active model space. You can select standard paper size formats, set max sheets per row, horizontal/vertical spacing offsets, scale, rotation, and specify the insertion point on-screen.
   * **Export as Individual DWGs**: Specify an output folder where the plugin will save each PDF page as its own `.dwg` file.
### Step 4: Execute
Click **Import PDF** to run the batch process.

Press the `F1` key at any point in the dialog to open the help documentation.

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

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

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Compatibility Matrix

| AutoCAD Version | Target Framework | Runtime Requirement |
| :--- | :--- | :--- | :--- |
| **AutoCAD 2021 – 2024** | `net48` | **.NET Framework 4.8** (Legacy) |
| **AutoCAD 2025 – 2026** | `net8.0-windows` | **.NET 8.0** (Core) |
| **AutoCAD 2027** | `net10.0-windows` | **.NET 10.0** (Core) |

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Developer
**Arshdeep Singh**<br>
Full-Stack Industrial Automation Developer  
Autodesk Expert Elite | C. Tech | CMSE® | CAPM®

&nbsp;
<p align="center">◈ ◈ ◈</p>
&nbsp;

## Version History
| Version | Date | Changes |
| :--- | :--- | :--- |
| **1.0.0** | June 2026 | Pre Release |
