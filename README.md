-----------------------------------------------------------
# MonoHiggsToGG analysis
-----------------------------------------------------------
## Install flashgg 

This package depends on [flashgg](https://github.com/cms-analysis/flashgg).

From MiniAOD to MicroAOD production flashgg package can be used.


### get flashgg:

   export SCRAM_ARCH=slc7_amd64_gcc700

   cmsrel CMSSW_10_6_29

   cd CMSSW_10_6_29/src

   cmsenv

   git cms-init

   git clone -b dev_legacy_runII https://github.com/cms-analysis/flashgg 

   source flashgg/setup_flashgg.sh



   If everything now looks reasonable, you can build:

   cd $CMSSW_BASE/src

   scram b -j 8


-----------------------------------------------------------
# Run the Analysis
-----------------------------------------------------------
## MicroAOD to diPhotonTrees 


### get MonoHiggsToGG:

   cd $CMSSW_BASE/src

   git clone https://github.com/ashimroy/MonoHiggsToGG.git

   scram b -j 8



   If everything now looks fine, you can run:

   cmsRun MonoHiggsToGG/analysis/test/diPhoAna_2018.py