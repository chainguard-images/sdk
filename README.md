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
| `dev-wolfi-20221120` | `sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e) | `amd64` |
| `0.0.1-r0-glibc` | `sha256:92c02b8516e1ac77f1c58077ed9efb3db9917d100c453e7f9ac72d247cfa59a2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:92c02b8516e1ac77f1c58077ed9efb3db9917d100c453e7f9ac72d247cfa59a2) |  |
| `testing` `testing-20221118` | `sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8) | `amd64` |
| `dev-alpine-20221118` | `sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5) | `amd64` `arm64` |
| `dev-alpine-20221119` | `sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157) | `amd64` `arm64` |
| `dev-alpine` `dev-alpine-20221120` | `sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca) | `amd64` `arm64` |
| `dev-wolfi-20221119` | `sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027) | `amd64` |
| `latest` | `sha256:a9eed31fc5cc01b4900d62ed7025c34eb059629d8418162e176cf390040746d9`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a9eed31fc5cc01b4900d62ed7025c34eb059629d8418162e176cf390040746d9) | `amd64` `arm64` `armv7` |
| `testing-20221117` | `sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313) | `amd64` |
| `dev-wolfi-20221118` | `sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736) | `amd64` |
| `dev-wolfi` `dev-wolfi-20221121` | `sha256:211bc053fa50e2bdf0887829d39c7b544c11992cbbca2319b3ed077011837c35`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:211bc053fa50e2bdf0887829d39c7b544c11992cbbca2319b3ed077011837c35) | `amd64` |


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
        "docker-manifest-digest": "sha256:a9eed31fc5cc01b4900d62ed7025c34eb059629d8418162e176cf390040746d9"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "9bca32c69d85b3d151eccef1fefffcfd82554cae",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/sdk",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIDKTAvBIM45S+S6BdwT+xDzouNJbEkwErwS4mXyjHk3SAiEAo347NugOu2iqw7sbUg2qcsPoJglI6381gLHLmw8IzZs=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIzZmVlMWRkOWE5YWZiMmM2NzBjNmI3YjA0NjNkZTgwYzcwNDBlMjk4Yjk4MmZlYWZmYmMzM2Q1ODI2NDAzNTg4In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJQzFONnhSZ2srOVE0ZWdwenNOUTRlNm5MQXpkMlovM0lYaEFScnJnV2VWREFpRUFtK1hIOFpDMjZhQVg4RWZCT3N0SmFkRFZGWG1jZVVxMXJLSkRZK3VPMk9nPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUndha05EUVhsNVowRjNTVUpCWjBsVllVZzFOSGx6WjBkd1ZsUkZNWEZzWVVzNVpIQnZRbWhGUXl0bmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hoTlJFVjNUMVJSTUZkb1kwNU5ha2w0VFZSSmVFMUVSWGhQVkZFd1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVYwVWs5blZtRlZia3AxZG5rMVdXUlJZbWhyTUc1TWNFTnFTVUZWTkU1SE5tWkpXa2NLWnpCRGVsbFZWVkE0TURSMU5rdFhXRXRwU3pCWFdtaGpaekoyT1RaemVGcDZjMmRIUjFGdWJIUnVibEpoZHpRM1YwdFBRMEZyYzNkblowcElUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlYxTXk5MUNtVXZLM1prWm1Kd1FYcFdjRkpSYTBkemVFVkhOVEEwZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwUldVUldVakJTUVZGSUwwSkdjM2RYV1ZwWVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6VG10aGVUaDFXakpzTUdGSVZtbE1NMlIyWTIxMGJXSkhPVE5qZVRsNVdsZDRiRmxZVG14TWJteG9ZbGQ0UVdOdFZtMWplVGx2Q2xwWFJtdGplVGwwV1Zkc2RVMUVhMGREYVhOSFFWRlJRbWMzT0hkQlVVVkZTekpvTUdSSVFucFBhVGgyWkVjNWNscFhOSFZaVjA0d1lWYzVkV041Tlc0S1lWaFNiMlJYU2pGak1sWjVXVEk1ZFdSSFZuVmtRelZxWWpJd2QwWm5XVXRMZDFsQ1FrRkhSSFo2UVVKQloxRkpZekpPYjFwWFVqRmlSMVYzVG1kWlN3cExkMWxDUWtGSFJIWjZRVUpCZDFGdlQxZEthbGxVVFhsWmVsazFXa1JuTVZscVRtdE5WRlY0V2xkT2FscFhXWGhhYlZadFdtMWFhbHB0VVRSTmFsVXhDazVIVG1oYVZFRmpRbWR2Y2tKblJVVkJXVTh2VFVGRlJVSkJOVVJqYlZab1pFZFZaMVZ0Vm5OYVYwWjZXbFJCYWtKbmIzSkNaMFZGUVZsUEwwMUJSVVlLUWtKV2FtRkhSbkJpYldReFdWaEthMHhYYkhSWlYyUnNZM2s1ZWxwSGMzZElVVmxMUzNkWlFrSkJSMFIyZWtGQ1FtZFJVR050Vm0xamVUbHZXbGRHYXdwamVUbDBXVmRzZFUxSlIweENaMjl5UW1kRlJVRmtXalZCWjFGRFFrZ3dSV1YzUWpWQlNHTkJNMVF3ZDJGellraEZWRXBxUjFJMFkyMVhZek5CY1VwTENsaHlhbVZRU3pNdmFEUndlV2RET0hBM2J6UkJRVUZIUld3M2RtdHRkMEZCUWtGTlFWTkVRa2RCYVVWQkszQnZaa3R2U1M5WE5uZ3pkMFZWT0hOM2RqY0tTMnBTUm1RcmJVSjNhRWRzTTA5NVF6UTFaMmhFWTFGRFNWRkRkbEEyV1c1eWF6bHRiVkIxTkdsQmJVOUxZVlJYWkdZMlVIaHdjR05rY1ZKU1VXOHhWQXBUU1dOaE1tcEJTMEpuWjNGb2EycFBVRkZSUkVGM1RtOUJSRUpzUVdwRlFUaDJSV1JVS3pkSGExY3JiRGh6YlhBMGVVMVVSbWR5ZG5jclNtZ3dObkpYQ2pScU0zTktUbGhQTVVkdVduVk1iU3RsT1VORlRsVklXVVUxVjFNd2FtNXhRV3BDWkdjck5YTmFkbUZSUmpkbFZtTklaRE5OTTJKd2VIbHZaR1JNVEV3S0wyWTBWRnBIV0hacVV6bDVZazlWZGpCWFNXNDRZeXRYV1RZNFEwOHhZMHh0VUVVOUNpMHRMUzB0UlU1RUlFTkZVbFJKUmtsRFFWUkZMUzB0TFMwSyJ9fX19",
          "integratedTime": 1668992991,
          "logIndex": 7507867,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/sdk/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/sdk",
      "githubWorkflowSha": "9bca32c69d85b3d151eccef1fefffcfd82554cae",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3510474728",
      "sha": "9bca32c69d85b3d151eccef1fefffcfd82554cae"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko).

