# Open311 GitHub Adapter
Middleware adapter to create a read-write proxy of the GitHub Issues API as an Open311 GeoReport v2 endpoint

General Architecture:

- GeoReport services and services definitions can be specified as YML or JSON in the repository and either servied directly or rendered first via Jekyll
- GeoReport requests are stored as YML in issues
- Any non-public information in a request is encrypted with an endpoint owner's public key, but the encrypted values are publicly accessible
- Requests can be created directly via the GitHub Issues interface and the adapter will still support minimal mapping to the GeoReport spec
