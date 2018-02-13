# Simple split data by field value

* awk '{ if (($5 - 13) % 20 == 0) print}' InFile.tsv > OutFile_test.tsv

# sort and uniq
* cut -f1 inFile.tsv | sort | uniq -c | sort -n > $2.txt

# shuffle lines of file
* shuf -n 1000 file
