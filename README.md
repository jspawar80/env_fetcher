

## Installation

1. **Clone the Repository**

2. **Install Dependencies**
   Before running the servers, you need to install the necessary dependencies.
   ```bash
   npm install
   ```


### Frontend Server

1. **Start the Frontend Server**
   ```bash
   node index.html
   ```

   This will start the frontend server on `http://localhost:3000`.

2. **Available Endpoints**

   - **GET** `/` - Serves the main frontend page.
   - **GET** `/get-instances` - Retrieves the list of available instances.
   - **GET** `/containers/:instanceName` - Fetches the containers for a given instance.
   - **GET** `/config/:instanceName/:containerId` - Retrieves the environment configuration for a specific container in an instance.
   - **POST** `/save-config/:instanceName/:containerId` - Updates the environment configuration for a specific container in an instance.

### Backend Server

1. **Start the Backend Server**
   ```bash
   node main.js
   ```

   This will start the backend server on `http://localhost:3000`.

2. **Available Endpoints**

   - **GET** `/` - Serves the main backend page.
   - **GET** `/get-instances` - Retrieves the list of available instances.
   - **GET** `/containers/:instanceName` - Fetches the containers for a given instance.
   - **GET** `/config/:instanceName/:containerId` - Retrieves the environment configuration for a specific container in an instance.
   - **POST** `/save-config/:instanceName/:containerId` - Updates the environment configuration for a specific container in an instance.

## Configuration

The servers are configured using an `instances` array. Each instance has the following properties:

- `name`: The name of the instance.
- `user`: The SSH user for the instance.
- `host`: The SSH host for the instance.
- `port`: The SSH port for the instance.
- `privateKey`: The path to the private key for SSH authentication.
- `paths`: An array of paths to configuration files on the instance.
