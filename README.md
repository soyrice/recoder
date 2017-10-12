# recoder
Standardize and map future land use data with ArcPy

# About

This tool standardizes land use/land cover data from various sources. It uses `openpyxl` to read data from an Excel sheet and runs as an ArcGIS geoprocessing tool to re-code land use/land cover attributes.

See [Google Drive](https://drive.google.com/file/d/0BzpR0X1lXypvVTBTOVpmNWt4OUU/view?usp=sharing) to preview the template Excel sheet, or clone repository to save the Excel template locally.

<details>
<summary>
Click the dropdown to get more background on the project
</summary>

<p>
This tool was developed for the Rhode Island Statewide Planning Program to build a composite future land use map. Municipalities designate their own future land use classes, so to analyze differences between municipal future land use trends land use classes need to be standardized. Often municipal land use data is too big to edit manually, so a geoprocessing tool automates the data management and processing.

`Openpyxl` is used to get cell values from the template sheet, but the tool can be edited to handle various formats and write back to the sheet. `Openpyxl` is used for flexibility, but Pandas can also be used in this format.
</p>
</details>

# Installation

* Add `recoder.py` to a new [ArcGIS script tool](http://pro.arcgis.com/en/pro-app/help/analysis/geoprocessing/basics/create-a-python-script-tool.htm)

* Create 6 input parameters from comments
```python
# name = Excel worksheet, type = any value
# name = Excel column name, type = string
# name = Input workspace, type = workspace
# name = Input features, type = feature class
# name = Field name, type = field, dependency = Input features
```
* Upload `landuse.xlsx` to geoprocessing tool
