# French population

The file "samples.txt" contains the ids of samples for the French.
It was made like this:

    awk 'tolower($6) == "french" {print $2}' ../samples.txt > samples.txt

These samples had been downloaded previously by Nathan Harris. I copied his
versions of these file into the current directory.  I then added
"--no-clobber" to the "wget" commands within "download.slr", so that the
download script will not download a second copy. I'm also downloading the
checksum files. These will allow me to verify Nathan's versions of these
files.

Use md5sum to check integrity of downloaded files:

    [notchpeak2 french]$ md5sum -c *.md5
    LP6005441-DNA_B05.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_B05.annotated.nh2.vcf.gz: OK
    SS6004468.annotated.nh2.vcf.gz.tbi: OK
    SS6004468.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_A05.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_A05.annotated.nh2.vcf.gz.tbi: OK

