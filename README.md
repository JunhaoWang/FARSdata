# FARSdata
get data from FARS ftp address and use python to create massive data table for analysis
# wget BRP data files from FARS ftp
wget -A 'FARS*.zip' -r -nd -l 7 --tries=10 --waitretry=1 --proxy=on ftp://ftp.nhtsa.dot.gov/FARS/