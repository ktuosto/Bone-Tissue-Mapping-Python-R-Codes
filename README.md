# Cortical_bone_tissue_type_calculation

This code is used to calculate the pixel amount of different cortical bone tissue types after a bone section has been mapped following McFarlin et al., 2016 method, basic statistical analysis (i.e., mean, standard deviation, principal component analysis - PCA) of tissue types between age groups within a species and between species, and basic data visualization.

# Project Objective
Examine patterns of bone microstructural development in wild *Gorilla beringei beringei* (Virunga mountain gorillas) and compare with an existing data set on wild *Hylobates lar* (white-handed gibbon) and *Pan troglodytes* (common chimpanzee), to build a comparative foundation for understanding the evolution of growth and development in the human fossil record.

![primates](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/a15b8fd3-913e-416b-95cc-6cd5bdd731ef)
Fig. 1 Images of the three wild represenative of apes used in this study (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa). 

## Background 
Modern humans have a unique life history pattern, characterized by slow body growth during childhood followed by accelerated growth during adolescence. This is evidenced by deposition of fast-forming fibro-lamellar bone during infancy and adolescence, and the absence of this tissue type during childhood (Fig. 2) (Goldman *et al.*, 2009).

However, there are few comparative data on bone microanatomy from our closest living relatives, the apes. Such data would allow us to understand whether this pattern is unique to humans, and if so, better interpret fossil evidence of its evolution (McFarlin *et al.*, 2016).

![Growth pic2](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/e91914cb-7b30-4c15-8d40-c0a1b425d058)
Fig. 2 Modern human bone growth microstructural pattern. Bone microstructure from McFarlin *et al.*, 2016 (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa). 

## Data used for practice  
The data provided for practice is not the exact same data used for the project, which is currently being prepared for publication (Tuosto *et al.*, *in prep*). 

The data is from a selcet few primates from McFarlin 2006, McFarlin *et al.*, 2008 and McFarlin *et al.*, 2016 publications. 

## Image preperation 
Prior to using this code to calculate tissue types, make sure when hand mapping tissue types in Adobe Photoshop, Gimp, or other image-editing sowftware the Pencil Tool is at a hardness level of 100%, otherwise you will have thousands of different pixel colors vs the 13 tissue mapping colors. 

If you still have more then the 13 tissue mapping colors, even after you confirmed the Pencil Tool's hardness level was at 100%, it is most likely that you have un-tissue mapped/un-colored areas. 

Cortical bone tissue map images must be flatten and converted into a PNG file.

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
The first code section/function (PixelCount) reads in the PNG file and converts the image into grayscale, calculates the number of pixels for each tissue map color, and returns a gradient map and value data frame table with 2 variables (Var1 & Freq) and 12 objects (i.e., tissue types + background color).

The 13 object numbers in Var1 correspond to these cortical bone tissue types:

Background
- 255 - White background

Periostseal origin tissue
- 43 - Fibro-lamellar complex (FLC)
- 57 - Transitional Fibro-lamellar complex (FLC-LZPO)
- 80 - Parallel-fiered (PF)
- 99 - Transitional Parallel-fiered to Lamellar (PF-LAM)
- 154 - Lamellar (LAM)

Endosteal origin tissue 
- 121 - Parallel-fiered (EPF)
- 145 - Transitional Parallel-fiered to Lamellar (EPF-LAM)
- 162 - Lamellar (ELAM)
- 134 - Compacted Coarse Cancellous (ECC)

Other tissue types
- 97 - Osteonal tissue (HAV)
- 226 - Sharpey's fiber (SF)
- 200 - Interstitial bone tissue (INT)

Note: Because the image file types tend to be massive (even after reducing file size) and can take a relatively long time computing pixel number, the current code if for one image at a time, however, it is possible to apply this code in a loop. 

## 2 Second code section
The second code section changes... 

# Working on!
