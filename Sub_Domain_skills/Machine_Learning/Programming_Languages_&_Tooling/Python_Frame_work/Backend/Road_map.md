# 🐍 PYTHON BACKEND ROADMAP (COMPLETE MASTER TREE)
# Rule: only "-" bullets + indentation (deep knowledge checklist)

=====================================================================
FOUNDATIONS (backend prerequisites)
=====================================================================

- Python runtime mastery (backend-useful parts only)
  - functions
    - parameters & argument binding rules
      - positional arguments
        - ordering
          - left-to-right binding
      - keyword arguments
        - name-based binding
          - collisions (same param set twice)
      - defaults
        - evaluation time (definition-time)
          - mutable default pitfall
            - sentinel pattern (object() / None + check)
      - positional-only parameters
        - "/" separator
          - when to use (API stability, speed, clarity)
      - keyword-only parameters
        - "*" separator
          - forcing named args in public APIs
      - variadic args
        - *args capture
          - tuple capture semantics
        - **kwargs capture
          - dict capture semantics
      - call-time unpacking
        - *iterable expansion
          - list/tuple/range
            - generator
              - custom iterator (__iter__/__next__)
          - mixing explicit + expanded positionals
            - f(a, *it, b)
              - order guarantees
          - mismatch errors
            - too many args
              - too few args
        - **mapping expansion
          - dict literal
            - dict comprehension
              - custom mapping (keys/__iter__)
          - key rules
            - keys must be strings
              - keys must match param names (unless **kwargs catches)
          - collision errors
            - explicit keyword duplicates **mapping
        - combined
          - f(*args, **kwargs)
            - forwarding pattern in wrappers/decorators
  - exceptions
    - exception hierarchy
      - BaseException vs Exception
    - try/except/else/finally
      - cleanup patterns
        - context managers
    - raise
      - chaining
        - raise X from Y
  - OOP (backend patterns)
    - classes
      - instance state
        - initialization (__init__)
      - class vs instance attributes
        - shared mutable pitfalls
      - methods
        - instance methods
        - classmethods (alternate constructors)
        - staticmethods (utility namespace)
      - properties
        - validation on set
      - inheritance
        - super()
          - cooperative multiple inheritance
        - MRO concept
      - composition (prefer for services)
        - dependency injection pattern
  - iteration model
    - iterables vs iterators
      - generators
        - yield
          - streaming responses / pipelines
  - typing (backend correctness)
    - type hints
      - request/response models
      - service interfaces
    - typing constructs
      - Optional / Union
      - Literal
      - Protocol (structural typing)
      - Generic/TypeVar (repositories/services)
  - concurrency model awareness
    - threads
      - IO-bound patterns
        - locks
    - processes
      - worker model
    - async/await
      - event loop concept
        - coroutines
          - tasks
            - cancellation semantics

- OS + dev environment
  - CLI basics
    - files/paths
      - permissions concept
  - environment variables
    - config via env
      - 12-factor config mindset
  - virtual environments
    - venv
      - pip
        - reproducible installs
  - packaging awareness (backend deployment)
    - pyproject.toml overview
      - dependencies
      - tooling config
  - git workflow (backend teams)
    - branching
    - code review basics

=====================================================================
WEB FUNDAMENTALS (protocols and browser rules)
=====================================================================

- HTTP core (must)
  - request structure
    - method
      - GET
      - POST
      - PUT
      - PATCH
      - DELETE
      - OPTIONS
        - preflight for CORS
    - URL
      - path
      - query parameters
    - headers
      - content-type
      - accept
      - authorization
      - cache-control
      - etag/if-none-match
      - content-length
      - host
    - body
      - JSON
      - form-data
      - multipart (file upload)
  - response structure
    - status codes
      - 1xx informational
      - 2xx success
      - 3xx redirects
      - 4xx client errors
      - 5xx server errors
    - headers
      - set-cookie
      - content-type
      - location
      - vary
    - body
      - JSON
      - HTML (if SSR)
  - semantics
    - idempotency
      - GET/PUT/DELETE idempotent
      - POST not idempotent
    - safe methods
      - GET/HEAD safe
  - caching behavior
    - browser cache
      - cache-control directives
    - CDN cache
      - caching keys (path/query/headers)
    - server cache
      - ETag strategy
        - conditional requests
  - connection model
    - keep-alive concept
    - timeouts
    - retries (careful with POST)
  - content negotiation
    - Accept headers
    - versioning via headers vs URL

