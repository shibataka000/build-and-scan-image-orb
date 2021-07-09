# Build and Scan Image Orb

[![CircleCI](https://circleci.com/gh/shibataka000/build-and-scan-image-orb.svg?style=shield)](https://circleci.com/gh/shibataka000/build-and-scan-image-orb)

Build and scan Dockerfile and container image by following tools.

- [hadolint](https://github.com/hadolint/hadolint)
- [dockle](https://github.com/goodwithtech/dockle)
- [trivy](https://github.com/aquasecurity/trivy)
- [docker scan](https://github.com/docker/scan-cli-plugin) (option)

## Usage

### Examples
See [examples](./src/examples) .

### Ignore specific violations and vulnerabilities
Tools ([hadolint](https://github.com/hadolint/hadolint), [dockle](https://github.com/goodwithtech/dockle), [trivy](https://github.com/aquasecurity/trivy)) provide some way to ignore specific violations and vulnerabilities.

- Using configuration file
    - `.hadolint.yaml`
    - `.dockleignore`
    - `.trivyignore`
- Using inline comment (hadolint only)

See document of each tools for more details.

### Commercial usage
Some of trivy's data sources, especially for programing language, are only licensed for non-commercial usage. See following sites for more details.

- https://github.com/aquasecurity/trivy/blob/main/docs/vuln-detection/data-source.md
- https://github.com/aquasecurity/trivy/issues/491

If you use this action for commercial usage, you MUST set `trivy-vuln-type` option as `os` and use trivy without non-commercial data sources.
