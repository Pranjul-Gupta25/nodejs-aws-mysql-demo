# 🌐 Node.js + Docker + AWS RDS MySQL App

This project demonstrates how to build and run a simple Node.js application that connects to a **MySQL database hosted on Amazon RDS**, all inside a Docker container.

It’s a great example of integrating cloud services with containerized applications — perfect for DevOps, Cloud, and Backend beginners.

---

## 🚀 Features

- Node.js backend app
- MySQL database (AWS RDS)
- Dockerized environment
- Uses environment variables for configuration
- Clean project structure for learning and experimentation

---

## 🛠️ Tech Stack

- **Node.js**
- **MySQL** (hosted on AWS RDS)
- **Docker**
- **Express.js** (if used)
- **Environment Variables**

---

## 📂 Project Structure

.
├── Dockerfile
├── package.json
├── package-lock.json
├── /src
│ └── app.js
└── /public



2. Run Docker Container with AWS RDS Configuration



docker run -itd -p 3000:3000 \
  -e DB_HOST="your-rds-endpoint.ap-south-1.rds.amazonaws.com" \
  -e DB_USER="your-db-username" \
  -e DB_PASSWORD="your-db-password" \
  -e DB_NAME="my_app_db" \
  node-rds-app
🔐 Make sure your AWS RDS security group allows inbound connections on port 3306 from your machine or Docker host IP.
for trail use all trafic from anywhere in SG for testing only 


To acess Db install mysql_client in instance and acess it using 

mysql -h your-rds-endpoint.ap-south-1.rds.amazonaws.com -u admin -p

