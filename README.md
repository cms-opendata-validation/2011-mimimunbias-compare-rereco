# Validation code to plot basic physics objects from AOD 

This is a simple comparison code to validate the reprocessing step on the Open Data VM by comparing the resulting file (newly rereconstructed from the RAW data sample available on the Open Data Portal) and  the original AOD (also available on the Open Data portal). It loops over different physics objects (tracks, electrons, muons, photons, jets, taus and missing et) and fills histograms with P, pt, eta and phi of these objects.

The new AOD can be repocessed from RAW with minor modifications (global tag, input file, commenting out unnecessary steps) to the configuration file which is recorded together with the original AOD file on the Open Data portal (http://opendata.cern.ch/record/24). See https://github.com/cms-opendata-validation/recotest for the updated configuration file and instructions.

By default, this code reads the original AOD (see demoanalyzer_cfg.py).

Run this code in CMS Open Data VM [http://opendata.cern.ch/VM/CMS/2011]
```
cmsrel CMSSW_5_3_32
cd CMSSW_5_3_32/src
cmsenv
git clone https://github.com/cms-opendata-validation/compare-rereco.git

cd compare-rereco
scram b
ln -sf /cvmfs/cms-opendata-conddb.cern.ch/FT_53_LV5_AN1_RUNA FT_53_LV5_AN1
ln -sf /cvmfs/cms-opendata-conddb.cern.ch/FT_53_LV5_AN1_RUNA.db FT_53_LV5_AN1_RUNA.db
ls -l
ls -l /cvmfs/
cmsRun demoanalyzer_cfg.py
```



