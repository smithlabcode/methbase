# methbase
Thousands of high-quality analyzed methylomes.

The track hub can be turned on for human hg38 with this
[link](http://genome.ucsc.edu/cgi-bin/hgTracks?hubUrl=http://smithlab.usc.edu/methbase/data/methbase2/trackhub/hub.txt&genome=hg38&position=lastDbPos).

At present the track hub file is here, but it migh move while things are settling:
```text
http://smithlab.usc.edu/methbase/data/methbase2/trackhub/hub.txt
```

If you would like to suggest a publicly available methylome for
inclusion in methbase, please submit an issue
[here](https://github.com/smithlabcode/methbase/issues).

The methbase database includes many more methylomes than are available
for viewing with the methbase track hub. Those selected for the track
hub meet criteria that help ensure they have been analyzed correctly.

Currently the criteria are:

- 0.9: Minimum bisulfite conversion rate.
- 1.0: Minimum average coverage across the genome.
- 0.8: Minimum fraction of CpG sites covered.
