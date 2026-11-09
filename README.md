Full-Stack JavaScript Architecture
A structured starting point for building full-stack JavaScript applications with separate frontend, backend, database, and deployment services.
Maintained by Satish Jadav
---
About
This repository documents an example architecture for a full-stack JavaScript product. It separates the application into services for a landing website, web application, mobile application, API, database, and deployment.
The structure is intended as a reference that can be adapted to the needs of an individual project.
> **Project note:** This repository is based on the Full-Stack JavaScript Architecture project originally published by Atul Yadav. The original project and its contributors retain credit for their work. This copy is maintained and adapted by Satish Jadav.
Core Structure
```text
project/
├── backend/
│   ├── api/             # Node.js API service
│   ├── database/        # MongoDB
│   └── proxy/           # NGINX reverse proxy
├── deployment/          # Docker Compose configuration
├── frontend/
│   ├── app/
│   │   ├── mobile/      # React Native application
│   │   └── web/         # React web application
│   └── landing/         # React landing website
└── README.md
```
Technology Stack
Backend
Node.js
Express
MongoDB
NGINX
Frontend
React
Next.js
Redux
React Router
Material UI
React Native
Deployment
Docker
Docker Compose
Main Services
Service	Technology	Example port
API	Node.js, Express	8000
Web application	React	5000
Landing website	React / Next.js	3000
Database	MongoDB	27017
Reverse proxy	NGINX	80 / 443
Ports and service choices can be changed to suit your environment.
Prerequisites
Install the tools required for the parts of the project you intend to run:
Node.js and npm
MongoDB
Docker and Docker Compose (for containerized deployment)
Android Studio (for Android development)
Xcode (for iOS development on macOS)
Setup and Running
The original architecture separates the application into independently runnable services. The commands below describe the intended workflow; check each service's `package.json` and environment example files for the exact scripts and variables available in your checkout.
1. Clone the repository
```bash
git clone https://github.com/satishjadav01/REPOSITORY-NAME.git
cd REPOSITORY-NAME
```
Replace `REPOSITORY-NAME` with the actual repository name.
2. Configure the API
```bash
cd backend/api
npm install
```
Create the environment file expected by the API (for example, `.env.local`) and configure values such as:
```env
PORT=8000
NODE_ENV=development
MONGO_URL=mongodb://localhost:27017/example
LANDING_URL=http://localhost:3000
WEB_URL=http://localhost:5000
API_URL=http://localhost:8000
```
Do not commit real credentials, secrets, or production environment files.
Run the API using the script defined in the API package:
```bash
npm start
```
3. Configure the landing website
```bash
cd frontend/landing
npm install
npm start
```
Configure the landing website's environment variables according to its environment example file.
4. Configure the web application
```bash
cd frontend/app/web
npm install
npm start
```
Configure the web application's API and application URLs according to its environment example file.
5. Mobile application
For the mobile application:
```bash
cd frontend/app/mobile
npm install
```
Configure the API and web URLs for your local network, then follow the React Native instructions for your platform.
6. Deployment
If the repository includes a Docker Compose configuration, review its services and environment variables before deploying.
```bash
cd deployment
docker compose up --build -d
```
Screenshots
Add screenshots of your own running application here:
```md
![Application screenshot](./docs/images/screenshot.png)
```
Create the `docs/images` folder and add your project screenshots before using the example above.
Author
Satish Jadav
GitHub: @satishjadav01
GitHub profile: https://github.com/satishjadav01
Original Project Credit
This README is an adapted version of the Full-Stack JavaScript Architecture documentation originally published by Atul Yadav.
Original author: Atul Yadav
Original project: Full-Stack JavaScript Architecture
Please refer to the original repository for its original license and contribution history.
---
If you find this repository useful, feel free to explore my other projects on GitHub.
