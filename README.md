# 🔐 Auth gRPC Service - Proto + Go

Protobuf-first authentication service for microservices architecture. Provides both the API contract and Go server implementation.

---

## 🚀 gRPC Services

**Auth Service** — User authentication & token management
- `Auth.Login` — Authenticate user with login/password, receive JWT tokens
- `Auth.Register` — Create new user account
- `Auth.Refresh` — Rotate access and refresh tokens
- `Auth.Logout` — Invalidate session and tokens

**User Service** — Profile management
- `User.GetUser` — Get user profile by ID
- `User.UpdateUser` — Update login, email, or other profile data
- `User.ChangePassword` — Change password with old password confirmation

**Token Service** — Token validation for downstream services
- `Token.ValidateToken` — Verify JWT token, return user_id and roles

---

## 🛠️ Tech Stack

- **Protocol Buffers** — API definition (`auth.proto`, `user.proto`, `tokens.proto`)
- **Go gRPC** — High-performance implementation
- **JWT Tokens** — Stateless authentication with access + refresh token rotation
- **Go Module** — `mkaascs.v1.auth;authv1`