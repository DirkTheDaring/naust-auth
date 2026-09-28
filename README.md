# naust-auth

Pure authentication, token issuance/verification, password hashing, and RBAC primitives for [Naust](https://github.com/DirkTheDaring/naust).

## Architectural Principles
- **Transport- and Storage-Free**: Pure domain security engine without HTTP handlers, network transports, or database connections.
- **Zero-Allocation Hot Path**: Shared configuration structures (`Arc<AuthConfig>`) for ultra-high throughput authorization decisions.
- **Constant-Time Verification**: Constant-time comparison for secrets and sentinel hashes to prevent timing attacks.
- **Strong Typing**: Built on [`naust-types`](https://github.com/DirkTheDaring/naust-types) (`CanonicalRepoName`, `RepositoryAccessPattern`).

## License
MIT