- Browser security model (backend must know)
  - same-origin policy
    - what counts as origin
      - scheme + host + port
  - CORS
    - preflight OPTIONS
      - allowed origins
      - allowed methods
      - allowed headers
      - credentials mode
  - cookies
    - attributes
      - HttpOnly
      - Secure
      - SameSite
        - Lax/Strict/None
      - Domain/Path
      - Expires/Max-Age
  - sessions
    - session id cookie pattern
      - server-side session store
        - redis/db/in-memory tradeoffs
  - CSRF
    - why cookies cause CSRF risk
      - CSRF tokens
      - SameSite mitigation
    - framework protections (Django emphasizes CSRF, clickjacking, host validation, etc.) :contentReference[oaicite:4]{index=4}

=====================================================================
API DESIGN (REST + beyond)
=====================================================================

- REST design
  - resource modeling
    - nouns in paths
      - /users
      - /users/{id}
  - operations
    - list
      - pagination
        - offset/limit
        - cursor pagination
          - stable ordering requirement
    - retrieve
    - create
    - update
      - PUT full replace
      - PATCH partial update
    - delete
  - filtering/sorting
    - query syntax
      - whitelisting allowed fields
  - validation & errors
    - consistent error envelope
      - error code
      - message
      - details
  - versioning
    - URL versioning (/v1)
    - header versioning
  - idempotency keys
    - payments/order creation safety
  - rate limiting
    - token bucket concept
    - leaky bucket concept
    - per-user/per-IP/per-token
  - API documentation
    - OpenAPI/Swagger
      - request models
      - response models
      - auth schemes

- Non-REST APIs
  - GraphQL (optional)
    - schema
    - resolvers
    - N+1 problem
      - dataloader pattern
  - gRPC (optional)
    - protobuf
    - streaming calls
  - WebSockets (real-time)
    - handshake (HTTP upgrade)
    - auth for sockets
    - reconnect strategy
  - Server-Sent Events (SSE)
    - one-way streaming
    - backpressure considerations

=====================================================================
FRAMEWORKS (choose one primary, understand both models)
=====================================================================

- Server interfaces
  - WSGI (sync model)
    - typical for Flask/Django
  - ASGI (async model)
    - typical for FastAPI, async Django
  - deployment patterns for ASGI servers (uvicorn docs) :contentReference[oaicite:5]{index=5}

- FastAPI track (API-first, modern typing)
  - basics
    - app instance
      - routing
        - path params
        - query params
      - request body
        - Pydantic models
          - nested models
          - validators
          - custom types
      - response models
        - serialization
          - exclude/include
      - dependency injection
        - Depends()
          - request-scoped dependencies
          - auth dependencies
      - background tasks
        - BackgroundTasks
      - middleware
        - CORS middleware
        - logging middleware
      - exception handlers
        - HTTPException
        - custom exception mapping
  - async usage
    - async def endpoints
      - when to keep sync def
    - database IO in async
      - async drivers
      - connection pooling
  - OpenAPI customization
    - tags
    - security schemes
    - docs disabling in prod

- Django track (full-stack framework, can do APIs)
  - project layout
    - settings
      - environments (dev/stage/prod)
    - apps
      - app boundaries
  - request/response lifecycle
    - URL routing
    - views
      - function-based
      - class-based
        - mixins
    - middleware
      - auth/session/csrf
  - ORM
    - models
      - fields
      - relationships
        - one-to-one
        - foreign key
        - many-to-many
    - queries
      - select_related / prefetch_related
        - avoid N+1
    - migrations
      - schema evolution
        - rollback strategy
  - security (official Django security topics) :contentReference[oaicite:6]{index=6}
    - CSRF protection
    - XSS protection
    - SQL injection protection
    - clickjacking protection
    - host header validation
    - session security

- Flask track (minimal)
  - routing
  - request/response
  - blueprints
  - extensions ecosystem
  - production server separation (never built-in dev server)

=====================================================================
DATABASES (design + operations + performance)
=====================================================================

