# Codes Overview:

This project is broken into two sections: Python and R. 

The Python code section has two* types of codes:

1) Code to count the specific color of pixels in an image that matches the color key (see Fig. 3).
2) Code to create new columns and variables (i.e., percent area variables).

*In the process of developing a deep learning algorithm to partially or fully tissue map bone histological images. 

The R code is broken up into five sections:

1) Descriptive Statistics
2) Exploratory Data Analysis
3) Statistical Testing Analysis - ANOVA and Linear Regression
4) Multivariate Analysis - Principal Component Analysis (PCA)
5) Predictive Analysis

# Project Background 

In the field of human evolution, it is common to hear and read that hominins, our early human ancestors, have an 'ape-like' growth pattern. However, visual observations of growth in different ape species (i.e., gorillas, chimpanzees, orangutans, gibbons, etc) show that each ape species have their own unique growth pattern. 

We also know that modern humans have a unique growth pattern--rapid growth as infants, slow growth during childhood followed by a growth spurt during puberty--compared to apes and hominins. 

However, we cannot visually observe the growth patterns in hominins as they are all extinct, and all that remains are parts of their fossilized skeletal systems. 

Luckily for people studying human evolution, the bones of the skeletal system are like tree rings, keeping a record of the individual's growth. We can map the patterns of growth based on how fast or slow bone tissue is deposited in a bone cross-section to understand how an individual grew in life after death (Fig. 1).

Unfortunately, there are few comparative datasets on bone microanatomy from our closest living relatives--apes and monkeys--and few comparative analyses of bone microanatomy growth patterns between ape species (McFarlin *et al.*, 2016; Tuosto *et al*., 2019).  

Understanding the growth pattern differences in our closest living primate relatives can help us determine the potential growth patterns our early human ancestors followed.

##Add image of bone cross-section

# Project Objective
The objective of this project is to determine if nonhuman primates (i.e., monkeys, chimpanzees, gibbons, etc) have evidence of similar bone growth patterns as modern humans (i.e., fast-slow-fast growth pattern) from their bone microstructure during bone growth or if this growth pattern is unique to humans. 

## Image and data used for practice  

**Python Image**
The image provided for the Python code is a random bone histological image that was mapped by K. Tuosto and is not part of the images used for the project publication (Tuosto *et al.*, *in prep*).

**R Data**
The data provided for practice is simulated data of the data currently being prepared for publication (Tuosto *et al.*, *in prep*). 
 
# Code
The code is broken up into 4 sections:

1. Pixel color count code - Code that calculates the number of pixels in an image (practice image provided), and provides a data frame with the pixel counts.
2. Bone tissue type proportions - Code that calculates proportions of the bone tissue types from the raw pixels. 
3. Plot bone tissue proportions - Code that plots bone tissue proportion by species, age group, and sex separated and combined. 
4. Principal component analysis (PCA) - PCA code to visualize and summarize the variance within species, and detect broad species patterns of bone tissue types proportions.

### Tissue Mapping
Please refer to McFarlin *et al*., 2006/McFarlin *et al.*, 2008, and McFarlin *et al.*, 2016 publications for information on how to tissue map cortical bone (Fig. 3).

Or if you would like guidance on the tissue mapping method, please feel free to contact me on GitHub. 

![TissueMappingColorCodes](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/433b407c-b49f-462d-84ab-e7fd762e6fc8)
Fig. 3 Example of cortical bone tissue type mapping. For cortical bone tissue mapping you will need a brightfield (LM) and circularly-polarized light (CPL) or polarized light (PL) images layered on top of each other with the CPL/PL at a reduced opacity. Mapping of the various tissue types should be done in their own layer. Note, interstitial bone tissue (INT) is missing from the color table (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa).

# Code sections

## Packages used in code
- raster 
- pander
- ggplot2
- dummies

## 1 First code section
The first code section/function (PixelCount) reads in the PNG file and calculates the number of pixels for each tissue map color, and returns a gradient map and value data frame table with 2 variables (Var1 & Freq) and 13 objects (i.e., tissue types + background color).

The 13 object numbers in Var1 correspond to these cortical bone tissue types.

**Note: Because the image file types tend to be massive (even after reducing file size) and can take a relatively long time computing pixel number, the current code is for one image at a time, however, it is possible to apply this code in a loop.** 

The second part of this code changes the structure of the data out put from long data to wide data, adds a column for individual ID, and renames the columns to the specific bone tissue type. 

The third part of this code combines the data frames from each image into one data frame and exports it as a excel file. 

## 2 Second code section
The second code section calculates total cortical bone area from the raw pixel numbers and transforms the raw pixel numbers into proportions for each bone tissue type, providing us with information of the make up of the bone microstructure. 

## 3 Third code section
Plot bone tissue propotions

#Working on this still!
