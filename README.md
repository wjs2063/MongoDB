# MongoDB
Mongo DB

### OS : MAC OS 

## 설치 공식문서 https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/

설치는 생략 


## START 
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
