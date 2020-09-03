A generic bundled spa in React, which introspects Swagger OpenAPI definitions file, to build automatically html forms (bootstrap4) for POST endpoints exchanging JSON

GOALs:
- build automatically an html form, by introspecting Swagger OpenAPI definitions file
- the introspection works at runtime, not at `npm` build time

non-GOALS:
- not a "low-code" app generator

# DEMO

Watch the video on YouTube:

[![Watch the video](https://img.youtube.com/vi/av_DoGNl2jI/hqdefault.jpg)](https://youtu.be/av_DoGNl2jI)

## Building and running on localhost

First install dependencies:

```sh
npm install
```

To create a production build:

```sh
npm run build-prod
```

To create a development build:

```sh
npm run build-dev
```

## Running

Open the file `dist/index.html` in your browser

## Deploying on Quarkus:

Add to Quarkus app `pom.xml` this project and webjars-locator dependencies:

```
<dependency>
    <groupId>org.kie</groupId>
    <artifactId>openapi-as-reactforms</artifactId>
    <version>1.0.0-SNAPSHOT</version>
    <scope>runtime</scope>
</dependency>
<dependency>
    <groupId>io.quarkus</groupId>
    <artifactId>quarkus-webjars-locator</artifactId>
</dependency>
```

Can now navigate to `http://localhost:8080/webjars/openapi-as-reactforms/index.html`.
