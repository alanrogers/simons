# Japanese population

The file "samples.txt" contains the ids of samples for the Chinese.
It was made like this:

    awk 'tolower($6) == "japanese" {print $2}' ../samples.txt > samples.txt

These samples had been downloaded previously by Nathan Harris. I
copied his versions of these file into the current directory:

    cp ~/grp1/harris/data/jpt/LP6005441-DNA_C06.annotated.nh2.vcf.gz .
    cp ~/grp1/harris/data/jpt/LP6005441-DNA_D06.annotated.nh2.vcf.gz .
    cp ~/grp1/harris/data/jpt/LP6005592-DNA_C02.annotated.nh2.vcf.gz .
    cp ~/grp1/harris/data/jpt/LP6005441-DNA_C06.annotated.nh2.vcf.gz.tbi .
    cp ~/grp1/harris/data/jpt/LP6005441-DNA_D06.annotated.nh2.vcf.gz.tbi .
    cp ~/grp1/harris/data/jpt/LP6005592-DNA_C02.annotated.nh2.vcf.gz.tbi .

I then added "--no-clobber" to the "wget" commands within
"download.slr", so that the download script will not download a second
copy. I'm also downloading the checksum files. These will allow me to
verify Nathan's versions of these files.

Use md5sum to check integrity of downloaded files:

    [kp346 japanese]$ md5sum -c *.md5
    LP6005441-DNA_D06.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_D06.annotated.nh2.vcf.gz: OK
    LP6005592-DNA_C02.annotated.nh2.vcf.gz.tbi: OK
    LP6005592-DNA_C02.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_C06.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_C06.annotated.nh2.vcf.gz: OK


