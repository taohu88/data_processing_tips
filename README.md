# Simple split data by field value
* awk '{ if (($6 - 13) % 20 == 0) print}' InFile.tsv > OutFile_test.tsv

# sort and uniq
* cut -f1 inFile.tsv | sort | uniq -c | sort -k1,1 -nr > $2.txt

# shuffle lines of file
* shuf -n 1000 file

# Random sample large file
* http://metadatascience.com/2014/02/27/random-sampling-from-very-large-files/

# select columns
* cut -f1 inputFile.tsv
* awk  -F $'\t' 'BEGIN {OFS = FS} { if (($6 - 13) % 20 != 0) print }'


# join file line by line
* paste -d "\t" file1 file2

# find and run command 
find . -type f -name "*.tsv" -exec sed -i.orig 's/\t/ /g' {} +
find . -type f -name "*.tsv" -exec dos2unix {} +

