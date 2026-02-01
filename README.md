# spring-security-b010201

ssia-ch2-ex1

## Project Generation

This project was generated with Spring CLI v4.0.1.

```bash
spring init --type=gradle-project \
--language=java \
--groupId=tech.samagua \
--artifactId=spring-security-b010201 \
--packageName=tech.samagua.spring_security_b010201 \
--packaging=jar \
--javaVersion=25 \
--dependencies=web,security
unzip ./spring-security-b010201.zip -d spring-security-b010201
```

## Execution
To run the application, navigate to the project directory and use the following command:

```bash
# http profile
./gradlew bootRun -Dspring.profiles.active=http
# https profile
# configure your keystore settings in application-https.yml before running
./gradlew bootRun -Dspring.profiles.active=https
```

### Generate a self-signed certificate
To generate a self-signed certificate for HTTPS, use the following command:
```bash
openssl req -newkey rsa:2048 -x509 -keyout key.pem -out cert.pem -days 365
openssl pkcs12 -export -in cert.pem -inkey key.pem -out certificate.p12 -name "certificate"
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

[//]: # (TODO: Review the development guide)