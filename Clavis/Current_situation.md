- Setup redis container ☑
- Connected redis contrainer through fastapi-redis libvrary 
added env REDIS_URL ☑
- Added redis endpoint to see health check ☑
- Added websocket_token file to handle and save token
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
