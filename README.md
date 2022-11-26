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
| `latest` | `sha256:7c14296da5be9f118096ce905ba9b61279ba1976eab85c8bda614edbbf94c4ca`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7c14296da5be9f118096ce905ba9b61279ba1976eab85c8bda614edbbf94c4ca) | `amd64` `arm64` `armv7` |
| `testing-20221117` | `sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e198df88dcb8ef760794218a309330e0b8b3c8e1dd4c211f2951f87be1f47313) | `amd64` |
| `testing` `testing-20221118` | `sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d6e6172257fba34e9c39e8ccd6f7292c1634357b552da0527269f3e66171c4e8) | `amd64` |
| `dev-wolfi-20221119` | `sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:aefddde028e9c3d271e7a3254cd917eb249581d3a76d1fade132243a9ebe0027) | `amd64` |
| `dev-wolfi-20221120` | `sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5475c40123a6ebbfd4aab4fa77ab7a3f7189e8084c9bd59c718ac8a585afc21e) | `amd64` |
| `dev-wolfi-20221121` | `sha256:94a61c7857febefef01c12f364bcc582296d1b39b3ac1fba84a3b908cf0607f2`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:94a61c7857febefef01c12f364bcc582296d1b39b3ac1fba84a3b908cf0607f2) | `amd64` |
| `dev-alpine-20221123` | `sha256:abc19835b5c35dff2d33041da5e30846598601eb4bc05d86fdc17651c4016538`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:abc19835b5c35dff2d33041da5e30846598601eb4bc05d86fdc17651c4016538) | `amd64` `arm64` |
| `dev-wolfi` `dev-wolfi-20221126` | `sha256:aa430f502c3d91198f0a2ac23d5e8956c10ada8c79498c81772bdff34a729013`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:aa430f502c3d91198f0a2ac23d5e8956c10ada8c79498c81772bdff34a729013) | `amd64` |
| `dev-alpine-20221118` | `sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ed43cbaa2a57c14034aec99ac48c4ea89eed8aca8bc52a1d327e33e2d2a7cad5) | `amd64` `arm64` |
| `dev-alpine-20221120` | `sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:4c806210640ffce120e92d6b708c48b5fc90a347536ebc671f4a0122bf7ebfca) | `amd64` `arm64` |
| `0.0.1-r0-glibc` | `sha256:df17e6f480a5d191612599c5f83abfe98229f8923454812e838c5d4b6b5f4a2c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:df17e6f480a5d191612599c5f83abfe98229f8923454812e838c5d4b6b5f4a2c) |  |
| `dev-alpine-20221121` | `sha256:d17b5535920b7ee245c51f3d0f5d4317e925ad3bc6ac731c47956df0ba2fb9a4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d17b5535920b7ee245c51f3d0f5d4317e925ad3bc6ac731c47956df0ba2fb9a4) | `amd64` `arm64` |
| `dev-wolfi-20221122` | `sha256:ef2dc5677acae79e49be72cc0241cd7329dcf7b369ce645e35cdc8f356f9aeee`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ef2dc5677acae79e49be72cc0241cd7329dcf7b369ce645e35cdc8f356f9aeee) | `amd64` |
| `dev-wolfi-20221124` | `sha256:2d836578c7c624eb1257f482ef6ec581285c965af2ac644b3cb3f1ea00d05264`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:2d836578c7c624eb1257f482ef6ec581285c965af2ac644b3cb3f1ea00d05264) | `amd64` |
| `dev-alpine-20221124` | `sha256:7203b3719a18f626a2efea1a552fce545bd4f537f63edce9d70e509fdb44f053`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7203b3719a18f626a2efea1a552fce545bd4f537f63edce9d70e509fdb44f053) | `amd64` `arm64` |
| `dev-wolfi-20221118` | `sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:5b49de60a54bedb10578bff89509a04cfcf44978fbe17f5c823a78741bdd6736) | `amd64` |
| `dev-alpine` `dev-alpine-20221125` | `sha256:3633ae4ec4f28b15fa084e9e7f684197c021f0ee58a91736f30167fbff9bee11`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:3633ae4ec4f28b15fa084e9e7f684197c021f0ee58a91736f30167fbff9bee11) | `amd64` `arm64` |
| `dev-alpine-20221119` | `sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:8aabbaf50bf153583a523e5ff0db915fa232208a4791fa8fbd16005ba80b4157) | `amd64` `arm64` |
| `dev-alpine-20221122` | `sha256:130d2accbfe32c4a83a20ec0632661834b4ee732715f3ffa33f72ab3dd5080c4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:130d2accbfe32c4a83a20ec0632661834b4ee732715f3ffa33f72ab3dd5080c4) | `amd64` `arm64` |
| `dev-wolfi-20221123` | `sha256:69adc4d96dc34877f831af12f04d752acc4869a0853530736864138227efd377`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:69adc4d96dc34877f831af12f04d752acc4869a0853530736864138227efd377) | `amd64` |
| `dev-wolfi-20221125` | `sha256:65b371411fae5350b91f65c8c831e6bb35699862f6d8dcbab7ea71511b12a182`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:65b371411fae5350b91f65c8c831e6bb35699862f6d8dcbab7ea71511b12a182) | `amd64` |


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
        "docker-manifest-digest": "sha256:7c14296da5be9f118096ce905ba9b61279ba1976eab85c8bda614edbbf94c4ca"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "push",
      "1.3.6.1.4.1.57264.1.3": "9f829613a2134b20e35f764f1487445581fc6db5",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/sdk",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIFz50tMulxjOw6ZS+A0n7Gy2CsPkA9b9VP0dggKsMqb0AiEA+JOV20SgL39JAER2lUTkLDg2cDF6jOY5P/mJfouDokw=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI2NGMzODc1MTAyMDFlMWZjYTNjMDlkNDMxMjY2ZWU4OGQ3Y2Y2ZGZkNTUxYzhjMDllMGI3NzEyZDFhNTk4M2EyIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUURBSkpuUjI3S1FXT3M0Lzk1MjJtb2FXOW1Ua2xadWFjMzZsTi91Nkp3UzFBSWhBSWZmMnF0b0lkSEIvSG5WRFV4T2dSZzRDWm9IOXJvV0d4ZCtmUlJwbWkveiIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnZha05EUVhscFowRjNTVUpCWjBsVlNYVkxReTlWYWxvclZrdExVWGRpZVU5RGVXb3pRWHBpTVV3d2QwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1RGTlZFbDZUMFJOTTFkb1kwNU5ha2w0VFZSSk1VMVVTVEJQUkUwelYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVY1UVRkT1lsZzFia3hCVWxVeFNYQkRPWHBKU1hrdllYbzBWRlkzUWtGNVRURkxZVGNLWlZrd1dVSlNNV1oyWW5aRVNtWkdkV1pzY25kSVkyd3lWMFpEWW1ReE1URlNkbWt4TjFSVWIwUnBkMEY2UkdsSWFIRlBRMEZyWTNkblowcEVUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlYyUm5GS0NsaDJlazl3UW10dVpVdFhMM0pHZEZSTWJuWkdhaXMwZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwUldVUldVakJTUVZGSUwwSkdjM2RYV1ZwWVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d6VG10aGVUaDFXakpzTUdGSVZtbE1NMlIyWTIxMGJXSkhPVE5qZVRsNVdsZDRiRmxZVG14TWJteG9ZbGQ0UVdOdFZtMWplVGx2Q2xwWFJtdGplVGwwV1Zkc2RVMUVhMGREYVhOSFFWRlJRbWMzT0hkQlVVVkZTekpvTUdSSVFucFBhVGgyWkVjNWNscFhOSFZaVjA0d1lWYzVkV041Tlc0S1lWaFNiMlJYU2pGak1sWjVXVEk1ZFdSSFZuVmtRelZxWWpJd2QwVm5XVXRMZDFsQ1FrRkhSSFo2UVVKQloxRkZZMGhXZW1GRVFUSkNaMjl5UW1kRlJRcEJXVTh2VFVGRlJFSkRaelZhYW1kNVQxUlplRTB5UlhsTlZFMHdXV3BKZDFwVVRURmFhbU15VGtkWmVFNUVaek5PUkZFeFRsUm5lRnB0VFRKYVIwa3hDazFDZDBkRGFYTkhRVkZSUW1jM09IZEJVVkZGUkd0T2VWcFhSakJhVTBKVFdsZDRiRmxZVG14TlEwMUhRMmx6UjBGUlVVSm5OemgzUVZGVlJVWlhUbThLV1Zkc2RWb3pWbWhqYlZGMFlWY3hhRm95Vm5wTU0wNXJZWHBCWkVKbmIzSkNaMFZGUVZsUEwwMUJSVWRDUVRsNVdsZGFla3d5YUd4WlYxSjZUREl4YUFwaFZ6UjNaMWx6UjBOcGMwZEJVVkZDTVc1clEwSkJTVVZtVVZJM1FVaHJRV1IzUkdSUVZFSnhlSE5qVWsxdFRWcElhSGxhV25walEyOXJjR1YxVGpRNENuSm1LMGhwYmt0QlRIbHVkV3BuUVVGQldWTjFla0ZaTDBGQlFVVkJkMEpKVFVWWlEwbFJReXRWYlRkemJXdDBRa056VlhkNFdISjRTM0V5U0d4NGVTc0tWVXB4ZVRoclJGWTRlbkpKY0dST04ybDNTV2hCVUdobFZuRkVjVFpLVlVkUmQycFhWVk5GYlVoa05FVmhlblJVTDBGVmVXSmFlRzlXTTJKMlpXWTVXZ3BOUVc5SFEwTnhSMU5OTkRsQ1FVMUVRVEpuUVUxSFZVTk5SbXBxYjBKMVQwTk5XREpsZUM5VVJVd3lXbTlDUTFGVFdsQkZWVk5WYjBsc1QyeDFWRzlzQ204M2FEVkpLMDB5TjJWS2JsTk9ZVTVNV25VeWJubGxiREJSU1hoQlQxcG1SMWRLUm05cmNYTkNWRlJJWlhKTE9EWnJPRmxhYkV4eVEzUmpRMnRXZDJnS2QyTkxSV05YT1ZrdmVtZE1lVXRITm1ZeWVrWTNlR2RhWVVOdWFUWkJQVDBLTFMwdExTMUZUa1FnUTBWU1ZFbEdTVU5CVkVVdExTMHRMUW89In19fX0=",
          "integratedTime": 1669379928,
          "logIndex": 7825190,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/sdk/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/sdk",
      "githubWorkflowSha": "9f829613a2134b20e35f764f1487445581fc6db5",
      "githubWorkflowTrigger": "push",
      "run_attempt": "1",
      "run_id": "3547806515",
      "sha": "9f829613a2134b20e35f764f1487445581fc6db5"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [melange](https://github.com/chainguard-dev/melange) and [apko](https://github.com/chainguard-dev/apko).

