# Papuan population

The file "samples.txt" contains the ids of samples.  It was made like
this:

    awk 'tolower($6) == "papuan" {print $2}' ../samples.txt > samples.txt

These samples had been downloaded previously by Nathan Harris. I copied his
versions of these file into the current directory.  I then added
"--no-clobber" to the "wget" commands within "download.slr", so that the
download script will not download a second copy. I'm also downloading the
checksum files. These will allow me to verify Nathan's versions of these
files.

Sample LP6005443-DNA_G07 is listed in ../samples.txt, but is not in
../harris-ftplist.txt. So I don't have a URL for this sample.

Use md5sum to check integrity of downloaded files:

    LP6005443-DNA_H07.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_H07.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_C07.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_C07.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_B08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_B08.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_A08.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_A08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_E08.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_E08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_D07.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_D07.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_C08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_C08.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_F07.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_F07.annotated.nh2.vcf.gz: OK
    SS6004472.annotated.nh2.vcf.gz.tbi: OK
    SS6004472.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_F08.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_F08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_E07.annotated.nh2.vcf.gz.tbi: OK
    LP6005443-DNA_E07.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_D08.annotated.nh2.vcf.gz: OK
    LP6005443-DNA_D08.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_A10.annotated.nh2.vcf.gz.tbi: OK
    LP6005441-DNA_A10.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_B10.annotated.nh2.vcf.gz: OK
    LP6005441-DNA_B10.annotated.nh2.vcf.gz.tbi: OK
