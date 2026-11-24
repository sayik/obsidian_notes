docker compose down
docker compose down -v
volumes:
  - ./alembic:/app/alembic
  - ./alembic.ini:/app/alembic.ini
docker compose up -d db redis
docker compose run --rm app uv run alembic revision --autogenerate -m "initial schema"

- Added websocket_token creator to endpoint router handler 
- passed user_id to it, confused about redis connection invocation though. 
- now need to test it end to end with redis testcontainers, replacing env variable is important. 
- Next to do it consume the token. 
- Also File needs to be directly connected with user_id
# Make websocket work
next step
- redis integrated ✔️
- router function in **auth.py** for getting token - ie called when dashboard is loaded, js calls ws-token route, so it internally calls create token. 
- router function in **chat.py** to consume token and start chat with dummy output
- test test test
- Now deal with ws data stream and return dummy response. send patient id with 
- store patient context in redis 
- Connecting bedrock cheapest mode for refining keywords. 
- Take in audio data
- test test test



Testing 
version tracking - clean up
logging 
monitoring
