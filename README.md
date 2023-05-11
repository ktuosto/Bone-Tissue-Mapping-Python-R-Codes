# Cortical_bone_tissue_type_calculation

This code is used to calculate the pixel amount of different cortical bone tissue (tissue that makes up bone) types after a bone section has been mapped following McFarlin et al., 2016 method, basic statistical analysis (i.e., mean, standard deviation, principal component analysis - PCA) of tissue types between age groups within a species and between species, and basic data visualization.

# Project Background 
Modern humans have a unique life history pattern, characterized by slow body growth during childhood followed by accelerated growth during adolescence. This is evidenced by deposition of fast-forming fibro-lamellar bone during infancy and adolescence, and the absence of this tissue type during childhood (Fig. 2) (Goldman *et al.*, 2009).

However, there are few comparative data on bone microanatomy from our closest living relatives, the nonhuman primates, monkeys and apes. Such data would allow us to understand whether this pattern is unique to humans, and if so, provide a better understanding of the evolution of this growth pattern in the human fossil record (McFarlin *et al.*, 2016).

![Growth pic2](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/e91914cb-7b30-4c15-8d40-c0a1b425d058)
Fig. 1 Modern human bone growth microstructural pattern. Bone microstructures from McFarlin *et al.*, 2016 (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa). 

# Project Objective
The objective of this project is to determine if nonhuman primates (i.e., monkeys, chimpanzees, gibbons, etc) have evidence of similar bone growth patterns as modern humans (i.e., fast-slow-fast growth pattern) from their bone microstructure during bone growth or if this growth pattern is unique to humans. 

## Data used for practice  
The data provided for practice is not the exact same data used for the project, which is currently being prepared for publication (Tuosto *et al.*, *in prep*). 

The data is from a selcet few primates from McFarlin 2006, McFarlin *et al.*, 2008 and McFarlin *et al.*, 2016 publications. 

Images provided for the pixel color count code are sample images and not from the actual primates used in this study. 

# Code
The code is broken up into 4 sections:

1. Pixel color count code - Code that calculates the number of pixels in an image (practice image provided), and provides a data frame with the pixel counts.
2. Bone tissue type proportions - Code that calculates proportions of the bone tissue types from the raw pixels. 
3. Plot bone tissue propotions - Code that plots bone tissue proportion by spieces, age group, and sex separated and combined. 
4. Principal component analysis (PCA) - PCA code to visualize and summarize the variance within spieces, and detect broad species patterns of bone tissue types proportions.

## Image preperation 
Prior to using this code to calculate tissue types, make sure when hand mapping tissue types in Adobe Photoshop, Gimp, or other image-editing sowftware the Pencil Tool is at a hardness level of 100%, otherwise you will have thousands of different pixel colors vs the 13 tissue mapping colors. 

If you still have more then the 13 tissue mapping colors, even after you confirmed the Pencil Tool's hardness level was at 100%, it is most likely that you have un-tissue mapped/un-colored areas. 

Cortical bone tissue map images must be flatten, converted into a PNG file, and in grayscale. 

### Tissue Mapping
Please refer to McFarlin *et al*., 2006/McFarlin *et al.*, 2008, and McFarlin *et al.*, 2016 publications for information on how to tissue map cortical bone (Fig. 3).

Or if you would like guidance on the tissue mapping method, please feel free to contact me on GitHub. 

![TissueMappingColorCodes](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/433b407c-b49f-462d-84ab-e7fd762e6fc8)
Fig. 3 Example of cortical bone tissue type mapping. For cortical bone tissue mapping you will need a brightfield (LM) and circularly-polarized light (CPL) or polarized light (PL) images layered ontop of each other with the CPL/PL at a reduced opacity. Mapping of the various tissue types should be done in their own layer. Note, interstitial bone tissue (INT) is missing from color table (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa).

# Code sections

## Packages used in code
- raster 
- pander
- ggplot2
- dummies

## 1 First code section
The first code section/function (PixelCount) reads in the PNG file and calculates the number of pixels for each tissue map color, and returns a gradient map and value data frame table with 2 variables (Var1 & Freq) and 13 objects (i.e., tissue types + background color).

The 13 object numbers in Var1 correspond to these cortical bone tissue types.

Note: Because the image file types tend to be massive (even after reducing file size) and can take a relatively long time computing pixel number, the current code is for one image at a time, however, it is possible to apply this code in a loop. 

The second part of this code changes the structure of the data out put from long data to wide data, adds a column for individual ID, and renames the columns to the specific bone tissue type. 

The third part of this code combines the data frames from each image into one data frame and exports it as a excel file. 

## 2 Second code section
The second code section calculates total cortical bone area from the raw pixel numbers and transforms the raw pixel numbers into proportions for each bone tissue type, providing us with information of the make up of the bone microstructure. 

## 3 Third code section
Plot bone tissue propotions

#Working on this still!
