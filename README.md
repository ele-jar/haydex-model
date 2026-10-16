# Haydex scanner models

Versioned ONNX weights for the Haydex browser scanner. Inference runs on the visitor's device.

Current model: **v3-7ddc7003a914d5ee** · 430 item classes · 224px item input · 32px digit input.

## Downloads

The [GitHub Release](https://github.com/ele-jar/haydex-model/releases/tag/v3-7ddc7003a914d5ee) contains `items.onnx`, `digits.onnx`, `manifest.json`, and `SHA256SUMS`.

| File | Bytes |
| --- | ---: |
| items.onnx | 97474665 |
| digits.onnx | 1427158 |

## Browser downloads

GitHub release download URLs do not provide the cross-origin response headers needed by browser `fetch`. The website uses the same files from this repository's pinned version tag:

```text
https://raw.githubusercontent.com/ele-jar/haydex-model/v3-7ddc7003a914d5ee/items.onnx
https://raw.githubusercontent.com/ele-jar/haydex-model/v3-7ddc7003a914d5ee/digits.onnx
```

The scanner checks exact byte sizes and SHA-256 hashes against its bundled manifest before activation, and caches verified weights in IndexedDB. A release tag must keep matching weights and metadata. Publish changed models under a new tag and update the website manifest together.

## Verify

```bash
sha256sum -c SHA256SUMS
```

This repository distributes model files. The main website source remains in `ele-jar/hayday`. GitHub hosting remains subject to GitHub's service policies and availability.
