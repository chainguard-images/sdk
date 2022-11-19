# sdk

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/sdk/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/sdk/actions/workflows/release.yaml)

Development image for [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko).

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/sdk:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `latest` | `sha256:7dc615b80a61e0bfa00b41861b217bc7b05fb88580d918d0063014194d2c80b2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7dc615b80a61e0bfa00b41861b217bc7b05fb88580d918d0063014194d2c80b2) | `amd64` `arm64` `armv7` |
| `0.0.1-r0-glibc` | `sha256:376fe3a1606f1257886de39623bbfe917c37badc17a8b23c77c6502e8cc51c03`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:376fe3a1606f1257886de39623bbfe917c37badc17a8b23c77c6502e8cc51c03) |  |
| `testing-20221117` | `sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313) | `amd64` |
| `testing` `testing-20221118` | `sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8) | `amd64` |
| `dev-wolfi` `dev-wolfi-20221118` | `sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736) | `amd64` |
| `dev-alpine` `dev-alpine-20221118` | `sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5) | `amd64` `arm64` |


## Usage

### With melange

Clone down your development fork/branch:

```
git clone https://github.com/chainguard-dev/melange.git
cd melange
```

Run the image, mounting the repo workspace (`--privileged` flag required):

```
docker run --privileged --rm -it -v "${PWD}:${PWD}" -w "${PWD}" cgr.dev/chainguard/sdk
```

Upon entering the image, you should see the following welcome message:

```

Welcome to the development environment!


[sdk] ❯
```

Inside the environment, test out local changes to the melange codebase
by running the following:

```
make melange install
```

Then run melange commands as normal:

```
melange keygen

melange build \
  --arch x86_64,arm64 \
  --empty-workspace \
  --repository-append packages \
  --signing-key melange.rsa \
  examples/gnu-hello.yaml
```

### With apko

Clone down your development fork/branch:

```
git clone https://github.com/chainguard-dev/apko.git
cd apko
```

Run the image, mounting the repo workspace:

```
docker run --rm -it -v "${PWD}:${PWD}" -w "${PWD}" cgr.dev/chainguard/sdk
```

Upon entering the image, you should see the following welcome message:

```

Welcome to the development environment!


[sdk] ❯
```

Inside the environment, test out local changes to the apko codebase
by running the following:

```
make apko install
```

Then run apko commands as normal:

```
apko build --debug \
  examples/alpine-base.yaml \
  alpine-base:latest output.tar
