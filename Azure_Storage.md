# Azure Storage

- Storage Performance types-

  - Standard
  - Premium

- When choosing Premium Performance under Storage Account we get follwoign options-

  - File Shares
  - Block Blobs
  - Page Blobs

  - Account
    - Container
      - Blobs

### Blob Storage

- Service used for storing videos, images, docs etc. is Blob Service
- It is also used for storign disk files as VHD file.
- Default Access Tier is Hot.
- Frequently access objects should have Hot Access Tier.
- If objects dont have frequent access then it should be having Cool Access Tier.
- Archive access tier is used where objects are stored and not being accessible.
  - To access it needs to be re-hydrated (moving back to Hot or Cool) and it may take several hours.

### Redundancy Options

- LRS, GRS, ZRS, GZRS