- SQL fundamentals (must)
  - relational modeling
    - entities
    - relationships
    - normalization
      - 1NF/2NF/3NF intuition
    - denormalization tradeoffs
  - queries
    - SELECT
      - WHERE
      - JOIN
        - inner/left/right
      - GROUP BY
      - HAVING
      - ORDER BY
      - LIMIT/OFFSET
  - constraints
    - primary keys
    - foreign keys
    - unique
    - not null
    - check constraints
  - indexes (critical)
    - B-tree concept
    - composite indexes
    - covering indexes idea
    - index selectivity
  - transactions
    - ACID
    - isolation levels
      - read committed
      - repeatable read
      - serializable (concept)
    - deadlocks concept
    - retries for serialization failures

- PostgreSQL (recommended)
  - connection management
    - pooling
  - query planning awareness
    - EXPLAIN basics
  - JSONB (hybrid use)
  - migrations
    - zero-downtime patterns (advanced)

- ORM layer
  - ORM concepts
    - models map to tables
    - queries build SQL
  - pitfalls
    - N+1 query problem
      - eager loading patterns
    - long transactions
    - hidden queries in serialization
  - schema migrations
    - forward migration
    - rollback
    - data migration

- NoSQL (optional but common)
  - document DB (MongoDB)
    - schema design (flexible but not free)
    - indexing
  - key-value stores (Redis)
    - caching
    - sessions
    - rate limiting
  - search stores (Elasticsearch/OpenSearch)
    - full-text search
    - indexing pipelines

=====================================================================
AUTHENTICATION + AUTHORIZATION (deep)
=====================================================================

- Authentication (who are you)
  - password auth
    - password hashing
      - bcrypt/argon2 concept
      - salt concept
    - login endpoints
      - brute-force mitigation
  - session-based auth
    - session id in cookie
      - server-side session store
        - rotation on login
    - CSRF protection required
  - token-based auth
    - bearer tokens
    - JWT
      - claims
      - expiry
      - signature verification
      - refresh token pattern
      - rotation & revocation strategy
  - OAuth2/OIDC (industry standard)
    - auth code flow concept
    - PKCE concept
    - identity provider integration
  - API keys (service-to-service)
    - rotation
    - scoping

- Authorization (what can you do)
  - RBAC
    - roles
      - role to permission mapping
  - ABAC (advanced)
    - policies based on attributes
  - object-level permissions
    - per-resource access checks
  - multi-tenant authorization
    - tenant isolation
      - row-level filtering

=====================================================================
SECURITY (backend survival checklist)
=====================================================================

- Input validation
  - schema validation
    - reject unknown fields (often)
  - type validation
  - size limits
    - request body limits
    - file upload limits

- Output safety
  - prevent leaking secrets
    - stack traces off in prod
    - safe error messages

- Common web vulns (OWASP-style)
  - SQL injection
    - parameterized queries
    - ORM safe patterns
  - XSS
    - escaping in templates
  - CSRF (cookie-based)
    - tokens / SameSite
  - SSRF
    - block internal IP ranges
  - path traversal
    - safe path join
  - command injection
    - avoid shell=True
  - insecure deserialization
    - avoid untrusted pickle
  - auth flaws
    - broken access control
    - session fixation
    - token replay
  - security headers (important)
    - HSTS
    - CSP (if serving HTML)
    - X-Frame-Options / frame-ancestors
    - Referrer-Policy
    - X-Content-Type-Options
  - HTTPS everywhere
    - TLS termination at proxy/load balancer

- Framework security features
  - Django has explicit built-in protections list (CSRF, XSS, clickjacking, etc.) :contentReference[oaicite:7]{index=7}

=====================================================================
CACHING + PERFORMANCE
=====================================================================

- Caching layers
  - client caching
    - cache-control
    - ETag / conditional GET
  - CDN caching
    - cache keys
    - purge/invalidation strategy
  - server caching
    - in-memory cache (process-local)
    - distributed cache (Redis)
      - TTL strategy
      - cache stampede mitigation
        - locks
        - stale-while-revalidate concept
  - database caching patterns
    - query result caching (careful)
    - materialized views concept (Postgres)

- Performance engineering
  - latency budgeting
    - p50/p95/p99 thinking
  - profiling
    - CPU profiling
    - memory profiling
  - N+1 elimination
  - pagination everywhere
  - background jobs for slow tasks
  - streaming responses (large outputs)
  - connection pooling
  - timeouts
    - DB timeout
    - HTTP client timeout
    - upstream timeout

=====================================================================
BACKGROUND JOBS + MESSAGING
=====================================================================

