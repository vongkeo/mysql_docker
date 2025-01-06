# Docker-Compose Setup for MySQL with DataGrip Connectivity

This repository provides a `docker-compose.yml` file to quickly set up a MySQL database container with persistent storage and connect it to JetBrains DataGrip or other database clients.  

---

## Features
- MySQL 8.0 container.
- Custom user, password, and initial database.
- Exposed on port `3306` for easy client access.
- Persistent volume to retain data between container restarts.

---

## How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/vongkeo/mysql_docker.git
cd mysql_docker
```
### 2. Start the MySQL Container
```bash
docker-compose up -d
```

### 3. Default Configuration
- Root User: root
- Root Password: root_password
- Database: testdb
- User: testuser
- User Password: testpassword
- Port: 3306

> You can modify these values in the docker-compose.yml file as needed.

### 4. How to Connect Using DataGrip
Steps:
1. Open DataGrip and create a new Data Source.
2. Select MySQL as the database type.
3. Fill in the connection details:
    - Host: localhost
    - Port: 3306
    - User: testuser
    - Password: testpassword
    - Database: testdb (optional)
4. Test the connection. If successful, save the configuration.

### 5. Stop the MySQL Container
```bash
docker-compose down
```

### 6. Restart the MySQL Container
```bash
docker-compose up -d
```

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Contributions
Contributions are welcome! Please feel free to submit a PR or open an issue.