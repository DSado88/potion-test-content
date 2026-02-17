# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Dark mode support for all pages
- Export to PDF functionality

### Changed
- Improved search performance by 3x

## [2.1.0] - 2026-02-10

### Added
- Real-time collaboration via WebSocket
- User presence indicators
- Inline commenting on documents
- `Ctrl+K` command palette

### Changed
- Upgraded React from 18.2 to 19.0
- Migrated from Webpack to Turbopack
- Redesigned settings page

### Fixed
- Fixed memory leak in document editor (#1201)
- Fixed incorrect pagination on search results (#1198)
- Fixed dark mode flicker on page load (#1195)

### Security
- Updated dependencies to patch CVE-2026-1234

## [2.0.0] - 2026-01-15

### Added
- **BREAKING:** New API v2 with different response format
- Multi-workspace support
- Team permissions and roles
- Audit log for all actions

### Changed
- **BREAKING:** Authentication now requires OAuth 2.0
- Redesigned the entire UI with new design system
- Improved accessibility (WCAG 2.1 AA compliance)

### Removed
- **BREAKING:** Removed API v1 endpoints
- Removed legacy CSV export (use API instead)
- Removed IE11 support

### Migration Guide

1. Update your API client to use v2 endpoints
2. Migrate authentication to OAuth 2.0 flow
3. Update any CSV export scripts to use the API
4. See [Migration Guide](./migration-v2.md) for details

## [1.5.2] - 2025-12-01

### Fixed
- Fixed crash when opening documents with >10k lines
- Fixed timezone handling in date picker
- Fixed file upload size limit not being enforced

## [1.5.1] - 2025-11-15

### Fixed
- Hotfix for login loop on Safari
- Fixed missing translations for Japanese locale

## [1.5.0] - 2025-11-01

### Added
- Document templates
- Keyboard shortcuts customization
- Offline mode (read-only)

### Changed
- Improved loading times by 40%
- Better error messages for API failures
