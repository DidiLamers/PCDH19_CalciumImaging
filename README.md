# CalciumImaging

This folder contains all the code I used to analyse the calcium imaging data for my PhD thesis on PCDH19. 

imageGateway.m is the main program, written by Gian Michele Ratto. All other functions in the folder are called by imageGatway. In my work I, used 
imageGateway to obtain a binarised version of my calcium imaging data. 
Note that abfload.m is an already existing Matlab function (not written by us).
The Image Processing Toolbox is required to use ImageGateway. 

The other program contained in this folder is particleanalysisdidi.m, written by me to process calcium transients.
It takes detected calcium transients and detected up states from LFP data as an input and outputs quantifications of transients and their
occurence within up states. The comments on the top of the program explain its functioning and required inputs in more detail. 



