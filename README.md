# Docker & Container Security — Practical Assessment

## Student Details

- **Name:** Bhoomi Garg
- **Registration Number:** 202401100200116
- **Port:** 96
- **GitHub Repository:** https://github.com/BhoomiG28/202401100200116-docker-assessment
- **Docker Hub Username:** Not configured yet

## Project Overview

FestPass is a containerized event-registration application consisting of three services:

- **Frontend:** HTML, JavaScript and Nginx
- **Backend:** Python, Flask and PostgreSQL driver
- **Database:** PostgreSQL

Docker Compose is used to run the services together.

## Technologies Used

- Docker and Docker Compose
- Python and Flask
- PostgreSQL
- Nginx
- Git and GitHub
- Trivy for vulnerability scanning
- ChatGPT for command guidance, code explanations and troubleshooting

## Implementation Progress

### Stage 1 — Containerise the Backend

- Created the backend Dockerfile.
- Built the `fest-backend:0.1` image.
- Ran the backend container and tested the health endpoint.
- Used registration number `202401100200116`.

### Stage 2 — Compose the Application

- Configured frontend, backend and database services.
- Configured separate frontend-backend and backend-database networks.
- Configured a named PostgreSQL data volume.
- Tested event registration through the frontend.

### Stage 3 — Security Scanning

- Pulled the Trivy Docker image.
- Attempted to scan the backend image.
- Final vulnerability scan results and the fixed image are not yet verified.

### Stage 4 — Docker Hub Release

- Not completed.
- The versioned backend image has not yet been verified as published to Docker Hub.

### Stage 5 — Image Signing

- Not completed.
- Cosign signing and verification have not yet been performed.

## Vulnerability Results

| Metric | Before | After |
|---|---:|---:|
| Critical vulnerabilities | Not verified | Not verified |
| High vulnerabilities | Not verified | Not verified |
| Image size | Not recorded | Not recorded |

## How to Run

Ensure Docker Desktop is running. From the project directory, execute:

```powershell
docker compose up -d --build
```

Open the application at:

http://localhost:96

To inspect the services:

```powershell
docker compose ps
docker compose logs --tail 50
```

To stop the application without deleting the database volume:

```powershell
docker compose down
```

## Remaining Tasks

- Complete and save the Trivy before-and-after reports.
- Fix and verify the backend image's vulnerabilities.
- Publish versioned images to a public Docker Hub repository.
- Sign and verify the release using Cosign.
- Capture and organize all required assessment screenshots.
- Update the vulnerability counts, image sizes and image digest.

## AI Tool Disclosure

ChatGPT was used for code explanations, Docker command guidance, troubleshooting and README drafting. Commands were executed on the student's own machine.
