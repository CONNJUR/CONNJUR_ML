# NMRSWML - NMR Spectral Workflow Markup Language
Summary  
This project capitalizes on recent advances in the PREMIS data-model to create an object-oriented metadata framework for recording complex computational processes regarding NMR spectra.  

Why base our workflow system on PREMIS? NMR spectroscopy experiments begin, not end, when data are written to disk by scientific instruments. In a typical computational experiment, the data are often then transformed and processed by tens of agents and software environments. PREMIS’ object orientation means that the repository will be able add agents and environments systematically, for re-use. This is good for both our goal of recording computational work-flow, careful software versioning, the preservation of the software and virtual machines the software.  In a typical deployment, a scientist would provide initial data to our scientific workflow engine. This would instantiate a container PREMIS object that would link all related objects. Next, the initial spectra-data would be written into a PREMIS bitstream object using the objectCharacteristicsExtended container. Our deployment allows either direct deposit of a spectra and its metadata or a pointer to the file and its metadata directly within   The workflow software would initiate agents linked to environments that transform the data. Every time the data are changed, a new bitstream object is initiated and written to disk and a PREMIS event is recorded. When data are part of a complex computational pipeline where intermediate data are never exposed, the intermediate bitstreams can obviously not be recorded. In those cases, we will rely on PREMIS representations to substitute as place-holders. Representations might also be used when researchers find no value in intermediate data, especially when data are in the terabytes range.  