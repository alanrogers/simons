# Han population

The file "samples.txt" contains the ids of samples for the Han
Chinese. It was made like this:

    awk 'tolower($6) == "han" {print $2}' ../samples.txt > samples.txt

Use md5sum to check integrity of downloaded files:

    [kp346 han]$ md5sum -c *.md5
    LP6005441-DNA_C05.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_C05.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_D05.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_D05.annotated.nh2.vcf.gz.tbi: OK
    SS6004469.annotated.nh2.vcf.gz: OK
    SS6004469.annotated.nh2.vcf.gz.tbi: OK

