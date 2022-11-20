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
| `dev-wolfi` `dev-wolfi-20221120` | `sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e) | `amd64` |
| `dev-alpine` `dev-alpine-20221120` | `sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca) | `amd64` `arm64` |
| `dev-wolfi-20221119` | `sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027) | `amd64` |
| `testing-20221117` | `sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313) | `amd64` |
| `testing` `testing-20221118` | `sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8) | `amd64` |
| `dev-wolfi-20221118` | `sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736) | `amd64` |
| `dev-alpine-20221119` | `sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157) | `amd64` `arm64` |
| `latest` | `sha256:50832e427cd55c22aee123af84eb35a7debb4729ac3b5f5699e39d5ebbcb3ac7`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:50832e427cd55c22aee123af84eb35a7debb4729ac3b5f5699e39d5ebbcb3ac7) | `amd64` `arm64` `armv7` |
| `0.0.1-r0-glibc` | `sha256:92c02b8516e1ac77f1c58077ed9efb3db9917d100c453e7f9ac72d247cfa59a2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:92c02b8516e1ac77f1c58077ed9efb3db9917d100c453e7f9ac72d247cfa59a2) |  |
| `dev-alpine-20221118` | `sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5) | `amd64` `arm64` |


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
        "docker-manifest-digest": "sha256:50832e427cd55c22aee123af84eb35a7debb4729ac3b5f5699e39d5ebbcb3ac7"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "71a0a52d5b4a5b31a49de46d7231b850d8908ce5",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/sdk",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQDBY8XZzKwx5CLL6Y2EVu2lD+W951qPx0P2d+SIrNgZugIgF22zAjbbAlzY9ybml1cULnPYqlRV8rOVGQb6q04P60Y=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIzMDI3ZTdhYjdiZjhjMTQxODAzZmMxMWQ1NjQ2ODE0N2M5ZjU5Y2E3ZTNmMDg4ZTY1YzY3NGU3ZmE5MDNiZDBlIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJQ25TQXYwVFZyOW1CM3Z3Z3FuUEN3RGg0Rk1LNHNEeVU4QUFEWWR6VmdVRUFpRUF3ZlEzZkNXdzl4cU9kWEVaS3NHMVZJeFNaeGQybW1PSVRkUEYwOE8wV3ZnPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUndWRU5EUVhsMVowRjNTVUpCWjBsVlJYZDRiRzkyVGpobFlWZEJZMlZUV21oMWRrWk5LMmx2TUVKSmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hkTlJFVjNUbFJCTWxkb1kwNU5ha2w0VFZSSmQwMUVSWGhPVkVFeVYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZwZEhOeGNrc3ZhVUozWlRGS1EydFhXVE5HYkhocVRHOUNTM0JhTTAxaGNXTjBkbWtLVnpCMlRFZ3pVV0pOWlZFelVHNVFPRGhMUTIxUVVVdHlSMVUwWTBSc01sQlVjRkZ6YVRoTGIxcEphR2huWTFOUU4zRlBRMEZyYjNkblowcEhUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZ4WmsxMkNsZHdkM3BLVlRoQ1VteEhkVVpFU0dRd2QySllkRkZGZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwUldVUldVakJTUVZGSUwwSkdjM2RYV1ZwWVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6VG10aGVUaDFXakpzTUdGSVZtbE1NMlIyWTIxMGJXSkhPVE5qZVRsNVdsZDRiRmxZVG14TWJteG9ZbGQ0UVdOdFZtMWplVGx2Q2xwWFJtdGplVGwwV1Zkc2RVMUVhMGREYVhOSFFWRlJRbWMzT0hkQlVVVkZTekpvTUdSSVFucFBhVGgyWkVjNWNscFhOSFZaVjA0d1lWYzVkV041Tlc0S1lWaFNiMlJYU2pGak1sWjVXVEk1ZFdSSFZuVmtRelZxWWpJd2QwWm5XVXRMZDFsQ1FrRkhSSFo2UVVKQloxRkpZekpPYjFwWFVqRmlSMVYzVG1kWlN3cExkMWxDUWtGSFJIWjZRVUpCZDFGdlRucEdhRTFIUlRGTmJWRXhXV3BTYUU1WFNYcE5WMFV3VDFkU2JFNUVXbXRPZWtsNlRWZEpORTVVUW10UFJHdDNDazlIVG14T1ZFRmpRbWR2Y2tKblJVVkJXVTh2VFVGRlJVSkJOVVJqYlZab1pFZFZaMVZ0Vm5OYVYwWjZXbFJCYWtKbmIzSkNaMFZGUVZsUEwwMUJSVVlLUWtKV2FtRkhSbkJpYldReFdWaEthMHhYYkhSWlYyUnNZM2s1ZWxwSGMzZElVVmxMUzNkWlFrSkJSMFIyZWtGQ1FtZFJVR050Vm0xamVUbHZXbGRHYXdwamVUbDBXVmRzZFUxSlIwdENaMjl5UW1kRlJVRmtXalZCWjFGRFFraDNSV1ZuUWpSQlNGbEJNMVF3ZDJGellraEZWRXBxUjFJMFkyMVhZek5CY1VwTENsaHlhbVZRU3pNdmFEUndlV2RET0hBM2J6UkJRVUZIUld0d1JrdFVaMEZCUWtGTlFWSjZRa1pCYVVWQmJqVkVWRUZsTm1aSFV5OU1MMlp2UTFNdmVra0tkRlpJSzI0NGIyOUhOR05PTjNBeVpVeEdhVVYwYm5ORFNVUm5Wek5CUlc1MFEyOXZZMHhOUWxnNFZGYzNaRzFqYWtST1ZYSXlPV3hETmxCR1dGbzBWd3BVUW5JNFRVRnZSME5EY1VkVFRUUTVRa0ZOUkVFeVowRk5SMVZEVFZGRVl6TnpWbUpRTWtoM1ZYWXZhMDVJUmt4WU9UQjJXa05OVW1NdlluaGFZVkZLQ2t4YVkzVXhjRzF4U2k5bE1sVlhOSGhpVHpSYVUyZFZSMUI1T0N0TGJFRkRUVVV2WTNsMGJYcDZiRkJ1V0dKSlVrRjVUSFZWVjNkak9HcE9WalpqYjJFS1FreGtOazVIYTIwMlFrMVBSMmN5UWtkNldFdFhNSEJMYVVKbWQyMUpaRTkzZHowOUNpMHRMUzB0UlU1RUlFTkZVbFJKUmtsRFFWUkZMUzB0TFMwSyJ9fX19",
          "integratedTime": 1668906313,
          "logIndex": 7448758,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/sdk/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/sdk",
      "githubWorkflowSha": "71a0a52d5b4a5b31a49de46d7231b850d8908ce5",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3505787310",
      "sha": "71a0a52d5b4a5b31a49de46d7231b850d8908ce5"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko).

