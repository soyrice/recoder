# recoder
Standardize and map future land use data with ArcPy

# About

<details>
<summary>
This tool standardizes land use/land cover data from various sources. It uses `openpyxl` to read data from an Excel sheet and runs as an ArcGIS geoprocessing tool to re-code land use/land cover attributes.
</summary>

<p>
<br>
This tool was developed for the Rhode Island Statewide Planning Program to build a composite future land use map. Municipalities designate their own future land use classes, so to analyze differences between municipal future land use trends land use classes need to be standardized. Often municipal land use data is too big to edit manually, so a geoprocessing tool automates the data management and processing.

`Openpyxl` is used to get cell values from the template sheet, but the tool can be edited to handle various formats and write back to the sheet. `Openpyxl` is used for flexibility, but Pandas can also be used in this format.
</p>
</details>

See [Google Drive](https://drive.google.com/file/d/0BzpR0X1lXypvVTBTOVpmNWt4OUU/view?usp=sharing) to preview the template Excel sheet or clone repository to save the Excel template locally.

# Install

* Add `recoder.py` to a new [ArcGIS script tool](http://pro.arcgis.com/en/pro-app/help/analysis/geoprocessing/basics/create-a-python-script-tool.htm)

* Create the 6 input parameters from the comments:
```python
# name = Excel worksheet, type = any value
# name = Excel column name, type = string
# name = Input workspace, type = workspace
# name = Input features, type = feature class
# name = Field name, type = field, dependency = Input features
```

![](https://user-images.githubusercontent.com/22160049/31854162-18cc0c52-b663-11e7-9b22-ebb348f7504f.png)

# Try it out

After building the ArcGIS script tool, fill out `landuse.xlsx` with your local and general land use measures:

![](https://user-images.githubusercontent.com/22160049/31854150-f27f426c-b662-11e7-8c72-9f0c96f7687d.png)

Run the tool and view the changes:

![](https://user-images.githubusercontent.com/22160049/31854138-d8e7d756-b662-11e7-9972-229713a8d5e9.png)

