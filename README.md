# elastic-sync-autobuild  

Schedule updates elastic search index data  

ex:dev to production 

run docker(scheduler):  
docker run -itd bowwow/sync-els  

run docker(now):
docker run --rm  bowwow/elastic-sync-autobuild /usr/bin/sync.sh

sync.sh: 
ex:
```
echo "sync start:" $(date +"%Y%m%d %T")  

/usr/local/lib/node_modules/elasticdump/bin/elasticdump --input=http://dev --output=http://pro --type=data

echo "sync end:" $(date +"%Y%m%d %T")
```
