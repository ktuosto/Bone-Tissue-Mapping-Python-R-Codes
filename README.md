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
The objective of this project is to explore the differences in growth patterns in primate microanatomy and build a predictive model to provide the probability of a new tissue map growing more like which primate.

# Code Sections

### Python Section 1: Count Pixels
This code will count the number of pixels of the specific colors in the bone maps and provide the pixel results as a table.

### Python Section 2: Create New Variables
This code will calculate the proportions of the bone tissue types from the raw pixels and create 4 new variables from the existing variables, C.Ar, %CA, %PCA, and %ECA (see Data Description for more information). Converting the raw pixel values into proportions allows us to control for body size differences between the primates and image size differences. 

### R Section 1: Descriptive Statistics
### R Section 2: Exploratory Data Analysis
### R Section 3: Statistical Testing Analysis - ANOVA and Linear Regression

### R Section 4: Multivariate Analysis - Principal Component Analysis (PCA)
Principal component analysis (PCA) was done to visualize and summarize the variance within species differences by age and sex and to detect broad species growth pattern differences.

### R Section 5: Predictive Analysis

# Data set:

simulation_primate_bone.csv

# Data Description:

**Python Image**
The image provided for the Python code is a random bone histological image that was mapped by K. Tuosto and is not part of the images used for the project publication (Tuosto *et al.*, *in prep*).

**R Data**
The data provided for practice is simulated data of the data currently being prepared for publication (Tuosto *et al.*, *in prep*). There are #  observations and 20 variables.

**Note: Genus has been modified for the practice set.**

1) GENUS = Ape 1, Ape 2, Ape 3, Monkey 1
2) SEX = M (male), F (female), U (unknown)
3) AGE = Ages based on dental eruption and skeletal fusion, 6 age classes from youngest to oldest: PDICED, DECID, M1, M2, M3, EPIPH
4) WOV = Fastest forming bone regardless of bone cortex, mostly observed on the outer cortex
5) FLC = Fast-forming bone regardless of bone cortex, mostly observed on the outer cortex
6) FLC-LZPO = Fast-forming bone transitioning to slower-forming bone on the outer cortex 
7) PF = Moderate speed forming bone on the outer cortex 
8) PF-LAM	= Slow-forming bone on the outer cortex
9) LAM = Slowest forming bone on the outer bone cortex 
10) ECCC = Transition bone type 
11) EPF = Moderate speed forming bone on the inner cortex 
12) EPF-LAM = Slow-forming bone on the inner cortex
13) ELAM = Slowest forming bone on the inner bone cortex 
14) SP = Muscle attachment fibers 
15) INTER = Bone tissue in-between osteonal bone tissue 
16) HAV = Osteonal bone tissue 
17) C.Ar = Cortical bone area 
18) %CA = Percent cortical bone area 
19) %PCA = Percent periosteal cortical bone area (i.e., outer bone cortex)
20) %ECA = Percent endosteal cortical bone area (i.e., inner bone cortex)

**For a description of each bone tissue type, see the supplemental materials from McFarlin *et al.*, 2016.**

# Tissue Mapping
Please refer to McFarlin *et al*., 2006/McFarlin *et al.*, 2008, and McFarlin *et al.*, 2016 publications for information on how to tissue map cortical bone (Fig. 2).

Or if you would like guidance on the tissue mapping method, please feel free to contact me on GitHub. 

![TissueMappingColorCodes](https://github.com/ktuosto/Cortical_bone_tissue_type_calculation/assets/49923281/433b407c-b49f-462d-84ab-e7fd762e6fc8)
Fig. 2 Example of cortical bone tissue type mapping. For cortical bone tissue mapping you will need a brightfield (LM) and circularly-polarized light (CPL) or polarized light (PL) images layered on top of each other with the CPL/PL at a reduced opacity. Mapping of the various tissue types should be done in their own layer. Note, interstitial bone tissue (INT) is missing from the color table (Tuosto *et al*., 2019 poster presentation at the International Symposium on Palaeohistology, South Africa).
