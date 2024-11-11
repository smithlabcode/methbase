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
