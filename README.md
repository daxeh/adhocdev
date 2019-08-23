Adhoc dev [daxeh/adhocdev](https://my-json-server.typicode.com/daxeh/adhocdev)


# README

## Quickstart

Create `db.json`

```
touch db.json
```

Generate data

```bash
$ curl "https://randomuser.me/api/?inc=name,location,email,picture&nat=au&page=1&results=20&format=pretty" | jq 'del(.info)' | jq .results | jq to_entries | jq 'map( (.value.id = 10000+.key ) | .value)' | jq -S
```

Query endpoint
