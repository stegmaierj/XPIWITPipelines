# XPIWITPipelines
This repository contains a selection of pipelines for XPIWIT, an ITK-based graphical user interface that allows you to assemble image processing pipelines in a drag&drop style. The latest binaries of XPIWIT for all major platforms (Windows, Linux, macOS) can be obtained form https://bitbucket.org/jstegmaier/xpiwit/downloads/ .

Reference: Bartschat, A., Hübner, E., Reischl, M., Mikut, R., & Stegmaier, J. (2016). XPIWIT—an XML pipeline wrapper for the Insight Toolkit. Bioinformatics, 32(2), 315-317.

# Cellpose3D

This pipeline can be used to apply our 3D implementation of the Cellpose algorithm (originaly by Stringer et al., 2021). Make sure to use one of the latest XPIWIT releases, as the filter was only recently added. 

- Input: The filter expects an input image, which can be either a 2D or a 3D image containing cellular membranes or cell nuclei (depending on which pretrained model you're using).
- Output: Segmented image in the subfolder `*GradientVectorFlowTracking*`.
- Parameters:
>- Filter: `BinaryThreshold`, Parameter `LowerThreshold`: The probability at which the background prediction should be thresholded. Values below this threshold are background and values above it are considered as foreground. Note that the remaining filters only operate on the foreground region, i.e., potentially decrease the value if you find objects disappearing. 

![Cellpose3D Pipeline](Data/Screenshots/Cellpose3D.png "Overview of the cellpose 3D approach.")

Reference: Eschweiler, D., & Stegmaier, J. (2021). Robust 3D Cell Segmentation: Extending the View of Cellpose. arXiv preprint arXiv:2105.00794.

# TWANG

![TWANG Pipeline](Data/Screenshots/TWANG.png "Overview of the TWANG segmentation approach.")

Reference: Stegmaier, J., Otte, J. C., Kobitski, A., Bartschat, A., Garcia, A., Nienhaus, G. U., ... & Mikut, R. (2014). Fast segmentation of stained nuclei in terabyte-scale, time resolved 3D microscopy image stacks. PloS one, 9(2), e90036.
