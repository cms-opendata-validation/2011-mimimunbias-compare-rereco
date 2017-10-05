# compare-rereco

This is a simple comparision code to compare the original AOD (available on the Open Data portal) and the AOD file which has be reprocessed from a RAW data sample on the Open Data VM. It loops over different physics objects (tracks, electrons, muons, photons, jets, taus and missing et) and fills histograms with P, pt, eta and phi of these objects.

The AOD file to be compared can be repocessed from RAW with minor modifications (global tag, input file, commenting out unnecessary steps) to the configuration file which is recorded together with the original AOD file on the Open Data portal (http://opendata.cern.ch/record/24). See https://github.com/katilp/recotest for the updated configuration file and instructions.

Run this code in CMS Open Data VM [http://opendata.cern.ch/VM/CMS/2011]
```
cmsrel CMSSW_5_3_32
cd CMSSW_5_3_32/src
cmsenv
git clone https://github.com/katilp/compare-rereco.git

cd compare-rereco.git
ln -sf /cvmfs/cms-opendata-conddb.cern.ch/FT_53_LV5_AN1_RUNA FT_53_LV5_AN1
ln -sf /cvmfs/cms-opendata-conddb.cern.ch/FT_53_LV5_AN1_RUNA.db FT_53_LV5_AN1_RUNA.db
cmsRun demoanalyzer_cfg.py
```



