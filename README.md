# Node-RED Docker Deployment Guide

This guide provides instructions on how to deploy Node-RED using Docker, including how to manage flows and install additional libraries.

## Starting Node-RED

To start Node-RED using Docker, navigate to the Node-RED directory and use Docker Compose:

```bash
cd node-red
docker compose up 
```

## Managing Flows

Flows are stored outside the container in the default Node-RED directory. To access your flows, navigate to:

```bash
/home/pi/.node-red/data/lib/flows
```

This location will typically be `~/.node-red/data/lib/flows` on your filesystem.

## Installing Additional Libraries

If you wish to install additional Node.js libraries:

1. Navigate to the Node-RED data directory:

    ```bash
    cd ~/.node-red/data
    ```

2. Add your dependencies to the `package.json` file located in this directory.

3. Run the following command to install the dependencies:

    ```bash
    npm install
    ```

## Managing Permissions

If you encounter any permission issues, particularly when accessing files or directories, you can modify the permissions recursively using `chmod`. **Note:** Use this command with caution as it grants wide permissions.

```bash
sudo chmod -R 755 ~/.node-red/data    # Permissão apenas quem criou
sudo chmod -R 777 ~/.node-red         # Permissão todos usuarios
```

## Conclusion

Following these instructions should help you set up and manage your Node-RED instance within a Docker container. For more detailed information on Node-RED and Docker integration, refer to the official [Node-RED documentation](https://nodered.org/docs/).

## Getting Started
- [Installing Node-RED](https://nodered.org/docs/getting-started)
- [Creating your first flow](https://nodered.org/docs/tutorials/first-flow)
- [Node-RED Concepts](https://nodered.org/docs/user-guide/concepts)
- [Using the Node-RED Editor](https://nodered.org/docs/user-guide/editor)
- [InfluxDB with Node-Red](https://funprojects.blog/2020/02/01/influxdb-with-node-red/).
