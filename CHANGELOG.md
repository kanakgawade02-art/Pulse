# Changelog

## Unreleased — Song DNA + Poster Studio upgrade

### Added
- Song DNA dashboard for local audio files.
- Estimated energy, spectral brightness, bass share, dynamic range, and tempo metrics.
- A sampled loudness timeline to make the track's intensity changes easy to inspect.
- Analysis caching so opening Song DNA and then generating a poster does not decode and analyze the same file twice.
- Clearer local-file requirements and metric caveats.

### Improved
- Poster and analysis share the same analysis results.
- Poster preview is sized for smaller screens and the modal can scroll on mobile.
- README now documents features, limitations, local run steps, and Git workflow.

### Notes
- Analysis runs locally in the browser; audio files are not uploaded.
- Tempo and mood/profile labels are estimates based on audio features.
