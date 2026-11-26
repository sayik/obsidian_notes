
Todo - [[Clavis/ToDo|ToDo]]
### 26/11/2026
- So I have get the register going, email verification is broken
- **login** is broken
- So I have decided to go ahead and fix WebSocket chat by removing user verification and sending the frontend token to start WebSocket to finish the feature.
- We will need to write tests for the WS chat 
- Auth tests coming next. 
	####  **Todays goal**
	1. Temporarily remove user verification for collecting WebSocket token
	2. Make creation of token work
	3. Make sending of token work
	4. Make script at frontend that receives token 
	5. Make the token be sent with WS chat initiation
	6. Make consumption of the token work
	7. Write tests for the whole lifecycle
	8. Make those test adaptable when login is integrated with dummy user and token


###  25/11/2026 
**Currently stuck at making the signup work, issue was with temp_token now I don't know what the issue is.**
# OK this is issue - verification = generate_email_verification_link(settings.FRONTEND_URL) 


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




