# Windows subsystem
* LxRunOffline.exe  install -nUbuntu -f e:\temp\16.04.2-server-cloudimg-amd64-root.tar.gz -de:\Ubuntu -re:\local\root
* LxRunOffline.exe run -nUbuntu

# Cut head line
* tail -n +2 Infile.tsv > outFile.tsv

# Simple split data by field value
* awk '{ if (($6 - 13) % 20 == 0) print}' InFile.tsv > OutFile_test.tsv

# Sort and uniq
* cut -f1 inFile.tsv | sort | uniq -c | sort -k1,1 -nr > $2.txt

# Shuffle lines of file
* shuf -n 1000 file

# Random sample large file
* http://metadatascience.com/2014/02/27/random-sampling-from-very-large-files/

# Select columns
* cut -f1 inputFile.tsv
* awk  -F $'\t' 'BEGIN {OFS = FS} { if (($6 - 13) % 20 != 0) print }'


# Join file line by line
* paste -d "\t" file1 file2

# Find and run command 
find . -type f -name "*.tsv" -exec sed -i.orig 's/\t/ /g' {} +
find . -type f -name "*.tsv" -exec dos2unix {} +

