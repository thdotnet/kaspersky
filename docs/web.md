# Create a Zoner scan micro-service :new: :construction:

```bash
$ docker run -d -p 3993:3993 malice/zoner web

INFO[0000] web service listening on port :3993
```

## Now you can perform scans like so

```bash
$ http -f localhost:3993/scan malware@/path/to/evil/malware
```

> **NOTE:** I am using **httpie** to POST to the malice micro-service

```bash
HTTP/1.1 200 OK
Content-Length: 124
Content-Type: application/json; charset=UTF-8
Date: Sat, 21 Jan 2017 05:39:29 GMT

{
  "zoner": {
    "infected": true,
    "result": "EICAR.Test.File-NoVirus",
    "engine": "1979756",
    "updated": "20170707"
  }
}
```
