# FARSdata
get data from FARS ftp address and use python to create massive data table for analysis
# wget BRP data files from FARS ftp
wget -A 'FARS*.zip' -r -nd -l 7 --tries=10 --waitretry=1 --proxy=on ftp://ftp.nhtsa.dot.gov/FARS/
# unzip all files
find . -name "*.zip" | xargs -P 5 -I fileName sh -c 'unzip -o -d "$(dirname "fileName")/$(basename -s .zip "fileName")" "fileName"'
# delete zips
rm -r *.zip