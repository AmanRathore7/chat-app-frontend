## Run frontend

Install server : npm install -g http-server
Run Command: http-server -p 4000


## Implementation the frontend app

Step 1:
# Add CDN of socket.io into Head

Step 2:
# Create connection to socket
const socketIo = io("http://localhost:3000");

Step 3:
# Get message from server via socket and display it to chat box
socketIo.on("message", function(data) {
    insertChat("you", data, 1000);
});

# Send message 
socketIo.emit("message", text);

