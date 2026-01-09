# methbase
Thousands of high-quality analyzed methylomes.

The track hub can be turned on for human hg38 with this
[link](http://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http://smithlab.usc.edu/trackdata/methylation/hub.txt&genome=hg38&position=lastDbPos).

The track hub file is here:
```text
http://smithlab.usc.edu/trackdata/methylation/hub.txt
```
You can find it among the public hubs in the list at the UCSC Genome Browser.

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

**15,290** high-quality methylomes (as of 2026-01-08)
|  species              |  assembly                                                                                                                                                          |  count  |
|  :-                   |  :-                                                                                                                                                                |  -:     |
|  Mouse                |  [mm39](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=mm39&position=lastDbPos)          |  6270   |
|  Human                |  [hg38](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=hg38&position=lastDbPos)          |  6267   |
|  Cow                  |  [bosTau9](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=bosTau9&position=lastDbPos)    |  497    |
|  Pig                  |  [susScr11](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=susScr11&position=lastDbPos)  |  447    |
|  Zebrafish            |  [danRer11](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=danRer11&position=lastDbPos)  |  339    |
|  Rhesus               |  [rheMac10](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=rheMac10&position=lastDbPos)  |  262    |
|  Chicken              |  [galGal6](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=galGal6&position=lastDbPos)    |  245    |
|  A. mellifera         |  [apiMel2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=apiMel2&position=lastDbPos)    |  210    |
|  Rat                  |  [rn7](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=rn7&position=lastDbPos)            |  201    |
|  Sheep                |  [oviAri4](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=oviAri4&position=lastDbPos)    |  164    |
|  Dog                  |  [canFam6](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=canFam6&position=lastDbPos)    |  84     |
|  Stickleback          |  [gasAcu1](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=gasAcu1&position=lastDbPos)    |  60     |
|  Chimp                |  [panTro6](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=panTro6&position=lastDbPos)    |  59     |
|  Opossum              |  [monDom5](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=monDom5&position=lastDbPos)    |  44     |
|  Crab-eating macaque  |  [macFas5](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=macFas5&position=lastDbPos)    |  34     |
|  Medaka               |  [oryLat2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=oryLat2&position=lastDbPos)    |  22     |
|  Zebra finch          |  [taeGut2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=taeGut2&position=lastDbPos)    |  20     |
|  X. tropicalis        |  [xenTro10](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=xenTro10&position=lastDbPos)  |  15     |
|  Fugu                 |  [fr3](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=fr3&position=lastDbPos)            |  11     |
|  Cat                  |  [felCat9](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=felCat9&position=lastDbPos)    |  9      |
|  Gorilla              |  [gorGor6](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=gorGor6&position=lastDbPos)    |  6      |
|  S. purpuratus        |  [strPur2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=strPur2&position=lastDbPos)    |  4      |
|  Rabbit               |  [oryCun2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=oryCun2&position=lastDbPos)    |  4      |
|  Tetraodon            |  [tetNig2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=tetNig2&position=lastDbPos)    |  3      |
|  Panda                |  [ailMel1](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=ailMel1&position=lastDbPos)    |  3      |
|  Orangutan            |  [ponAbe3](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=ponAbe3&position=lastDbPos)    |  3      |
|  Horse                |  [equCab3](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=equCab3&position=lastDbPos)    |  3      |
|  Platypus             |  [ornAna2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=ornAna2&position=lastDbPos)    |  1      |
|  Gibbon               |  [nomLeu3](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=nomLeu3&position=lastDbPos)    |  1      |
|  Elephant shark       |  [calMil1](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=calMil1&position=lastDbPos)    |  1      |
|  Dolphin              |  [turTru2](https://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http%3A%2F%2Fsmithlab.usc.edu%2Ftrackdata%2Fmethylation%2Fhub.txt&genome=turTru2&position=lastDbPos)    |  1      |

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
