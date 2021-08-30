## Polling Nest

> Polling Nest is a full stack polling app. Users can create polls and solicit feedback from people or fans and let them vote and share in their polls. Users can also tailor their polls by incorporating videos, images and text options.The backend server was developed using Spring Boot and Spring Security along with JWT authentication. MySQL database was used for storage. The front-end application was made using React and Ant Design for designing our user interface.

![Polling Nest 1](https://github.com/smyrmnsr/polling-nest-frontend/blob/master/polling-nest.png)
![Polling Nest 2](https://github.com/smyrmnsr/polling-nest-frontend/blob/master/polling-nest1.png)
![Polling Nest 3](https://github.com/smyrmnsr/polling-nest-frontend/blob/master/polling-nest2.png)
![Polling Nest 4](https://github.com/smyrmnsr/polling-nest-frontend/blob/master/polling-nest3.png)
![Polling Nest 5](https://github.com/smyrmnsr/polling-nest-frontend/blob/master/polling-nest4.png)

## Steps to Setup the Spring Boot Back end app (polling-nest-backend)

1. **Clone the application**

   ```bash
   git clone https://github.com/smyrmnsr/polling-nest-backend
   cd polling-nest-backend
   ```

2. **Create MySQL database**

   ```bash
   create database polling_app
   ```

3. **Change MySQL username and password as per your MySQL installation**

   - open `src/main/resources/application.properties` file.

   - change `spring.datasource.username` and `spring.datasource.password` properties as per your mysql installation

4. **Run the app**

   You can run the spring boot app by typing the following command -

   ```bash
   mvn spring-boot:run
   ```

   The server will start on port 8080.

   You can also package the application in the form of a `jar` file and then run it like so -

   ```bash
   mvn package
   java -jar target/polls-0.0.1-SNAPSHOT.jar
   ```

5. **Default Roles**

   The spring boot app uses role based authorization powered by spring security. To add the default roles in the database. The following sql queries were added in `src/main/resources/data.sql` file. Spring boot will automatically execute this script on startup -

   ```sql
   INSERT IGNORE INTO roles(name) VALUES('ROLE_USER');
   INSERT IGNORE INTO roles(name) VALUES('ROLE_ADMIN');
   ```

   Any new user who signs up to the app is assigned the `ROLE_USER` by default.

## Steps to Setup the React Front end app (polling-nest-frontend)

First go to the `polling-nest-frontend` folder -

```bash
cd polling-nest-frontend
```

Then type the following command to install the dependencies and start the application -

```bash
npm install && npm start
```

The front-end server will start on port `3000`.

## Technologies Used

FRONTEND

![REACT](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JAVASCRIPT](https://img.shields.io/badge/-JAVASCRIPT-black?style=flat&logo=javascript)
![CSS3](https://img.shields.io/badge/-CSS3-black?style=flat&logo=css3)
![HTML5](https://img.shields.io/badge/-HTML5-black?style=flat&logo=html5&logoColor=red)

BACKEND

![NODE.JS](https://img.shields.io/badge/NODE.JS-black?style=flat&logo=node-dot-js&logoColor=green)
![MONGODB](https://img.shields.io/badge/MONGODB-black?style=flat&logo=mongodb&logoColor=green)
![EXPRESS](https://img.shields.io/badge/EXPRESS-black?style=flat&logo=express&logoColor=yellow)
