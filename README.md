# ClientServerMonitor

A concise Java console application demonstrating basic client-server networking using sockets, where an iterative server responds to system-level requests and a multithreaded client issues concurrent queries to measure turnaround performance.

---

## Project Structure

```
ClientServerMonitor/
├── src/
│   ├── IterativeServer.java
│   └── MultiThreadedClient.java
└──
```

---

## Core Java Classes

### `IterativeServer.java`
Implements a simple iterative TCP server:
- Listens on port `1234` and handles one client connection at a time.
- Accepts plain-text commands such as `date and time`, `uptime`, `memory use`, `netstat`, `current users`, and `running processes`.
- Executes each command using system-level operations and returns the result to the client.
- Uses standard Java networking and I/O classes to manage connections and responses.

### `MultiThreadedClient.java`
Implements a multithreaded TCP client:
- Prompts the user for the server IP, port number, command to send, and number of client requests to generate.
- Creates multiple threads where each thread connects to the server, sends the command, receives the response, and prints it.
- Tracks and calculates the total and average turnaround time for all requests to assess performance under load.

---

## Future Enhancements
- Convert the server to a fully multithreaded model for handling concurrent connections.
- Add logging for all client requests and server responses.
- Include error recovery and retry logic for failed connections.
- Build a GUI using Swing or JavaFX for real-time monitoring and control.

---

## License
This project is licensed for personal, non-commercial use only. Redistribution, resale, or modification is prohibited without written permission from the author.  
See the [LICENSE] file for full details.

---

## Author
**Trace Davis**  
- GitHub: https://github.com/Trace0727  
- LinkedIn: https://www.linkedin.com/in/trace-d-926380138/
