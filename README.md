Working on making light curves for Titan.

Processing of observational data and analysis mostlty done in python according to the code presented.

**This procedure works for polarized images, however, polarized images need to be created with a small tweak in the procedure. TBD.

Downloading Data

On OPUS, the following filters in search data are applied:
General Constraints
  Instrument Name: Cassini ISS
  Intended Target: Saturn -> Titan
  Observation Type: Image
  Measurement Quantity: Reflectivity
Surface Geometry Constraints
  Surface Geometry Target Selector: Saturn -> Titan
    This is important for metadata selections
Cassini ISS Constraints
  Camera: Select NAC or WAC
    Narrow angle camera or wide angle camera
  Filter: Select the filter of choice
    Filters are denoted, e.g., BL1, CB1, etc., but the configuration of ISS is such that there are two filters in a filter wheel, eg, CL1+BL1, or CB1+CL2, where CL1 and CL2 are clear. Which one it is depends on where you choose the NAC, or the WAC, combinations are given here:
    https://pds-rings.seti.org/viewmaster/volumes/COISS_0xxx/COISS_0011/calib/xpsf 
    Additionally, there are also filters with polarizers, denoted at BL2+P60 and so on.
  Missing Lines: Set Min and Max to 0

The following link is set up such that all you have to do is select the filter and camera: 
https://opus.pds-rings.seti.org/opus/#/COISSmissinglines1=0&COISSmissinglines2=0&instrument=Cassini+ISS&mission=Cassini&observationtype=Image&quantity=Reflectivity&surfacegeometrytargetname=Titan&target=Titan&cols=opusid,SURFACEGEOtitan_phase1,SURFACEGEOtitan_centerresolution1&widgets=COISScamera,COISSmissinglines,COISSfilter,surfacegeometrytargetname,quantity,mission,target,instrument,observationtype&order=time1,opusid&view=search&browse=data&cart_browse=gallery&startobs=1&cart_startobs=1&detail=

Once the filters are set, select Browse Results on the top left to visually inspect images
We need specific metadata, so click on Select Metadata, choosing to display:
  OPUS ID
  Observed Phase Angle (Min) [Titan] (degrees)
  Body Center Resolution (Min) [Titan] (km/pixel)

Again, the link above is set up such that after selecting filters, it already only shows this metadata.

  You can visually inspect images to ensure no overexposure or missing lines, and add to cart by checking the box all the way to the left of the image. Adding images that will be used for analysis to cart.
  Usually, you want to select images that show the disk of Titan, i.e., it is not close to the edge, or it is not cut off.
  Once the images are selected go to the shopping cart, and because the files tend to be big in size, to reduce the size, I usually only select the Calibrated Image option.
  Then click on Data Archive, which produces a link on the bottom right corner. Clicking that link will download a zipped file of the images.
  Extract all when done and place the file in the location of choice.
