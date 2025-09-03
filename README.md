# QuickCoord
QuickCoord v4

A QGIS plugin for digitizing, editing, and previewing polygons by entering coordinate pairs.
Supports automatic CRS transformations, live preview, and attribute form integration.

📌 Features
1. Coordinate-Based Digitizing
Enter X / Y coordinates manually in the input table.
Instantly visualize the polygon on the map canvas.
Works seamlessly with polygon layers only.
2. Live Preview
Real-time polygon preview using QgsRubberBand.
Zooms to polygon automatically when you click Preview.
3. Commit with Attribute Form
Clicking Commit:
Starts edit mode automatically.
Adds or updates the polygon geometry.
Opens the attribute form for entering feature details.
Keeps the layer editable after committing.
Triggers a layer repaint immediately.
4. CRS Transformation
Automatically converts between:
UTM Zone 31N → UTM Zone 32N
UTM Zone 32N → UTM Zone 31N
Handles mixed-coordinate digitizing seamlessly.
Input CRS selectable: EPSG:32632 (default), EPSG:32631, or EPSG:4326.
5. Auto Reset
Reset button clears the coordinate table and resets Input CRS → EPSG:32632.
Polygon preview and cached transformations are cleared.
6. Table Management
Add / Remove / Reorder vertices with buttons.
Automatic coordinate updates in preview.

📦 Installation
Method 1 — From ZIP (Recommended)
Download
In QGIS, go to Plugins → Manage and Install Plugins.
Click Install from ZIP.
Browse to the ZIP file → Click Install Plugin.
Enable QuickCoord from the Installed tab.
Method 2 — Manual Installation
Unzip the downloaded file.

🛠️ Usage
Open QuickCoord from the toolbar or Plugins menu.
Select a polygon layer from the dropdown.
Enter coordinates into the table.
Choose the input CRS:
Default: EPSG:32632 (UTM Zone 32N)
EPSG:32631 (UTM Zone 31N)
EPSG:4326 (Lat/Long)
Click Preview → Zooms and shows polygon on the map.
Click Commit:
Saves the polygon.
Opens the attribute form for data entry.
Keeps layer in edit mode.
Use Reset to clear and restore default settings.
🔄 CRS Handling
Default Input CRS → EPSG:32632
Supports on-the-fly transformations between:
Input CRS → Layer CRS → Canvas CRS
Always ensures polygons align with the target layer’s coordinate system.
