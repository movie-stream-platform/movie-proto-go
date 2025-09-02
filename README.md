# Go Protocol Buffer Stubs

Generated Go stubs for Movie Platform gRPC services.

## Overview
This package contains auto-generated Go structs and interfaces from Protocol Buffer definitions for the Movie Platform microservices architecture.

## Generated Services
- **Common**: Base request/response patterns, error handling, pagination, common types
- **User**: User management, profiles, preferences, watchlists, ratings, history
- **Auth**: Authentication, registration, sessions, tokens, permissions, MFA
- **Movie**: Movie content, search, media assets, catalog, streaming metadata
- **Recommendation**: ML-based recommendations, behavior analysis, content similarity
- **Playback**: Streaming management, progress tracking, quality adaptation
- **Notification**: User notifications, email, push, marketing communications

## Go Module
This package is a Go module with the following structure:

```go
module github.com/movieplatform/proto
```

## Dependencies Required
```go
require (
    google.golang.org/grpc v1.64.0
    google.golang.org/protobuf v1.33.0
    google.golang.org/grpc/cmd/protoc-gen-go-grpc v1.3.0
)
```

## Usage Example
```go
import (
    "github.com/movieplatform/proto/common"
    "github.com/movieplatform/proto/user"
)

// Create base request
baseRequest := &common.BaseRequest{
    RequestId: "req-123",
    AuthToken: "jwt-token",
}

// Use in service calls
request := &user.CreateUserRequest{
    BaseRequest: baseRequest,
    Username:    "john_doe",
    Email:       "john@example.com",
}
```

## Package Structure
```
github.com/movieplatform/proto/
├── common/          # Base types, error handling, pagination
├── user/            # User management services
├── auth/            # Authentication services
├── movie/           # Movie content services
├── recommendation/  # Recommendation engine services
├── playback/        # Streaming services
└── notification/    # Notification services
```

## Regeneration
To regenerate these stubs, run from the project root:
```bash
./proto/generate_proto.sh --go-only
```

## Notes
- Generated from Protocol Buffer definitions in `proto/` directory
- Uses Protocol Buffers v1.33.0
- Compatible with gRPC v1.64.0
- All services follow consistent naming conventions
- Includes comprehensive error handling and validation
