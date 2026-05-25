# Jobs JSON API

A zero-config REST API for job listings, powered by [json-server](https://github.com/typicode/json-server) and deployed on Render.

## Base URL
```
https://your-app-name.onrender.com
```

## Endpoints

### Get all jobs
```
GET /jobs
```

### Get a single job
```
GET /jobs/1
```

### Filter by field
```
GET /jobs?employment_type=FULL_TIME
GET /jobs?work_mode=REMOTE
GET /jobs?experience_level=SENIOR
GET /jobs?posting_status=PUBLISHED
GET /jobs?location_city=New York
GET /jobs?department=Engineering
```

### Paginate
```
GET /jobs?_page=1&_limit=10
```

### Sort
```
GET /jobs?_sort=salary_min&_order=desc
GET /jobs?_sort=created_at&_order=asc
```

### Full-text search
```
GET /jobs?q=frontend
```

### Combine filters
```
GET /jobs?work_mode=REMOTE&experience_level=MID&_sort=salary_max&_order=desc
```

## Create a job
```
POST /jobs
Content-Type: application/json

{ "title": "New Role", "department": "Engineering", ... }
```

## Update a job
```
PUT /jobs/1
Content-Type: application/json

{ "title": "Updated Title" }
```

## Delete a job
```
DELETE /jobs/1
```

## Deploy to Render
1. Push this repo to GitHub
2. Go to render.com → New → Web Service
3. Connect your repo
4. Set Build command: `npm install`
5. Set Start command: `npm start`
6. Deploy!
