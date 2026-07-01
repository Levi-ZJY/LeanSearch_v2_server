# LeanSearch v2 UCLA Server


## Quick Start


<!-- LeanSearch-v2 Standard Mode is deployed at `http://131.179.184.52:8000` -->


<!-- 1. This server address is on UCLA’s internal network. **Please connect to the campus network or UCLA VPN before accessing it.** -->


UCLA LeanSearch-v2 has been deployed on the public internet. Please do not share the access URL casually.

1. Standard mode API call:

CURL：

```
curl -u leansearch:x4xDV5PPtRokKXrG6OdL0rGd \
  -X POST https://causing-usage-disclaimer-still.trycloudflare.com/search \
  -H 'Content-Type: application/json' \
  -d '{"query": ["the order of a group element divides the order of the group"], "num_results": 10}'
```

Python:
```
import requests
import json

URL = "https://causing-usage-disclaimer-still.trycloudflare.com"
AUTH = ("leansearch", "x4xDV5PPtRokKXrG6OdL0rGd")

r = requests.post(
    f"{URL}/search",
    auth=AUTH,
    json={"query": ["the order of a group element divides the order of the group"],
          "num_results": 10},
    timeout=120,
)

print(json.dumps(r.json(), indent=2, ensure_ascii=False))
```

2. For Reasoning mode, since it is based on Standard mode with some additional processing using Claude Sonnet 4.5, you can follow the [LeanSearch-v2](https://github.com/frenzymath/LeanSearch-v2) repository to run it. (Note that Reasoning mode seems much slower than Standard mode)