- Background jobs
  - use cases
    - email sending
    - video processing
    - report generation
  - job systems
    - Celery concept
      - broker (Redis/RabbitMQ)
      - workers
      - retries
      - dead-letter patterns (concept)
    - simpler queues (RQ concept)
  - scheduling
    - cron
    - periodic tasks
  - idempotency
    - safe retries

- Messaging / event-driven
  - message broker concepts
    - pub/sub
    - topics/queues
  - reliability
    - at-least-once delivery
      - deduplication
    - ordering
    - consumer groups
  - outbox pattern (advanced)
    - DB transaction + event publishing consistency

=====================================================================
OBSERVABILITY (logs + metrics + traces)
=====================================================================

- Logging
  - structured logging (JSON logs)
    - request id correlation
    - user/tenant ids (careful)
  - log levels
  - redaction of secrets

- Metrics
  - application metrics
    - request count
    - latency histograms
    - error rates
  - system metrics
    - CPU/memory
    - GC behavior (if relevant)

- Tracing
  - distributed tracing concepts
    - spans
    - trace ids
  - instrumentation
    - middleware instrumentation
    - DB query spans

- Alerting
  - SLO/SLA mindset
  - paging rules
  - error budget concept

=====================================================================
TESTING (backend confidence)
=====================================================================

- Unit tests
  - pure logic tests
  - service layer tests
  - mocking external systems

- Integration tests
  - DB integration
    - migrations in CI
  - external API integration
    - contract tests concept

- API tests
  - endpoint tests
  - auth tests
  - permission tests
  - pagination/filter tests
  - idempotency tests

- Load tests (advanced)
  - baseline throughput
  - p95 latency under load
  - soak tests (long-running)

=====================================================================
DEPLOYMENT (production reality)
=====================================================================

- App server concepts
  - WSGI servers (Gunicorn)
  - ASGI servers (Uvicorn)
    - worker model
      - number of workers strategy
    - graceful shutdown
    - health endpoints
  - reverse proxy
    - Nginx concept
    - TLS termination
    - request size limits
    - timeouts

- Uvicorn deployment guidance exists officially :contentReference[oaicite:8]{index=8}
  - process manager usage
  - proxy usage
  - resilience considerations

- Containerization
  - Dockerfile
    - minimal base images
    - non-root user
    - env-based config
    - healthcheck
  - docker-compose (local dev)
    - app + db + redis

- CI/CD
  - pipeline stages
    - lint
    - type check
    - tests
    - security scan (concept)
    - build artifact
    - deploy
  - migrations in deploy
    - safe migration order
  - rollback strategy
    - blue/green
    - canary

- Cloud basics
  - compute
    - VM vs containers vs serverless
  - storage
    - object storage for files
  - managed DB
  - secrets management
    - never commit secrets
  - load balancer
    - health checks
    - sticky sessions (avoid if possible)

=====================================================================
SCALING + ARCHITECTURE (senior backend)
=====================================================================

- Scaling types
  - vertical scaling
  - horizontal scaling
    - stateless services goal
      - shared session store if needed

- Reliability patterns
  - timeouts
  - retries
    - exponential backoff
    - jitter concept
  - circuit breaker concept
  - bulkheads concept
  - rate limiting
  - backpressure
    - queues
    - shedding load

- Data consistency patterns
  - transactions
  - eventual consistency
  - sagas concept
  - CQRS concept

- Architecture choices
  - monolith
    - modular monolith
  - microservices
    - service boundaries
    - API gateway concept
    - service discovery concept

=====================================================================
PROJECT STRUCTURE (how real backends are organized)
=====================================================================

- Layering (typical)
  - API layer (routers/controllers)
    - request parsing/validation
    - auth middleware/dependencies
  - service layer
    - business rules
    - transactions boundary
  - data access layer
    - repositories
    - ORM models
    - raw SQL modules
  - integrations layer
    - external API clients
    - message broker client
  - common utilities
    - config
    - logging
    - error types
    - metrics/tracing

- Configuration management
  - settings objects
    - env overrides
    - per-environment configs
  - secrets separation

=====================================================================
WHAT “BACKEND COMPLETE” MEANS (final checklist)
=====================================================================

- You can build an API with:
  - clean routes
  - validation
  - auth + permissions
  - DB schema + migrations
  - caching
  - background jobs
  - observability
  - tests
  - secure defaults
  - production deployment with rollback plan
