# Satellite-Image-Mosaic
This project conducts the realization of algorithms for creation of seamless satellite image mosaic. 
It can be divided into 3 main steps:
Pre-Processing the data, Merging or Creation of mosaic, Post-Processing
The step by step project completions can be describes as following:
Data acquisition and management:

● Gather Sentinel-2 L2A images covering the target region.
● Ensure images are in JP2 format, merging different spectral bands to achieve coherent and accurate visualization.
Organize and preprocess the images:
● Reproject all images to a common Coordinate Reference System (CRS). In this case, EPSG:32632 was chosen, and a function (reproject_img) was implemented to ensure all images align with this system.
● Equalization of the resolution of the data to ensure proper overlap and seamless integration into the final mosaic.
● Applying various SCL mask classes, to reduce visual defects.
Image Merging:
● Develop and implement a Python-based pipeline using libraries like rasterio and gdal to merge the individual images.
● Minimize issues such as black edges or triangular gaps, which arise due to differences in image geometry.
● Resolve problems of image misalignment and ensure accurate spatial representation.
Postprocessing and Optimization:
● Compressing the mosaic, in order to optimize its usage.
● Visualizing the mosaic to determine the quality.
