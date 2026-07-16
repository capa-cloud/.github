<p align="center">
  <img src="https://raw.githubusercontent.com/capa-cloud/.github/main/profile/banner.png" alt="Capa Cloud" width="600">
</p>

# Capa Cloud

Cloud Application APIs and multi-runtime experiments based on Mecha architecture principles.

[Documentation](https://capa.rxcloud.group/) · [Java SDK](https://github.com/capa-cloud/capa-java) · [Runtime](https://github.com/capa-cloud/capa)

## Project lifecycle

Capa Cloud contains projects at different maturity levels. Repository presence does not imply production support; check each README and recent CI before adopting it.

### Primary and maintained surfaces

| Project | Role | Status |
| --- | --- | --- |
| [capa-java](https://github.com/capa-cloud/capa-java) | Rich-SDK implementation for Java applications | Primary Java SDK |
| [capa-java-aws](https://github.com/capa-cloud/capa-java-aws) | AWS SPI modules for Capa Java | Adapter modules; capability support varies |
| [capa.io](https://github.com/capa-cloud/capa.io) | Website and bilingual documentation | Public documentation source |

### Runtime and API specifications

| Project | Language | Status |
| --- | --- | --- |
| [capa](https://github.com/capa-cloud/capa) | Go | Experimental sidecar/runtime; implemented features and roadmap are documented separately |
| [cloud-runtimes-jvm](https://github.com/capa-cloud/cloud-runtimes-jvm) | Java | JVM API contracts plus partial adapter scaffolds |
| [cloud-runtimes-golang](https://github.com/capa-cloud/cloud-runtimes-golang) | Go | Interface definitions; module path remains under `reactivegroup` for compatibility |
| [cloud-runtimes-python](https://github.com/capa-cloud/cloud-runtimes-python) | Python | Alpha interface definitions; no bundled runtime adapter |

### Historical and reference projects

The following repositories preserve earlier integrations, prototypes, or solution work. Treat them as reference material unless their own README and CI state say otherwise:

- [capa-go](https://github.com/capa-cloud/capa-go)
- [capa-java-alibaba](https://github.com/capa-cloud/capa-java-alibaba)
- [capa-operator](https://github.com/capa-cloud/capa-operator)
- [capa-bff](https://github.com/capa-cloud/capa-bff)
- [capa-injector](https://github.com/capa-cloud/capa-injector)
- [capa-java-adaptor](https://github.com/capa-cloud/capa-java-adaptor)

## Architecture

Capa's rich-SDK path lets an application program against standard runtime APIs while selecting replaceable SPI implementations for its deployment environment.

```text
Application
    ↓ standard Cloud Runtime APIs
Capa Java SDK
    ↓ component and SPI contracts
Cloud or middleware adapter
```

The experimental [capa](https://github.com/capa-cloud/capa) runtime explores a separate sidecar path. Do not assume identical capability coverage between the Java SDK and Go runtime.

## Capability areas

The API repositories define contracts across service invocation, configuration, pub/sub, state, secrets, bindings, telemetry, files, locks, and selected native protocols. Actual support depends on the chosen SDK/runtime and adapter.

## Start here

- Read the [Capa overview](https://capa.rxcloud.group/docs/overview/).
- For Java applications, follow the [capa-java README](https://github.com/capa-cloud/capa-java#readme).
- For the Go sidecar experiment, follow the [capa README](https://github.com/capa-cloud/capa#readme).
- Report documentation problems in [capa.io Issues](https://github.com/capa-cloud/capa.io/issues).

## Contributing

Open issues and pull requests in the repository that owns the affected API, SDK, adapter, runtime, or documentation. Public examples must not include credentials, private endpoints, customer data, or personal identifiers.

Most repositories use the Apache License 2.0; verify the license in the specific repository before reuse.
