* [codegen](https://oss.sonatype.org/content/repositories/snapshots/io/swagger/swagger-codegen-cli/)
`set swagger3=C:\Users\wajianhu\OneDrive\jar\swagger3.jar`
```bash
# flask
java -jar %swagger3% generate -i http://petstore.swagger.io/v2/swagger.json -l python-flask -o flask
# sanic
pip install swagger-py-codegen
swagger_py_codegen -s api.yml sanic -tlp=sanic --ui --spec
# scala-play
https://github.com/iheartradio/play-swagger
# scala-lagom
java -jar %swagger3% generate -i http://petstore.swagger.io/v2/swagger.json -l scala-lagom-server -o lagom
# koa
https://github.com/lukeautry/tsoa
# fastify
https://github.com/fastify/fastify-swagger
# nodejs
java -jar %swagger3% generate -i http://petstore.swagger.io/v2/swagger.json -l nodejs-server -o node
# rust
java -jar %swagger3% generate -i http://petstore.swagger.io/v2/swagger.json -l rust-server -o rust
# json
java -jar %swagger3% generate -i api.yml -l swagger -o json
# yaml 
java -jar %swagger3% generate -i http://petstore.swagger.io/v2/swagger.json -l swagger-yaml -o yaml
```