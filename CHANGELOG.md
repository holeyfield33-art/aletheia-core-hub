# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.5.0] - 2026-04

### Added
- Receipt replay protection
- Threat level discretization to bands
- Timing-safe API key comparison
- XFF IP spoofing fix
- Fail-closed circuit breaker for Redis errors
- Unicode NFKC normalization on all inputs
- Veto reason sanitization

### Changed
- Shadow verdict oracle removed
- Test suite expanded to 502 passing tests across 19 files

## [1.4.7] - 2026-03

### Added
- HMAC receipts on all enforcement decisions
- Upstash Redis rate limiting integration
- Ed25519 manifest signing

### Fixed
- Rate limit bypass via header manipulation

## [1.4.0] - 2026-03

### Added
- Tri-agent pipeline: Scout, Nitpicker, Judge
- Cryptographically verifiable enforcement decisions
- Initial policy manifest schema

## [1.0.0] - 2026-02

### Added
- Initial release as aletheia-cyber-core on PyPI
- FastAPI bridge (bridge.fastapi_wrapper)
- Core enforcement engine
- Basic BLOCK / ALLOW decision logic
- Trusted Publishers deployment to PyPI