```


## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/sdk:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/sdk:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/sdk"
      },
      "image": {
        "docker-manifest-digest": "sha256:7dc615b80a61e0bfa00b41861b217bc7b05fb88580d918d0063014194d2c80b2"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "c99edd9a86073ae6ac4e01922a0d1098cc151669",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/sdk",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCICIVSCoeH/fOjy3KhP6/cw/ZVBct0Mz/BpyI19aJomj4AiEAqqGiSNsvcC/d4Cl36xIrTWK0nPK8lfPyVz1FH2slrsY=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI1NjMwMjRkMjkxNjNkZGNlOWVlZWNhMWRjMDQ1YjkyNjI5OTZkNGU2YTI4Zjg2ZGM5MDJiZmExYzkyY2U0MWNjIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FUUNJRjZuTkg5Yk0zaVErSmF1SkNLVzFOOE1lWC9uSlRLSFV6WWtjQ1ZaQ2dmd0FpQXBJa1FMeWFLNVBqNkZrUnBLMmJZV0VhWFMzTTJGOVdqNTgzZkJWZ0dEL3c9PSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUndha05EUVhsNVowRjNTVUpCWjBsVlNrZHZaamhEUzFKRVNIQmxMekJtTkVJME5WWlZSVUozZVdwVmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUlRWTlJFVjNUWHBGTkZkb1kwNU5ha2w0VFZSRk5VMUVSWGhOZWtVMFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVY1WlhRdlUxVnNOMFp6UmxaaVNreHJSMnM0UVdORWFVRkRVRlJEVG14TU1FcFpORFFLVG1saVdDODJNMkp2Ym1sa1pFUkJZMlZrYWxSWlFuZFZNRVoxVDNOUWFYQTVVbXhtTHpkcWNGUmthVFZQT0VGMmJqWlBRMEZyYzNkblowcElUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZxSzFaM0NtcE1lRTQzY0ZSUFVqbG5Va0p3UkRSTVVGcGpZMmx2ZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwUldVUldVakJTUVZGSUwwSkdjM2RYV1ZwWVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6VG10aGVUaDFXakpzTUdGSVZtbE1NMlIyWTIxMGJXSkhPVE5qZVRsNVdsZDRiRmxZVG14TWJteG9ZbGQ0UVdOdFZtMWplVGx2Q2xwWFJtdGplVGwwV1Zkc2RVMUVhMGREYVhOSFFWRlJRbWMzT0hkQlVVVkZTekpvTUdSSVFucFBhVGgyWkVjNWNscFhOSFZaVjA0d1lWYzVkV041Tlc0S1lWaFNiMlJYU2pGak1sWjVXVEk1ZFdSSFZuVmtRelZxWWpJd2QwWm5XVXRMZDFsQ1FrRkhSSFo2UVVKQloxRkpZekpPYjFwWFVqRmlSMVYzVG1kWlN3cExkMWxDUWtGSFJIWjZRVUpCZDFGdldYcHJOVnBYVW10UFYwVTBUbXBCTTAweVJteE9iVVpxVGtkVmQwMVVhM2xOYlVWM1drUkZkMDlVYUdwWmVrVXhDazFVV1RKUFZFRmpRbWR2Y2tKblJVVkJXVTh2VFVGRlJVSkJOVVJqYlZab1pFZFZaMVZ0Vm5OYVYwWjZXbFJCYWtKbmIzSkNaMFZGUVZsUEwwMUJSVVlLUWtKV2FtRkhSbkJpYldReFdWaEthMHhYYkhSWlYyUnNZM2s1ZWxwSGMzZElVVmxMUzNkWlFrSkJSMFIyZWtGQ1FtZFJVR050Vm0xamVUbHZXbGRHYXdwamVUbDBXVmRzZFUxSlIweENaMjl5UW1kRlJVRmtXalZCWjFGRFFrZ3dSV1YzUWpWQlNHTkJNMVF3ZDJGellraEZWRXBxUjFJMFkyMVhZek5CY1VwTENsaHlhbVZRU3pNdmFEUndlV2RET0hBM2J6UkJRVUZIUldwWGJFdDZaMEZCUWtGTlFWTkVRa2RCYVVWQmNuRlBWWEZ6ZUZkU2NXTlhVazlTVFdRd1RHZ0tlVkJqTVRReWQwUmFSVE5NUkZOMFJHd3hTM3BZUTJkRFNWRkVkekpGVjBjck1rWkpSVFJSYkZveGRIQllaR1V4VTBSalNEWnllV1JvTWpkWGMzUkpOZ3A1Y0RVcldYcEJTMEpuWjNGb2EycFBVRkZSUkVGM1RtOUJSRUpzUVdwQ09HZHNlREUwWW5WNEt6Vm9lVzVzUm1jNU1XYzFSVkE0VjBOTk5ISmFXaXRMQ2twNWFtSlBXV2RWT1UxRVFsTmhNazFJVm10aVpYQXdXRXBqWm5CMGN6QkRUVkZFYXk5a2RHVkdRbVp5Um5GRWFHTTJabmQ2TVhCSFIwNXlNbWRYWVhFS1MyTXpNREkxVjFGb0swWkljM0YzWnpKSFkxSjJjMmd3TUdWdmFYVjZiV2xHYTI4OUNpMHRMUzB0UlU1RUlFTkZVbFJKUmtsRFFWUkZMUzB0TFMwSyJ9fX19",
          "integratedTime": 1668819808,
          "logIndex": 7383347,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/sdk/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/sdk",
      "githubWorkflowSha": "c99edd9a86073ae6ac4e01922a0d1098cc151669",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3501237616",
      "sha": "c99edd9a86073ae6ac4e01922a0d1098cc151669"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko).

