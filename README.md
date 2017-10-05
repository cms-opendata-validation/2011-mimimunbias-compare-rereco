# compare-rereco

This is a simple comparision code to compare the original AOD (available on the Open Data portal) and the AOD file which has be reprocessed from a RAW data sample on the Open Data VM. It loops over different physics objects (tracks, electros, muons, photons, jets, taus and missing et) and fills histograms with P, pt, eta and phi of these objects.

The AOD file to be compared can be repocessed from RAW with minor modifications (global tag, input file, commenting out unnecessary steps) to the configuration file which is recorded together with the original AOD file on the Open Data portal (http://opendata.cern.ch/record/24)

