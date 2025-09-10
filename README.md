### Video Demonstration:
https://drive.google.com/file/d/1OXFKr1EPZ-AwBEU4CvmPPn_VaGgqciiK/view?usp=drive_link

# Cloud Enabled Deployment In Action with AWS & GCP
This repository contains a cloud-enabled application with backend services deployed across AWS and GCP cloud platforms, demonstrating modern cloud deployment practices.

### 📁 Project Structure
- The repository contains four main projects:
- course-service (Spring Boot + GCP Cloud SQL MySQL)
- student-service (Spring Boot + Database)
- media-service (Spring Boot + Storage)
- frontend-app (React + TypeScript)

### 🚀 Cloud Deployment Architecture

### ☁️ Multi-Cloud Integration
- GCP Cloud SQL: MySQL database for course management
- AWS Services: Various AWS cloud services integrated
- Hybrid Architecture: Demonstrating multi-cloud deployment strategies

### 🛠️ Backend Services
#### 1. course-service (Deployed on GCP Cloud SQL)
- Entity: Course(id, name, duration)
- Database: GCP Cloud SQL MySQL instance
  - Endpoints:
  - GET /courses
  - GET /courses/{id}
  - POST /courses
  - DELETE /courses/{id}
- Default port: 8081
- Cloud Configuration: Configured for GCP Cloud SQL connection

#### 2. student-service
- Document: Student(registrationNumber, fullName, address, contact, email)
- Endpoints:
  - GET /students
  - GET /students/{id}
  - POST /students
  - DELETE /students/{id}
- Default port: 8082

#### 3. media-service
- Resource: files
- Endpoints:
  - POST /files (multipart/form-data: file)
  - GET /files (list)
  - GET /files/{id} (fetch)
  - DELETE /files/{id} (delete)
- Default port: 8083
- Storage: Cloud-optimized storage configuration

### Frontend (frontend-app)
- React + TypeScript + MUI + Axios + Vite app with 3 sections: Courses, Students, Media
- Scripts:
`npm run dev` (Vite dev server)
`npm run build` (TypeScript build + Vite build)
`npm run preview` (Preview built app)

### 📋 Prerequisites
- Java 17+
- Node.js 16+
- Maven
- GCP Account (for Cloud SQL)
- AWS Account (for cloud services)

### 🔧 Installation & Setup
#### 1. Clone the Repository
`git clone <your-repo-url>`

`cd cloud-enabled-deployment-in-action-with-aws`

#### 2. Backend Services Setup
build all backend services

`mvn -q -e -DskipTests package`

Or build individually

`cd course-service && mvn package`

`cd ../student-service && mvn package`

`cd ../media-service && mvn package`

#### 3. Frontend Setup

`cd frontend-app`
`npm install`

#### 4. GCP Cloud SQL Configuration

Create a MySQL instance in GCP Cloud SQL
Update `application-gcp.properties` with your connection details:

properties

`spring.datasource.url=jdbc:mysql://[YOUR_INSTANCE_IP]:3306/eca_courses`

`spring.datasource.username=[YOUR_USERNAME]`

`spring.datasource.password=[YOUR_PASSWORD]`

#### 5. AWS Configuration
Configure AWS services as needed for additional functionality

### Running the Application
#### Start Backend Services

#### Course Service (GCP Cloud SQL)

`cd course-service`

`java -jar target/course-service-1.0.0.jar --spring.profiles.active=gcp`

#### Student Service

`cd student-service`

`java -jar target/student-service-1.0.0.jar`

#### Media Service

`cd media-service`

`java -jar target/media-service-1.0.0.jar`

### Start Frontend

`cd frontend-app`

`npm run dev`

### 📊 Demonstration Video
https://drive.google.com/file/d/1OXFKr1EPZ-AwBEU4CvmPPn_VaGgqciiK/view?usp=drive_link

The video demonstrates:

- ✅ GCP Cloud SQL database configurations
- ✅ Successful connection from Spring Boot application
- ✅ CRUD operations working with cloud database
- ✅ Full application functionality with cloud infrastructure

### 📝 Assignment Completion Status
- ✅ Course Service Migration: Local MySQL → GCP Cloud SQL ✓
- ✅ Cloud Configuration: Proper environment setup ✓
- ✅ Database Connectivity: Secure cloud connections ✓
- ✅ AWS Integration: Cloud services implementation ✓
- ✅ Documentation: Updated README with instructions ✓
- ✅ Video Demonstration: Working system recording ✓
- ✅ Repository Organization: Proper project structure ✓

### 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

### 🤝 Contributing
Fork the repository

Create a feature branch (`git checkout -b feature/amazing-feature`)

Commit your changes (`git commit -m 'Add some amazing feature'`)

Push to the branch (`git push origin feature/amazing-feature`)

Open a Pull Request

### 📞 Support
For support or questions about this deployment, please open an issue in the GitHub repository.
