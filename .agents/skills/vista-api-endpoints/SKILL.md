
---
name: vista-api-endpoints
description: Standards and guidelines for creating FastAPI routes and Supabase database handlers in VISTA.
---
# VISTA API Endpoints Skill
## Purpose
Use this skill when adding new backend endpoints, managing citizen feedback, or writing Supabase database queries.
## Architecture Guidelines
- **Router Pattern**: Place modular routes in `backend/routers/`.
- **Database Client**: Always import the Supabase client from `backend/supabase_client.py`.
- **CORS Handling**: Ensure new endpoints allow cross-origin requests from `http://127.0.0.1:8085`.
## Standard Response Format
All JSON responses must return standard HTTP status codes:
```python
from fastapi import APIRouter, HTTPException
router = APIRouter(prefix="/api/v1", tags=["services"])
@router.get("/services")
async def get_services():
    try:
        return {"status": "success", "data": []}
    except Exception as e:
        raise HTTPException(status_code=500, detail=str(e))