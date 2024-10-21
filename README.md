# Sup de Vinci - Containers module project

*Tested with `rust v1.82.0` et `node 23.0.0`.*

## Development

### API

#### Basics

Use `cargo run` to start the dev environment.

You can also install [cargo-watch](https://crates.io/crates/cargo-watch) to watche over your project's source for changes, and runs Cargo commands when they occur : `cargo-watch -x run`.

#### Using Docker

You can use the compose.yml file to start the dev environment.

```bash
docker-compose up -d  # -d or --detach to run in background
```

You can also use an argument to specify the service you want to run, like `docker-compose up -d sdv-api`.

### Web

#### Basics

Use `npm install` to install all dependancies, and `npm run dev` to start the dev environment.

#### Using Docker

You can use the compose.yml file to start the dev environment.

```bash
docker-compose up -d  # -d or --detach to run in background
```

You can also use an argument to specify the service you want to run, like `docker-compose up -d sdv-web`.

## Production

### API

#### Basics

Run `cargo build --release` to build and compile the app. This will create an executable in `/target/release/sdv-api`.

#### Using Docker

To build the Docker image for the production environment, run the following command in the root directory of the project (sdv-api):

```bash
docker build -t <image-name:tag> .
```

### Web

#### Basics

Run `npm run build` to build the application, and run `npm run start` to start the Node.js server. 

#### Using Docker

To build the Docker image for the production environment, run the following command in the root directory of the project (sdv-web):

```bash
docker build -t <image-name:tag> .
```

## CI/CD

### GitHub Actions

The project uses GitHub Actions to automate the CI/CD process. The workflow is defined in the `.github/workflows` directory.

### Docker Hub

The project uses Docker Hub to store the Docker images. The images are automatically pushed to Docker Hub when a new release is created, and pushed to the `main` branch.

## Authors

- __Jarod Guichard__

### Liens

- [GitHub](https://github.com/Dassault7/sdv-m1do-containers-project)
- [Docker Hub](https://hub.docker.com/repositories/dassault7)
