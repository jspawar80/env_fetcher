## Description
This project provides a server-side interface to manage and interact with remote Docker instances. Through the provided endpoints, users can fetch a list of available instances, retrieve running containers in those instances, and manage environment configurations for specific containers. The system uses SSH to communicate with the remote instances, allowing for secure interactions.

## Installation

1. **Clone the Repository**

2. **Install Dependencies**
   Before running the servers, you need to install the necessary dependencies.
   ```bash
   npm install
   ```

3. **Start the App**
   ```bash
   node main.js
   ```

   This will start the frontend server on `http://localhost:3000`.



## Configuration

The servers are configured using an `instances` array. Each instance has the following properties:

- `name`: The name of the instance.
- `user`: The SSH user for the instance.
- `host`: The SSH host for the instance.
- `port`: The SSH port for the instance.
- `privateKey`: The path to the private key for SSH authentication.
- `paths`: An array of paths to configuration files on the instance.
