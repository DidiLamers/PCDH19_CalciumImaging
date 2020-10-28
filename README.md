# CalciumImaging

## General Information
This folder contains all the code I used to analyse the calcium imaging data for my PhD thesis on PCDH19. 
imageGateway.m is the main program, written by Gian Michele Ratto. All other functions in the folder are called by imageGatway.

The other program contained in this folder is particleanalysisdidi.m, written by me to process calcium transients.

## Use in PCDH19 project
In my work I used imageGateway to obtain a binarised version of my calcium imaging data. 

## Usage
ImageGateway allows importation of tiff and multi-tiff imaging data, then binning of the data and dF/F computation. It outputs a binarised version of the 
data based on the statistics of the dF/F process: in the absence of any calcium activity, dF/F will be normally distributed. Calcium activity, then, appears
as a tail on the right side of the distribution. In imageGateway, the user can choose a threshold at x times the standard deviation of the Gaussian 
distribution of the dF/F process. Pixels of each frame will then be labelled as either ‘0’ when below the threshold or ‘1’ if over the threshold. In this
way, the binarised stack contains only physiologically relevant events. Further restraints based on minimum size and time points of the remaining pixels
can be added. 

particleanalysisdidi.m takes detected calcium transients (based on the binarised image from imageGateway) and detected up states from LFP data as an input
and outputs quantifications of transients and their occurence within up states. 
The comments on the top of the program explain its functioning and required inputs in more detail. 

## Contributors
Gian Michele Ratto has written imageGateway, with inputs from Emanuele Paoli and Olga Cozzolino. abfload.m is an already existing Matlab function
(not written by us).

particleanalysisdidi.m is written by me. 

## Dependencies
The Image Processing Toolbox is required to use ImageGateway. 





