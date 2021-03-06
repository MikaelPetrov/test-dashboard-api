### How to work

Clone a repository
```bash
git clone https://github.com/MikaelPetrov/test-dashboard-api.git
```

Install dependencies
```bash
npm install
```

Run server
```bash
npm start
```

### API

```
GET     /sites                Get a list of sites
GET     /sites/[id]           Get a site by id
GET     /tests                Get a list of tests
GET     /tests/[id]           Get a test by id
```

### Data types

```typescript
enum Type {
  CLASSIC = "CLASSIC",
  SERVER_SIDE = "SERVER_SIDE",
  MVT = "MVT"
}

enum Status {
  DRAFT = "DRAFT",
  ONLINE = "ONLINE",
  PAUSED = "PAUSED",
  STOPPED = "STOPPED",
}

interface Site {
  id: number;
  url: string;
}

interface Test {
  id: number;
  name: string;
  type: Type;
  status: Status;
  siteId: number;
}
```
