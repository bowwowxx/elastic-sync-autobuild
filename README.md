# elastic-sync-autobuild  

Schedule updates elastic search index data  

ex:dev server to production server   

run docker:  
docker run -itd bowwow/sync-els  

sync.sh: 
ex:
```
echo "sync start:" $(date +"%Y%m%d %T")  

/usr/local/lib/node_modules/elasticdump/bin/elasticdump --input=http://dev --output=http://pro --type=data

echo "sync end:" $(date +"%Y%m%d %T")
```
