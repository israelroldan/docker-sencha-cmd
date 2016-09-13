# Supported tags and respective `Dockerfile` links

- [`6.2.0.103`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.2.0.103/Dockerfile), [`6.2.0`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.2.0.103/Dockerfile), [`6.2`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.2.0.103/Dockerfile), [`latest`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.2.0.103/Dockerfile) [_(v6.2.0.103/Dockerfile)_](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.2.0.103/Dockerfile)
- [`6.1.3.42`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.1.3.42/Dockerfile), [`6.1.3`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.1.3.42/Dockerfile), [`6.1`](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.1.3.42/Dockerfile) [_(v6.1.3.42/Dockerfile)_](https://github.com/israelroldan/docker-sencha-cmd/blob/v6.1.3.42/Dockerfile)

For more information about the changes in this version please check the [release notes](http://cdn.sencha.com/cmd/6.2.0.103/release-notes.html). This image is updated automatically on each generally available release of Sencha Cmd.

# What is Sencha Cmd?
Sencha Cmd is the cornerstone for building your Sencha Ext JS and Sencha Touch applications. Sencha Cmd provides a full set of lifecycle management features such as scaffolding, code minification, production build generation, and more, to complement your Sencha projects.
![](https://www.sencha.com/wp-content/uploads/2015/03/sencha-cmd-hero.png)

# How to use this image?

## Standalone applications

Standalone applications are those where workspace.json is at the root of the app (a single-application workspace).
To run any command over your codebase, just mount it over at `/code`:

    docker run -it -v /some/local/dir:/code sencha/cmd app build

## Multi-application workspace

Besides mounting your workspace at `/code` you'll need to specify the application directory to work on. This is done using the `--workdir` parameter. For example, to build an application located in the `myapp` directory inside the mounted workspace, you'd need to run this command:

    docker run -it -v /some/local/workspace:/code --workdir=/code/myapp sencha/cmd app build

# What's included?

This image is based on [OpenJDK's image](https://hub.docker.com/_/openjdk/) ([`openjdk:8-jre-alpine`](https://github.com/docker-library/openjdk/blob/54c64cf47d2b705418feb68b811419a223c5a040/8-jdk/alpine/Dockerfile)), so it is based on an Alpine Linux distribution.
 
- OpenJDK 8 JRE
- Ruby 2.2
- Sencha Cmd 6.2.0.103 with Compass extensions

## Including this image in your `Dockerfile`

You can include this image in your `Dockerfile`:

    FROM sencha/cmd:latest
    COPY . /code
    CMD ['app', 'build']

# License

Sencha Cmd is licensed commercially for free.<br>See [http://www.sencha.com/legal/sencha-tools-software-license-agreement](http://www.sencha.com/legal/sencha-tools-software-license-agreement) for license terms.

# User feedback

## Issues 

If you have any problems with or questions about Sencha Cmd, please use our [Forums](https://www.sencha.com/forum/forumdisplay.php?8-Sencha-Cmd) or [Support Portal](https://support.sencha.com/#login).

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/israelroldan/docker-sencha-cmd/issues).

## Contributing

You are invited to contribute new features, fixes, or updates. We'll do our best to process your pull requests as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/israelroldan/docker-sencha-cmd/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.