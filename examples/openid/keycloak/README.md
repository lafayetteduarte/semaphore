# openID Sample - Using Keycloak

This example shows how to run semaphore authentication via openid-Connect in an instance of keycloak.


Check out the keycloak website to read more about the product.

https://www.keycloak.org/

## how to run this example:
 cd to the samples\openid\keycloak directory

 execute docker-compose up to start the stack

Once started, the stack will expose the following:

http://localhost:8080

This is the Identity provider application.
The credentials to login to the admin console are defined in the docker-compose file.

username: admin
password: Pa55w0rd


http://localhost:3000
The semaphore container


# Test Users on keycloak

This example runs keycloak in dev mode ( plz, DO NOT RUN THIS IN PRODUCTION ENVS . ITS NOT SAFE) 
Also, the exaple seeds the keycloak with a realm for semaphore.
Inside that realm, the example seeds one user that could be used to test semaphore OIDC authentication

the seed file is located at the examples\openid\keycloak\imports\realm-export.json

Semaphore config.json are located at examples\openid\keycloak\config.json

the seed file contains one test user with the folowing creds:

username /password : user1@semaphore.com / semaphore


