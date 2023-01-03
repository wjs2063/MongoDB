# MongoDB
Mongo DB

### OS : MAC OS  or Cent OS

1.Virtual box 다운받고 
2. cent os 7 iso 파일 다운로드받는다 링크 : http://mirror.navercorp.com/centos/7.9.2009/isos/x86_64/
3. vm 만들고 putty 와 연결해준다 
4. 이제 몽고DB 를 다운로드해야함 링크 : https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-red-hat/
5. vi /etc/yum.repos.d/mongodb-org-6.0.repo 를 한후 해당 내용을 복사붙혀넣기
```
[mongodb-org-6.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/6.0/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-6.0.asc

```

6.
```
sudo yum install -y mongodb-org
```
7.
``` 
sudo yum install -y mongodb-org-6.0.3 mongodb-org-database-6.0.3 mongodb-org-server-6.0.3 mongodb-mongosh-6.0.3 mongodb-org-mongos-6.0.3 mongodb-org-tools-6.0.3
```
8. 
```
exclude=mongodb-org,mongodb-org-database,mongodb-org-server,mongodb-mongosh,mongodb-org-mongos,mongodb-org-tools

```

이하 공식문서 참고하면 됨.




## 설치 공식문서 https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/

설치는 생략 


## START 

CRUD !! 
java script 문법 지원
````
brew services start mongodb-community@6.0

시작
mongosh

use video

생성
movie = {
"title": "Star Wars: Episode IV -A New Hope",
"director":"George Lucas","year":1997
}

읽기 
db.movies.findOne()


갱신
updateOne
db.movies.updateOne( 찾고자하는 기준 , 바꾸고자하는 값 )
db.movies.updateOne({"title": "Star Wars: Episode IV -A New Hope"}, {$set:{revies :[]}} )


삭제

db.movies.deleteOne({"title": "Star Wars: Episode IV -A New Hope"})

````
