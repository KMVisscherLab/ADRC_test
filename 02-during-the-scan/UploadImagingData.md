Imaging data is uploaded using this protocol:


* Overview:
  * Data are uploaded to MIM (DICOMS only) as well as to CHEAHA (DICOMS and raw list files).
  * Some of the post-processed information from the imaging pipelines to be shared within our team is in this password protected box folder: https://uab.box.com/s/nrjcc9dq0m5gv6kqtesdld0ch17cj9za
  * On REDCAP, Nikki updates the file at this address ****

* Strategy:
  * At the scanner, data are pushed to MIM.  This only pushes the DICOMs
  * Thus all data must also be saved on a USB, and transferred by hand, like it is 1999.
    * This includes all dicoms as well as all .list files for PET data.  
    * The best way to move these data is to use the program Easy_Export.py on the console computer.  This program came from Alex Smith at GE.  EasyExport puts the files on an SSD which we have attached to the the console computer
    * These files are zipped on nautilus on the console.
    * These files are then moved from the ssd to Cheaha via rc upload (or sometimes another portal like filezilla)
    * Files are named by subject and by tracer.
    * All files go to this directory:
      *  (Mohammad, please fill this part in:  dkalbilab/ADRC/ ????)
    * Tau Day only: 
      *  Files are moved to /data/project/vislab/raw/METAFUN/ADRC/[ADCID]/ses-[TRACER]/
      *   [ADCID] is the subject number, which differs, and [TRACER] is AV1451 or ML.
   
    * 
    * moved to this location on CHEAHA as well as this location on CHEAHA *** for Deepak to read.
  * The data from this USB are transferred [how?  on your computer? do you use cyberduck or something else? ] to Box.  [also to cheaha?] 
