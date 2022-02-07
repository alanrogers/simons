# Han population

The file "samples.txt" contains the ids of samples for the Han
Chinese. It was made like this:

    awk 'tolower($6) == "han" {print $2}' ../samples.txt > samples.txt

