
Following is the description of use cases with data needs and sources. 

Contributors are asked to copy the template and add their use case to the document. 

## Use case template

Segmenting clear-sky-ocean versus everything else of Sentinel-3 SLSTR data with the Prithvi-EO 2.0 Foundation Model. 

### Contact
Boran Frank, LinkedIn

### Used training data

Please copy the underlying table for each used dataset and fulfil from applicable parts. Don't worry! It does not need to be complete! 

Please note that also non-publicly available datasets are in scope as well.

| Topic | Content |
|-------|---------|
| **Data source** | Input: .SEN3 from EUMETSAT data store via eumdac, Target: Binary Mask via Naive Probabilistic Cloud Mask from EUMETSAT RSP |
| **Data content** <br> (parameters / products / levels / etc.) | S3B SLSTR channel 1-6 in .SEN3 format, nadir view |
| **Geospatial resolution**| 500 m |
| **Temporal resolution**| |
| **Data format**| various NetCDF inside .SEN3 |
| **Preferred data format** | GeoTiff (georeferenced and on regular grid) |
| **Preferred data access mechanism** | |
| **Data preprocessing** | Python: Radiance to Reflectance, regridding to regular grid in order to export as GeoTiff |
| **Reason for usage** | We wanted to test the performance of the Prithvi-EO Foundation Model, which was trained on higher resolution Sentinel-2 data with lower resolution Sentintel-3 data.  |
| **Challenges** | It is possible to download Sen-3 as GeoTiff from eumdac (+ data tailor), but then all the required data for the radiance to reflectance data is lost. Also: I created the target data (clear-sky-ocean mask) myself from the .SEN3 file, which I also had to transform into GeoTiff. So as I don't know the transformation that is done inside eumdac, I needed to transform both the input and the target myself in order to do it consistently. |

### Missing data

Please describe which data are you missing / which data you believe would make usage better. 

| Topic | Content |
|-------|---------|
| **Explanation** | SEN3 TOA reflectance | 
| **Data content** <br> (parameters / products / levels / etc.) | All bands for which this transformation is possible. |
| **Geospatial resolution**| 500 m |
| **Temporal resolution**|  |
| **Preferred data format** | GeoTiff |
| **Preferred data access mechanism** |  |


