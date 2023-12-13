# Project overall Architecture
![UML class](https://github.com/ZongruiL/video_converter/assets/103609494/317e60b6-86fb-4472-a673-2a0309efd7a1)




# Endpoints

## Login
```curl -X POST http://gateway/login -u <email>:<password>```

## Upload mp4 file
```curl -X POST -F 'file=@./test.mp4' -H 'Authorization: Bearer <token>' http://mp3converter.com/upload```

## Download mp3 file
```curl --output mp3_download.mp3 -X GET -H 'Authorization: Bearer <token>' "http://mp3converter.com/download?fid=<id>"```
