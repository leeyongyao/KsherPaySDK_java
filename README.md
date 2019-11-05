/***
 * ksher 生存的RSA私钥是pkcs1格式，即-----BEGIN RSA PRIVATE KEY----- 开头的。java需要pkcs8格式的，
 * 是以-----BEGIN PRIVATE KEY-----开通的，以下命令可以装有openssl环境的linux机器上转化pcks1到pcks8格式。
 * 需要pkcs8格式的可以调用命令行转换:
 * openssl pkcs8 -topk8 -inform PEM -in private.key -outform pem -nocrypt -out pkcs8.pem
 * 1、PKCS1私钥生成
 * openssl genrsa -out private.pem 1024
 * 2、PKCS1私钥转换为PKCS8(该格式一般Java调用)
 * openssl pkcs8 -topk8 -inform PEM -in private.pem -outform pem -nocrypt -out pkcs8.pem
 */