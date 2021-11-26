# LogInOut
Full stack Log in out project using Spring Boot &amp; Angular 2

After creating DB you need to fell it with Roles:

INSERT INTO roles(name) VALUES('ROLE_USER');

INSERT INTO roles(name) VALUES('ROLE_MODERATOR');

INSERT INTO roles(name) VALUES('ROLE_ADMIN');

Using Post man First time:

Signup First Time

URL POST: localhost:8080/api/auth/signup 

Body:

{
	"username":"ModUser",
	"email":"ModUser@test.com",
	"password":"moduser",
	"role": ["mod", "user"]
}

Login First Time to get Token

URL POST: localhost:8080/api/auth/signup

Body:

{
	"username":"ModUser",
	"password":"moduser",
}

Response: will be similar

{
    "refreshToken": "8d97f296-6469-4289-9117-de7c6af3ac3c",
    "id": 1,
    "username": "ModUser",
    "email": "ModUser@test.com",
    "roles": [
        "ROLE_MODERATOR",
        "ROLE_USER"
    ],
    "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJNb2RVc2VyIiwiaWF0IjoxNjM3OTQzMDk5LCJleHAiOjE2Mzc5NDMxNTl9.1k8G5tqunqVMZyCjc-6JONZiG2NpHetwTJEZ0LoJa29Psj3h7rFvwMkYmfBICW2o-1dMqXRu3aV26LGrRdG1vQ",
    "tokenType": "Bearer"
}

