# Flask-backend-Application


Relationship diagram

<img width="975" height="704" alt="drawSQL-image-export-2026-04-21" src="https://github.com/user-attachments/assets/e5f5f820-5e0e-4d95-bfe3-605ac2aef630" />



Workout API

This is a simple Flask API for tracking workouts and exercises. It allows you to create workouts, add exercises, and link exercises to workouts with details like sets and reps.

Tech Used: Flask SQLAlchemy Flask-Migrate Marshmallow SQLite

Project Setup

1.Clone the project git clone cd workout-api
2.Install dependencies pipenv install,  pipenv shell
3.Set up the database export FLASK_APP=server/app.py flask db init flask db migrate -m "initial migration" flask db upgrade
4.Seed the database python server/seed.py
5.Run the server flask run --port 5555

Server runs on: http://127.0.0.1:5555/

API Routes Workouts GET /workouts → get all workouts GET /workouts/ → get one workout POST /workouts → create workout DELETE /workouts/ → delete workout

Exercises GET /exercises → get all exercises GET /exercises/ → get one exercise POST /exercises → create exercise DELETE /exercises/ → delete exercise

Link Exercise to Workout POST /workouts/<workout_id>/exercises/<exercise_id> (Add reps, sets, or duration)
