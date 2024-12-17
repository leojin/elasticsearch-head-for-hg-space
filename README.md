# elasticsearch-head

## 1. Deploy ES On Huggingface

### File `Dockerfile`

```dockerfile
FROM elasticsearch:8.16.0

ENV ES_JAVA_OPTS="-Xms12g -Xmx12g"
ENV discovery.type=single-node
ENV xpack.security.enabled=false
```

### File `README.md`

Add app_port in metadata.

```markdown
---
app_port: 9200
---
```

## 2. Run EsHead For HG instance

```bash
npm install
npm run start
```

## 3. Visit EsHead

```text
http://localhost:9100/?base_uri=https://<<huggingface-userName>>-<<huggingface-spaceName>>.hf.space&auth_token=<<huggingface-token>>
```

- huggingface-userName
- huggingface-spaceName
- huggingface-token: https://huggingface.co/settings/tokens, add read permissions to repos.
