# Vanilla OS Kipferl NVIDIA Modern Image

Containerfile for building a Vanilla OS Kipferl + NVIDIA image.

This image is based on top of [`Vanilla-KDE/desktop-image`](https://github.com/Vanilla-KDE/desktop-image/pkgs/container/kde) and offers the default Vanilla OS Desktop experience with KDE Plasma and NVIDIA drivers.

## Build

```bash
vib build recipe.yml
podman image build -t vanillakde/kipferl-nvidia-modern .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-OS/nvidia-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-kde/kde:latest --owner Vanilla-KDE
```
