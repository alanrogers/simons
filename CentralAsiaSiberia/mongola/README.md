# Mongola population

The file "samples.txt" contains the ids of samples.  It was made like
this:

    awk 'tolower($6) == "mongola" {print $2}' ../samples.txt > samples.txt

These samples had been downloaded previously by Mitch Lokey. I copied
his versions of these file into the current directory.  I then added
"--no-clobber" to the "wget" commands within "download.slr", so that
the download script will not download a second copy. I'm also
downloading the checksum files. These will allow me to verify Mitch's
versions of these files.

Use md5sum to check integrity of downloaded files:


