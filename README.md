# methbase
Thousands of high-quality analyzed methylomes.

The track hub can be turned on for human hg38 with this
[link](http://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http://smithlab.usc.edu/trackdata/methylation/hub.txt&genome=hg38&position=lastDbPos).

The track hub file is here:
```text
http://smithlab.usc.edu/trackdata/methylation/hub.txt
```
You should be able to find it among the public hubs in the list at the UCSC
Genome Browser, and if not now, then soon.

There's a chance this hub could be very slow. If you find it useful, and
would like to see better performance, the best way to help is simply to let
me (Andrew) know, because allocating resources to hardware is only worth
it if the resource will be used.

If you would like to suggest a publicly available methylome for
inclusion in methbase, please submit an issue
[here](https://github.com/smithlabcode/methbase/issues).

The methbase database includes many more methylomes than are available
for viewing with the methbase track hub. Those selected for the track
hub meet criteria that help ensure they have been analyzed correctly.

Currently the criteria are (somewhat arbitrary):

- 0.9: Minimum bisulfite conversion rate.
- 1.0: Minimum average coverage across the genome.
- 0.7: Minimum fraction of CpG sites covered.

# Genomes

MethBase2 includes methylomes for the following genomes. The number of
methylomes for each genome changes continually:

(as of 2025-12-01; 14,845 high-quality methylomes)
```text
hg38      6006
mm39      5822
bosTau9   473
susScr11  430
danRer11  335
rheMac10  260
galGal6   208
apiMel2   208
rn7       199
oviAri4   147
panTro6   59
canFam6   51
oryLat2   22
xenTro10  15
macFas5   9
felCat9   9
monDom5   8
gorGor6   6
strPur2   4
tetNig2   3
ponAbe3   3
equCab3   3
ailMel1   3
turTru2   1
oryCun2   1
ornAna2   1
nomLeu3   1
calMil1   1
```

# Methylome features

Moving forward, not all methylomes will have each kind of "feature" available
through the track hub. The criteria are below (in progress). If you want something
and you can't find it, possibly those features did not meet criteria. Please contact
me to ask and I can check if they might have barely failed to meet the criteria
and I might be able to adjust or provide them to you directly.

## Hypomethylated regions (HMRs)

These are identified with the `hmr` command in `dnmtools`, which is
very similar to the tool I wrote for the Molaro (2011) paper. For
MethBase, the analysis workflows attempt to identify HMRs in every
high-quality methylome from a vertebrate species. This clearly won't
make sense in all cases. In the most extreme example, cells with DNA
methylation erased should not be understood in terms of "valleys" of
low methylation. The approach I plan to implement will be to exclude
HMRs when they seem to be driven by a different biological feature.
This means identifying methylomes that are outliers. So far it seems
like most methylomes with HMRs corresponding to promoters and
enhancers have the following characteristics (which have been evident
for the past 10 years):

- Human: between 25K and 110K HMRs, with mean size between 750 bp and 4K bp.
- Mouse: between 20K and 100K HMRs, with mean size between 750 bp and 3K bp.

Eventually I plan to incorporate a sequential identification of PMDs
and HMRs so that methylomes with PMDs can still have HMRs accurately
identified. This will require revisiting some a fraction of the
methylomes to re-run HMR identification.
